# Team Fortress 2 Config

## Table of Contents

* [What you get](#what-you-get)
  * [Additional actions](./cfg/actions.cfg)
  * [Improved settings](./cfg/settings.cfg)
  * [Shift-modifiers](#shift-modifiers)
  * [Weapon-specific settings](#weapon-specific-settings)
  * [Quick loadout switch](#quick-loadout-switch)
  * [Quick class switch](#quick-class-switch)
* [Download](#download)
* [Install](#install)
* [Uninstall](#uninstall)
* [Contributing](#contributing)

## What you get

This is not an [FPS config](https://github.com/mastercoms/mastercomfig). This config is a framework that provides missing features to TF2:

* [Additional actions](./cfg/actions.cfg) (e.g. `alertSniper`, `alertSpyOnEngi`)
* [Improved settings](./cfg/settings.cfg) (e.g. interp, fov, and crosshair)
* [Modules](./cfg/modules/README.md): _Shift-modifiers, Weapon settings, Quick loadout switch, Quick class switch_

You should be able to swap in and out different parts of this config and customize the specifics.

### Shift-modifiers

These are some of shift actions that I use. For a more full explanation of how to work with these, read [this](./cfg/modules/key_modifiers/).

* <kbd>SHIFT</kbd>+<kbd>MOUSE1</kbd> -- _Alert Spy_
* <kbd>SHIFT</kbd>+<kbd>MOUSE2</kbd> -- _Alert Sniper ahead_
* <kbd>SHIFT</kbd>+<kbd>MOUSE3</kbd> -- _Alert Spy is sapping engineer's buildings_
* <kbd>SHIFT</kbd>+<kbd>MWHEELUP</kbd> -- _Alert Incoming_
* <kbd>SHIFT</kbd>+<kbd>MWHEELDOWN</kbd> -- _Alert Incoming from behind_

#### Class-specific shift-modifiers

You can define class-specific versions of these modifiers for your customization pleasure :beers:

For example, on Spy I have <kbd>MOUSE4</kbd> execute the `lastdisguise` command, but on Pyro <kbd>MOUSE4</kbd> does a `detonatorJump`. You can create shift-modified versions of these. I define these class-specific overrides in that class's `key_modifiers.cfg` file.

Here are my class-specific overrides:

<details>
  <summary>Engineer</summary>
  <ul>
    <li>
      <kbd>MOUSE3</kbd> -- <em>Destroy sentry and build</em>
    </li>
    <li>
      <a href="./cfg/classes/engineer/key_modifiers.cfg">
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
      <a href="./cfg/classes/pyro/key_modifiers.cfg">
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
      <a href="./cfg/classes/soldier/key_modifiers.cfg">
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
      <a href="./cfg/classes/spy/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

### Weapon-specific settings ([:arrow_upper_right:](./cfg/modules/weapon_settings.cfg))

This lets you load settings per weapon slot. For example, you could change the crosshair color for different weapons like [Mr. Slin does](https://github.com/misterslin/CrosshairSwitcher).

Currently I use it to turn the viewmodel on/off for certain slots.

#### Class-specific weapon settings

By default I turn the viewmodel on for all of the slots, but I change that with some classes. I define these class-specific overrides in that class's `key_modifiers.cfg` file.

<details>
  <summary>Engineer</summary>
  <li>
    <a href="./cfg/classes/engineer/weapon_settings.cfg">
      <code>weapon_settings.cfg</code>
    </a>
  </li>
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
  <li>
    <a href="./cfg/classes/scout/weapon_settings.cfg">
      <code>weapon_settings.cfg</code>
    </a>
  </li>
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
  <li>
    <a href="./cfg/classes/soldier/weapon_settings.cfg">
      <code>weapon_settings.cfg</code>
    </a>
  </li>
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
  <li>
    <a href="./cfg/classes/spy/weapon_settings.cfg">
      <code>weapon_settings.cfg</code>
    </a>
  </li>
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

### Quick loadout switch ([:arrow_upper_right:](./cfg/modules/loadout_switch.cfg))

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

### Quick class switch ([:arrow_upper_right:](./cfg/modules/class_switch.cfg))

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

## Download [[:arrow_double_down:](https://github.com/reeddunkle/reed-config/archive/master.zip)]

If the link doesn't work, click the green "Clone or download" button on the top right of this page and click "Download ZIP".

<img src="https://i.imgur.com/OX9A0dt.png" width="50%" height="50%" alt="Download ZIP">

1.  Unzip my config to its own folder.
1.  Rename the config folder from `reed-config-master` to just `reed-config`. (`master` is the [branch](https://guides.github.com/introduction/flow/))

## Install

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it should be:

* Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
* macOS: `~/Library/Application Support/Steam/SteamApps/common/team fortress 2/tf/`
* Linux: `~/.steam/steam/SteamApps/common/Team Fortress 2/tf/`

You can also:

1.  Right click TF2 in your Steam library
1.  Click Properties
1.  Go to the "Local Files" tab
1.  Click the "Browse Local Files..." button
1.  Open the `tf` folder

### 1. Back up your `cfg`

I recommend [making a backup](./BACKUP.md) of your current `cfg` folder in case you want to revert to your current setup. Also, remove any other configs you've got in place. You can even back up your whole `tf` folder if you want, it isn't that large.

### 2. Drop in my files

To install my files, open the `custom` folder that's inside of the `tf` folder. If `custom` doesn't exist, just create it.

1.  Navigate into `tf/custom/`
1.  Drop my config into here

You should now have my config located at `tf/custom/reed-config`. Restart TF2 and everything should be setup.

**Note**: If anything is wonky after you install my config, please [create an issue](https://github.com/reeddunkle/reed-config/issues).

## Uninstall

Did you try out my config but want to revert to your backup? Read [this](./UNINSTALL.md).

## Contributing

You can always fork and edit. If you notice better ways that I could be doing things, I welcome pull requests.

## Thanks

Thanks to the community. This scripting takes getting used to, and I'm still figuring out the nuances. I couldn't have gotten into it if you all weren't posting your scripts.

## License

[MIT](./LICENSE.txt)
