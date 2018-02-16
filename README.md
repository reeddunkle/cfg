# Team Fortress 2 Config

## Motivation

A lot of the TF2 scripts and configs out there in the wild are hacky, incomplete, and messy. The majority that I've seen seem to be made up of copied-and-pasted scripts mashed together, which makes the config unreliable and difficult to modify.

If you want to add a feature, you should only have to define it one place, wire it up, and know that it won't break anything else. This config is architected to make that a priority. It is easy and safe to edit my specific scripts and put yours in place.

If you have a feature request and you aren't sure how to make it happen, open an [issue](https://github.com/reeddunkle/cfg/issues) and I'll try to help.

## Overview

This config gets you a few things:

* Shift-modifiers
* Class-specific key bindings
* Class-specific, weapon-specific settings
* Quick loadout switch
* Quick class switch
* Game settings

You can edit all of the specifics.

### Shift-modifers

All of my actions -- the things that I want to happen with I hold shift and press a button -- are defined in my [actions.cfg](./custom/key_modifiers/actions.cfg) file. For a more in-depth explanation of how to work with the modifiers, check out [this](./custom/key_modifiers/README.md).

* <kbd>SHIFT</kbd>+<kbd>MOUSE1</kbd> -- _Alert Spy_
* <kbd>SHIFT</kbd>+<kbd>MOUSE2</kbd> -- _Alert Sniper ahead_
* <kbd>SHIFT</kbd>+<kbd>MOUSE3</kbd> -- _Alert Spy is sapping engineer's buildings_
* <kbd>SHIFT</kbd>+<kbd>MWHEELUP</kbd> -- _Alert Incoming_
* <kbd>SHIFT</kbd>+<kbd>MWHEELDOWN</kbd> -- _Alert Incoming from behind_
* <kbd>SHIFT</kbd>+<kbd>MOUSE4</kbd> -- _Say Game is hard_
* <kbd>SHIFT</kbd>+<kbd>ALT</kbd> -- _Say Affirmative_

### Class-specific key bindings

I define any class-specific actions in that class's `key_modifiers.cfg` file.

<details>
  <summary>Engineer</summary>
  <ul>
    <li>
      <kbd>MOUSE3</kbd> -- <em>Destroy sentry and build</em>
    </li>
    <li>
      <a href="./custom/engineer/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

<details>
  <summary>Pyro</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Detonator jump</em>
    </li>
    <li>
      <a href="./custom/pyro/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

<details>
  <summary>Soldier</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Rocket jump</em>
    </li>
    <li>
      I don't use this anymore, so I've commented this out (by adding two slashes). If you want to use it, remove the `//` from Line 4 and Line 7.
    </li>
    <li>
      <a href="./custom/soldier/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

<details>
  <summary>Spy</summary>
  <ul>
    <li>
      <kbd>MOUSE4</kbd> -- <em>Last diguise</em>
    </li>
    <li>
      <a href="./custom/spy/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

### Class-specific, weapon-specific settings

This is architected to allow you to perform an action when a given class selects a specific weapon. I set this up because I wanted to have my viewmodel drawn for certain weapons but not for others. With the Engineer for example, I want the viewmodel when I use the Wrench, but I want to turn it off for the Shotgun (slot 1) and Pistol (slot 2).

<details>
  <summary>Engineer</summary>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
      <th>Slot 4</th>
      <th>Slot 5</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Scout</summary>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Soldier</summary>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

<details>
  <summary>Spy</summary>
  <table>
    <tr>
      <th></th>
      <th>Slot 1</th>
      <th>Slot 2</th>
      <th>Slot 3</th>
      <th>Slot 4</th>
    </tr>
    <tr>
      <td>View model?</td>
      <td>No</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
  </table>
</details>

### Quick loadout switch

<details>
  <summary>Use the arrow keys to change your loadout.</summary>
  <ul>
    <li>:arrow_left: Loadout A</li>
    <li>:arrow_up: Loadout B</li>
    <li>:arrow_right: Loadout C</li>
    <li>:arrow_down: Loadout D</li>
  </ul>
</details>

I also have <kbd>ALT</kbd> bound to switch to Loadout A for quick resupply.

### Quick class switch

<details>
  <summary>Use the numpad numbers to change your class.</summary>
  <ol>
    <li>Scout</li>
    <li>Soldier</li>
    <li>Pyro</li>
    <li>Demo</li>
    <li>Heavy</li>
    <li>Engineer</li>
    <li>Medic</li>
    <li>Sniper</li>
    <li>Spy</li>
  </ol>
</details>

### Game settings

The [settings file](./custom/settings.cfg) runs when the game loads.

## Install

### Download my files

You can download a zip of this repo [here](https://github.com/reeddunkle/cfg/archive/master.zip), or by clicking the green "Clone or download" button on the top right of this repo's [homepage](https://github.com/reeddunkle/cfg).

![Download ZIP](http://i.imgur.com/lF3GOYJ.png)

### Install my files

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it may be:

* Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
* macOS: `~/Library/Application Support/Steam/SteamApps/common/team fortress 2/tf/cfg`
* Linux: `~/.steam/steam/SteamApps/common/Team Fortress 2/tf/cfg`

#### 1. Back up your `cfg` folder

Create a backup of the `cfg` folder that's inside of this `tf` folder. To do this, copy and paste the folder, and give it a different name, e.g. "cfg BACKUP". You can call it whatever you want.

In step 3 we'll put my files into the `cfg` folder, so this way you'll have a version to revert to if you ever want to go back. The `cfg` folder is pretty small; it won't hurt anything to leave your backup lingering.

#### 2. Disable cloud-sync

I recommend temporarily disabling Steam's cloud-sync to prevent my config from overwriting yours in case you don't like it. I think the sync is useful though, so I'd turn it back on once you're ready to commit.

To disable it:

1. Open Steam and navigate to your Steam Library.
2. Right-click on TF2 and select Properties.
3. Select the Updates tab and uncheck the Enable Steam Cloud synchronization option.
4. Click Close.

#### 3. Move my files into `cfg`

To install my files, drag them into the `cfg` folder. Don't drag them into the backup folder that you created in step 1. If you get warnings about any of the files already existing, choose to replace them.

Restart TF2 and everything should be setup.

## Uninstall

Tried out my config but want to revert to your backup?
Read [this](./custom/README.md).

## Contributing

You can always fork and edit. If you notice better ways that I could be doing things, I welcome pull requests.

## Set up your own cfg repo

My `.gitignore` file lists all the default files. Copy it into your `cfg/` directory. You can turn the directory into a git repo (run `git init`) and it will ignore the default files, and only add the custom files you set up.

In the future, I'll add more detailed instructions for those new to GitHub.

## Thanks

Thanks to the community. This scripting takes getting used to, and I'm still figuring out the nuances. I couldn't have gotten into it if y'all weren't posting your scripts.

## License

[MIT](./LICENSE.txt)
