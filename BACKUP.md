## Back up your `cfg` folder

Create a backup of the `cfg` folder that's inside of this `tf` folder. To do this, copy and paste the folder, and give it a different name, e.g. "cfg BACKUP". You can call it whatever you want.

The point is to have a version of your current config to revert to if you ever want to go back. This `cfg` folder is pretty small so it won't hurt anything to have an extra copy sitting around.

I recommend zipping it and e-mailing it to yourself (or uploading it somewhere) so that you always have a version to refer to.

## Remove/disable other custom configs

Before you install my config, you need to remove any configs that you've previously made or installed. If you already have a custom config inside your `tf/custom` folder, remove it while you're trying mine out.

If you're using custom files inside your `tf/cfg` folder, you should remove them while you're trying mine out. Since you've got your `cfg` folder backed up already, you can delete any class-specific files you might have (e.g. `spy.cfg`) as well as your `autoexec.cfg`.

This shouldn't be necessary, but if you're curious you can reset your `tf/cfg` folder to its factory defaults:

1.  Disable cloud-sync ([below](#disable-cloud-sync)).
1.  Delete the `cfg` folder.
1.  Remove anything in the custom folder.
1.  In your TF2 launch options, add `-autoconfig`.
1.  Start TF2 to restore the default config.
1.  Close TF2 and remove `-autoconfig` from the launch options.

## Disable cloud-sync

You might as well temporarily disable Steam's cloud-sync to prevent Steam from overwriting your cloud-backup version. I think the sync is useful though, so I'd turn it back on once you're ready to commit to the new config.

To disable it:

1.  Open Steam and navigate to your Steam Library.
1.  Right-click on TF2 and select Properties.
1.  Select the Updates tab and uncheck the Enable Steam Cloud synchronization option.
1.  Click Close.
