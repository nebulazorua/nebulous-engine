# Friday Night Funkin: Andromeda Engine

"ANDROMEDA ENGINE IS GOATED" - bbpanzu

Made as an alternative to other engines because im a lil' bitch and thought I could take a shot, so I did.
- Fully rebindable controls, a brand new input system based on other rhythm games' (Though you can goto week 7's)
- VERY customisable, even down to judgement window presets
- SICK AS FUCK WEEK 6 SHADERS THAT YOU CAN ACTUALLY RUN!!! (SUCK ON THAT TABI) ((idk why they work though LOL THEY JUST DO ITS MAGIC))
- Scroll velocity

AND IM STILL WORKIN' ON IT

NOTE: ENGINE KINDA SORTA IN BETA STAGES RN
## OG Friday Night Funkin'

Play the Ludum Dare prototype here: https://ninja-muffin24.itch.io/friday-night-funkin
Play the Newgrounds one here: https://www.newgrounds.com/portal/view/770371
Support the project on the itch.io page: https://ninja-muffin24.itch.io/funkin
Get the source code: https://github.com/ninjamuffin99/Funkin

## Credits / shoutouts

- [ninjamuffin99](https://twitter.com/ninja_muffin99) - Programmer
- [PhantomArcade3K](https://twitter.com/phantomarcade3k) and [Evilsk8r](https://twitter.com/evilsk8r) - Art
- [Kawaisprite](https://twitter.com/kawaisprite) - Musician
- Nebula - Andromeda Engine
- [Quaver](https://github.com/Quaver/Quaver) - Scroll code

Shoutouts to Newgrounds and Tom Fulp for creatin' the best website and community on the internet

## Build instructions

THESE INSTRUCTIONS ARE FOR COMPILING THE GAME'S SOURCE CODE!!!

IF YOU WANT TO JUST DOWNLOAD AND INSTALL AND PLAY THE GAME NORMALLY, GO TO ITCH.IO TO DOWNLOAD THE GAME FOR PC, MAC, AND LINUX!!

https://ninja-muffin24.itch.io/funkin

IF YOU WANT TO COMPILE THE GAME YOURSELF, CONTINUE READING!!!

### Installing the Required Programs

First you need to install Haxe and HaxeFlixel. I'm too lazy to write and keep updated with that setup (which is pretty simple).
1. [Install Haxe 4.1.5](https://haxe.org/download/version/4.1.5/) (Download 4.1.5 instead of 4.2.0 because 4.2.0 is broken and is not working with gits properly...)
2. [Install HaxeFlixel](https://haxeflixel.com/documentation/install-haxeflixel/) after downloading Haxe

Other installations you'd need is the additional libraries, a fully updated list will be in `Project.xml` in the project root. Currently, these are all of the things you need to install:
```
flixel
flixel-addons
flixel-ui
hscript
newgrounds
```
So for each of those type `haxelib install [library]` so shit like `haxelib install newgrounds`

You'll also need to install a couple things that involve Gits. To do this, you need to do a few things first.
1. Download [git-scm](https://git-scm.com/downloads). Works for Windows, Mac, and Linux, just select your build.
2. Follow instructions to install the application properly.

Then for each of these type `haxelib git [libraryname] [library]` so `haxelib git polymod https://github.com/larsiusprime/polymod.git`
```
 polymod https://github.com/larsiusprime/polymod.git
discord_rpc https://github.com/Aidan63/linc_discord-rpc
hxvm-luajit https://github.com/nebulazorua/hxvm-luajit
linc_luajit https://github.com/nebulazorua/linc_luajit
```

You should have everything ready for compiling the game! Follow the guide below to continue!

At the moment, you can optionally fix the transition bug in songs with zoomed out cameras.
- Run `haxelib git flixel-addons https://github.com/HaxeFlixel/flixel-addons` in the terminal/command-prompt.

### Compiling game

Once you have all those installed, it's pretty easy to compile the game. You just need to run 'lime test html5' in the root of the project to build and run the HTML5 version. (command prompt navigation guide can be found here: [https://ninjamuffin99.newgrounds.com/news/post/1090480](https://ninjamuffin99.newgrounds.com/news/post/1090480))

To run it from your desktop (Windows, Mac, Linux) it can be a bit more involved. For Linux, you only need to open a terminal in the project directory and run 'lime test linux' and then run the executible file in export/release/linux/bin. For Windows, you need to install Visual Studio Community 2019. While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:
* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows SDK (10.0.17763.0)

This will install about 4GB of crap, but once that is done you can open up a command line in the project's directory and run `lime test windows`. Once that command finishes (it takes forever even on a higher end PC), you can run FNF from the .exe file under export\release\windows\bin
As for Mac, 'lime test mac' should work, if not the internet surely has a guide on how to compile Haxe stuff for Mac.

### Additional guides

- [Command line basics](https://ninjamuffin99.newgrounds.com/news/post/1090480)
