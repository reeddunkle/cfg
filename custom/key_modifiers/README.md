# Key Modifiers

Current keys wired up:

* MOUSE1
* MOUSE2
* MOUSE3
* MOUSE4
* ALT
* MWHEELUP
* MWHEELDOWN
* `
* F10

If you want to use one of these keys but change the behavior, see below "[Change a current key state](#change-a-current-key-state)". If you want to wire up a new key and define its behavior, see below "[Create your own modifier states](#create-your-own-modifier-states)". If you want to create class-specific versions of key states that you've already defined, see below "[Create class-specific states](#create-class-specific-states)".

## Change a current key state

With my setup, if I hold SHIFT and press MOUSE2 it fires `alertSniper`, which actually executes this in your Tf2 console `voicemenu 1 0; say_team There's a sniper ahead;`. Let's say you want to change <kbd>SHIFT</kbd>+<kbd>M2</kbd> to instead let your teammates know that you popped uber.

Here's the current code:

```
# actions.cfg
alias alertSniper "voicemenu 1 0; say_team There's a sniper ahead;"

# shift_modifiers/index.cfg
alias shiftModifyKey_M2 "alias +M2_key alertSniper; alias -M2_key swallowAction;"
```

### Create your new action

```
# actions.cfg
alias alertUberPopped "say_team Get excited, it's Uber time."
```

### Set your modifier function to use the new action

```
# shift_modifiers/index.cfg
alias shiftModifyKey_M2 "alias +M2_key alertUberPopped; alias -M2_key swallowAction;"
```

### Swallow Action?

There's a known issue in Tf2 scripting where you don't want to use `bind` within an `alias`. I've tried it a few times, and I've gotten some bugs. To avoid it, I leave my shift modifier keys bound to an alias which has a `+/-` state. That's the `+M2_key` and `-M2_key` you see above in the shift modifier function.

When a key is bound to something without a `+/-` state, it just executes the thing that it's bound to. But when it's bound to something with a `+/-` state it fires the "`+`" action on keydown, and the "`-`" action on keyup.

This is important for actions like `attack`, which continues until you let up the key. In the example above, MOUSE2 is bound to `+M2_key`, which means that on keyup it will try to execute an action called `-M2_key`. The console prints an error if that action doesn't exist.

In the above example, you want MOUSE2 keydown to execute `alertUberPopped`, but that action doesn't have a "`-`" state. Rather than let the game catch my error and print to console, I just perform a cheap action. It's hacky.

### Alert Uber and also Use Uber

Imagine that you don't just want <kbd>SHIFT</kbd>+<kbd>M2</kbd> to alert that you popped uber, but you also want the same mouse press to actually pop the uber. I'll use the `alertUberPopped` from above, but I'll create a new action to perform the actual action that we want the key to use:

```
# actions.cfg
alias alertUberPopped "say_team Get excited, it's Uber time."
alias +uberAndAlert "+attack2; alertUberPopped;"  // <-- This is what you want MOUSE2 to do
alias -uberAndAlert "-attack2;"
```

Next you put this action in your modifier function:

```
# shift_modifiers/index.cfg
alias shiftModifyKey_M2 "alias +M2_key +uberAndAlert; alias -M2_key -uberAndAlert;"  // <-- Now your action does have both states
```

## Create your own modifier states

The point of a modifier is to give a key an additional state. Normally it performs a default action, but when you hold a "modifier key" it changes the key to perform a different action.

You need to define and wire up both of these states.

Let's say you want to wire up `F1`. You want its unmodified state to fake an uber call. You want its shift-modified state to just call "incoming".

### Create new actions

```
# actions.cfg
alias alertUberReady "voicemenu 1 7;"
alias alertIncoming "voicemenu 0 1;"
```

### Create your new reset function

Define a new function which resets your key to its unmodified state.

```
# index.cfg
alias resetKey_F1 "alias +F1_key alertUberReady; alias -F1_key swallowAction;"
```

### Create your new modifier function

```
# shift_modifiers/index.cfg
alias shiftModifyKey_F1 "alias +F1_key alertIncoming; alias -F1_key swallowAction;"
```

### Include your new reset function in `resetKeys.cfg`

When this file executes, it fires all of the `resetKey` functions. It's important to add your new function to this list.

```
# resetKeys.cfg
resetKey_M1
resetKey_M2
resetKey_M3
resetKey_M4
resetKey_ALT
resetKey_MWHEELUP
resetKey_MWHEELDOWN
resetKey_F1  //  <-- You add this line
```

### Include your new modifier function in `shiftModifiyKeys.cfg`

When this file executes, it fires all of the `shiftModify` functions. It's important to add your new modifier to this list.

```
# shift_modifiers/shiftModifyKeys.cfg
shiftModifyKey_M1
shiftModifyKey_M2
shiftModifyKey_M3
shiftModifyKey_M4
shiftModifyKey_ALT
shiftModifyKey_MWHEELUP
shiftModifyKey_MWHEELDOWN
shiftModifyKey_F1  //  <-- You add this line
```

### Bind `F1` to your new key state

Finally, you need to bind the key to the new variable.

```
# init.cfg
bind F1 +F1_key
```

## Create class-specific states

For example, on Spy I use MOUSE4 to use the `lastdisguise` action, but on Pyro I use it to perform `detonatorJump`. On both I keep the shift-modified version of MOUSE4 the same which is to `sayGameIsHard`.

In [`pyro/key_modifiers.cfg`](../pyro/key_modifiers.cfg), first I create my new action. Then I create my new reset function. Finally I execute it the reset function, because I'm changing MOUSE4's _unmodified_ state. If I were changing its modified state, I wouldn't preemptively initalize the function.

```
# pyro/key_modifiers.cfg
alias +detonatorJump "+jump; +duck; +CUSTOM_attack; +CUSTOM_attack2;"
alias -detonatorJump "-jump; -duck; -CUSTOM_attack; -CUSTOM_attack2;"

alias resetKey_M4 "alias +M4_key +detonatorJump; alias -M4_key -detonatorJump;"

//  Init
resetKey_M4
```

The Spy's [`key_modifier.cfg`](../spy/key_modifiers.cfg) is the same, except `lastdisguise` is a predefined action so I don't have to create it at the start.

_Remember that this class-specific method only works if you've previously created and wired-up a key modifier._

## Create a new modifier key

Maybe you want to make ALT a modifier too.

`TODO: write this section.`

## Note

I'm still actively working on and refactoring this system. If you have ideas on how to improve it please [create an issue](https://github.com/reeddunkle/cfg/issues) and I'll get in touch with you asap.
