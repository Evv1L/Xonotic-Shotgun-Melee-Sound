# Xonotic Shotgun Melee Sound
Inspired by [Xonotic Competitive Edition](https://rocketjump.zone/xce/). Thank you!<br>

I wanted a melee hit sound for a shotgun. I found this implementation on XCE, but I wanted to have it in my own Xonotic client.<br>
And instead of "Bonk" sound effect I use spank sound effect :)<br>

# Installation
Clone repo and move those files:
* Move sound effect file to your Xonotic data `/sound/weapons/` folder. Create if you don't have them. <br> Full path should look like this^: (`~.xonotic/data/sound/weapons/shotgun_melee_impact.ogg`). Of course you can make your own `.ogg `sound later.
* Move prebuilt `*progs.*` files to the root of your Xonotic data folder. <br> Should look like this: `~.xonotic/data/*progs.*`<br>

**BUT** these `progs` files are precompiled from Xonotic Git version (I didn't tested it on 0.8.2) and I recomend you to build your own `progs` like below.

# Compiling `progs` files
* Clone and compile Xonotic Git from this [offcial guide](https://gitlab.com/xonotic/xonotic/-/wikis/Repository_Access)
* Replace files in `qcsrc` in Xonotic game files `.../xonotic/data/xonotic-data.pk3dir/qcsrc`. You need to replace this:

```
qcsrc
└── common
    ├── sounds
    │   └── all.inc
    └── weapons
        └── weapon
            └── shotgun.qc
```
* Delete `csprogs-xonotic-*.pk3` file in `qcsrc` folder **AND** all `*progs.*` files in `.../xonotic/data/xonotic-data.pk3dir/` folder
* Recompile Xonotic changed files with `./all compile -r`
* Run the game and test it
