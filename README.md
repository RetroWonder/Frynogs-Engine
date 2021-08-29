# Friday Night Funkin Frynogs

Frynogs Engine repo.

![e6PbQF](https://user-images.githubusercontent.com/87475004/126863954-831fd7c8-e764-4f24-b41d-78c36b25956b.png)


[![Build status](https://ci.appveyor.com/api/projects/status/npxuk38tmfi7md8k?svg=true)](https://ci.appveyor.com/project/ManFire100/frynogs-engine)


## Credits / shoutouts

- [Manfire100)] - Programmer
- [RetroWonder/Gabriel M] - Logo

# How to download precompiled binaries? (windows only)

click on the bulid button, below the logo.

# Build instructions

THESE INSTRUCTIONS ARE FOR COMPILING THE GAME'S SOURCE CODE!!!

IF YOU WANT TO JUST DOWNLOAD THE LATEST MAJOR VERSION, GO TO RELEASES AND DOWNLOAD!
IF YOU WANT TO COMPILE THE GAME YOURSELF OR USE A MINOR VERSION, CONTINUE READING!!!

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
3. Run `haxelib git polymod https://github.com/larsiusprime/polymod.git` to install Polymod.
4. If don't have Xcode, to compile for Mac, run first `xcrun --install.`
5. Run `haxelib git discord_rpc https://github.com/Aidan63/linc_discord-rpc` to install Discord RPC.

You should have everything ready for compiling the game! Follow the guide below to continue!

At the moment, you can optionally fix the transition bug in songs with zoomed out cameras.
- Run `haxelib git flixel-addons https://github.com/HaxeFlixel/flixel-addons` in the terminal/command-prompt.

### Compiling game

Once you have all those installed, it's pretty easy to compile the game. You just need to run 'lime test html5 -debug' in the root of the project to build and run the HTML5 version. (command prompt navigation guide can be found here: [https://ninjamuffin99.newgrounds.com/news/post/1090480](https://ninjamuffin99.newgrounds.com/news/post/1090480))

To run it from your desktop (Windows, Mac, Linux) it can be a bit more involved. For Linux, you only need to open a terminal in the project directory and run 'lime test linux -debug' and then run the executable file in export/release/linux/bin. For Windows, you need to install Visual Studio Community 2019. While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:
* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows SDK (10.0.17763.0)

This will install about 4GB of crap, but once that is done you can open up a command line in the project's directory and run `lime test windows -debug`. Once that command finishes (it takes forever even on a higher end PC), you can run FNF from the .exe file under export\release\windows\bin
As for Mac, you must run 'lime test mac -debug'. 

### Additional guides

- [Command line basics](https://ninjamuffin99.newgrounds.com/news/post/1090480)

# A note

Now i will distribute pre-compiled binaries only of major versions. I 'm too slow to keep the rhythm (update, lime test,update, lime test,update, lime test,update, lime test,).
