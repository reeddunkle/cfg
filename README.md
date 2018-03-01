# Team Fortress 2 Config

## Motivation

A lot of the TF2 scripts and configs out there in the wild are hacky, incomplete, and messy. The majority that I've seen seem to be made up of copied-and-pasted scripts mashed together, which makes the config unreliable and difficult to modify.

If you want to add a feature, you should only have to define it one place, wire it up, and know that it won't break anything else. This config is architected to make that a priority. It is easy and safe to edit my specific scripts and put yours in place.

If you have a feature request and you aren't sure how to make it happen, open an [issue](https://github.com/reeddunkle/reed-config/issues) and I'll try to help.

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

All of my actions -- the things that I want to happen with I hold shift and press a button -- are defined in my [actions.cfg](./cfg/custom/key_modifiers/actions.cfg) file. For a more in-depth explanation of how to work with the modifiers, check out [this](./cfg/custom/key_modifiers/README.md).

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
      <a href="./cfg/custom/engineer/key_modifiers.cfg">
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
      <a href="./cfg/custom/pyro/key_modifiers.cfg">
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
      <a href="./cfg/custom/soldier/key_modifiers.cfg">
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
      <a href="./cfg/custom/spy/key_modifiers.cfg">
        <code>key_modifiers.cfg</code>
      </a>
    </li>
  </ul>
</details>

### Class-specific, weapon-specific settings

This is architected to allow you to perform an action when a given class selects a specific weapon. I set this up because I wanted to have my viewmodel drawn for certain weapons but not for others. With the Engineer for example, I want the viewmodel when I use the Wrench (slot 3) and the Pistol (slot 2), but I want to turn it off when I use the Shotgun (slot 1).

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

The [settings file](./cfg/custom/settings.cfg) runs when the game loads.

## Install

### Download my files

Download a ZIP of this repo [here](https://github.com/reeddunkle/reed-config/archive/master.zip), or by clicking the green "Clone or download" button on the top right of this page.

![Download ZIP](http://i.imgur.com/lF3GOYJ.png)

1.  Unzip my config.
1.  Delete the zip, you don't need it anymore.
1.  Rename the config folder from `reed-config-master` to just `reed-config`.

### Install my files

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it may be:

* Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
* macOS: `~/Library/Application Support/Steam/SteamApps/common/team fortress 2/tf/`
* Linux: `~/.steam/steam/SteamApps/common/Team Fortress 2/tf/`

#### 0. Back up your `cfg` folder

Create a backup of the `cfg` folder that's inside of this `tf` folder. To do this, copy and paste the folder, and give it a different name, e.g. "cfg BACKUP". You can call it whatever you want.

The point is to have a version of your current config to revert to if you ever want to go back. This `cfg` folder is pretty small so it won't hurt anything to have an extra copy sitting around.

I recommend zipping it and e-mailing it to yourself (or uploading it somewhere) so that you always have a version to refer to.

#### 1. Remove/disable other custom configs

Before you install my config, you need to remove any configs that you've previously made or installed. If you already have a custom config if your `tf/custom` folder, just remove it while you're trying mine out.

If you're using custom files inside your `tf/cfg` folder, you should remove them while you're trying mine out. Since you've got your `cfg` folder backed up already, you can just delete any class-specific files you might have (e.g. `spy.cfg`) as well as your `autoexec.cfg`.

This shouldn't be necessary, but if you're curious or ambitious you can reset your `tf/cfg` folder to its factory defaults:

1.  Disable cloud-sync (instructions [below](https://github.com/reeddunkle/reed-config#2-optional-disable-cloud-sync)).
1.  Delete the `cfg` folder.
1.  Remove anything in the custom folder.
1.  In your TF2 launch options, add `-autoconfig`.
1.  Start TF2 to restore the default config.
1.  Close TF2 and remove `-autoconfig` from the launch options.

#### 2. (Optional) Disable cloud-sync

You might as well temporarily disable Steam's cloud-sync to prevent Steam from overwriting your cloud-backup version. I think the sync is useful though, so I'd turn it back on once you're ready to commit to the new config.

To disable it:

1.  Open Steam and navigate to your Steam Library.
1.  Right-click on TF2 and select Properties.
1.  Select the Updates tab and uncheck the Enable Steam Cloud synchronization option.
1.  Click Close.

#### 3. Install my files

To install my files, open the `custom` folder that's inside of the `tf` folder. If `custom` doesn't exist, just create it.

1.  Navigate into `tf/custom/`.
1.  Move my config into here.

You should now have my config located at `tf/custom/reed-config`. Restart TF2 and everything should be setup.

## Uninstall

Tried out my config but want to revert to your backup?
Read [this](./cfg/custom/README.md).

## Contributing

You can always fork and edit. If you notice better ways that I could be doing things, I welcome pull requests.

## Thanks

Thanks to the community. This scripting takes getting used to, and I'm still figuring out the nuances. I couldn't have gotten into it if you all weren't posting your scripts.

## License

[MIT](./LICENSE.txt)
