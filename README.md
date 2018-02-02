# Team Fortress 2 Scripts

## Download Files

Most TF2 players aren't programmers, and don't have git setup.

You can download a zip of this repo [here](https://github.com/reeddunkle/cfg/archive/master.zip), or by clicking the green "Clone or download" button on the top right of this repo's [homepage](https://github.com/reeddunkle/cfg).

![Download ZIP](http://i.imgur.com/lF3GOYJ.png)

## Install

Navigate to your `tf` folder. If you've chosen a custom location for your Steam folder, then you know where it is. If you used the default install path, then it may be:

* Windows: `C:\Program Files (x86)\Steam\steamapps\common\Team Fortress 2\tf\`
* macOS:

First you should create a backup of the `cfg` folder that's inside of this `tf` folder. Just copy and paste the folder and give it a different name. _Note that it is probably worth temporarily disabling Steam's cloud-sync also. That way none of my changes will persist if you don't like them._

Once you've got it backed up, copy or move all of the files from this repo into your `cfg` folder. If you get warnings about any of the files already existing, choose to replace them.

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
