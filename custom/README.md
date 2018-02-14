## Restore your backup

If you want to remove my config and restore your backup, follow these steps.

1. Delete the `cfg` folder (containing my files).
1. Create another backup of your backup (to be safe). The cloud-sync stuff can overwrite files, so if you have any problems after reinstalling the backup it will be very helpful to have a pristine backup to use.
1. Rename one of the backs to `cfg`.
1. Restart TF2, go into a custom server and see if your buttons are all working.

There's a good chance that some of them won't have reverted correctly.

Here's a list of the keys that my config changes as of 2/13/2018. It's most likely that these are the keys that aren't resetting.

* <kbd>MOUSE1</kbd>
* <kbd>MOUSE2</kbd>
* <kbd>MOUSE3</kbd>
* <kbd>MOUSE4</kbd>
* <kbd>MWHEELUP</kbd>
* <kbd>MWHEELDOWN</kbd>
* <kbd>ALT</kbd>
* <kbd>SHIFT</kbd>
* <kbd>SPACE</kbd>
* <kbd>HOME</kbd>
* <kbd>END</kbd>
* <kbd>TAB</kbd>
* <kbd>1</kbd>, <kbd>2</kbd>, <kbd>3</kbd>, <kbd>4</kbd>, <kbd>5</kbd>
* <kbd>`</kbd>
* <kbd>F10</kbd>
* _The arrow keys_
* _The keypad numbers_

If any of your keys aren't working properly, try these steps.

1. Navigate into the extra backup of your `cfg`
1. Create a copy of the file `config.cfg` and name it `config_backup.cfg`
1. Move `config_backup.cfg` from your backup cfg folder into the actual `cfg` folder
1. Launch TF2
1. Open the console and type `exec config_backup.cfg`, press Enter

This should hopefully, fingers crossed, restore your keys to the state that you had them.

If this doesn't work, let me know.
