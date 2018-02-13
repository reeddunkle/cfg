# Team Fortress 2 Scripts

## Download Files

Most TF2 players aren't programmers, and don't have git setup.

You can download a zip of this repo [here](https://github.com/reeddunkle/cfg/archive/master.zip), or by clicking the green "Clone or download" button on the top right of this repo's [homepage](https://github.com/reeddunkle/cfg).

![Download ZIP](http://i.imgur.com/lF3GOYJ.png)

## Install

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it may be:

* Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
* macOS:

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

Make sure you've got your backup, and read [this](./custom/README.md).

## Contributing

You can always fork and edit. If you notice better ways that I could be doing things, I welcome pull requests.

## Set up your own cfg repo

My `.gitignore` file lists all the default files. Copy it into your `cfg/` directory. You can turn the directory into a git repo (run `git init`) and it will ignore the default files, and only add the custom files you set up.

In the future, I'll add more detailed instructions for those new to GitHub.

## Thanks

Thanks to the community. This scripting takes getting used to, and I'm still figuring out the nuances. I couldn't have gotten into it if y'all weren't posting your scripts.

## License

[MIT](./LICENSE.txt)
