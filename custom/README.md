## Removing my config (warning)

My config changes some bindings. If you want to remove my config, reverting to your backup might not be as simple as swapping out the `cfg` folder.

First, delete the `cfg` folder (containing my files). Next, instead of just renaming your backup `cfg`, create another copy of your backup (be extra safe) and name it `cfg`. The cloud-sync stuff can overwrite files, so if you have any problems after reinstalling the backup it will be very helpful to have a pristine backup to refer to.

Here's a list of the keys that my config changes as of 2/2/2018. I'll try to keep it updated. It's most likely that one of these keys will be broken.

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
* _The arrow keys_
* _The keypad numbers_

If any of your keys aren't working properly, go into the extra backup of your `cfg` and copy the file `config.cfg` into the `cfg` folder that's being used. **You need to change the name.** That's important. Call it `backup_config.cfg`. (Note that you shouldn't call it `default_config.cfg` because that's a reserved filename.)

Finally, launch the game. Open the console and run `exec backup_config`. This should hopefully, fingers crossed, re-bind your keys to the state that you had them.

If this doesn't work, let me know. If you made it this far but didn't create any backups, I'm sorry.
