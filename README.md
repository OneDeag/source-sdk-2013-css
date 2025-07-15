# Copyright-Strike: Source

The aim of this project is to have a base version of Counter-Strike: Source on the new SDK with additional fixes.

To play this mod, you will need to have both Counter-Strike: Source and Source SDK 2013 MP installed. Both will need to be on the newest versions. 

## Build instructions

Clone the repository using the following command:

`git clone https://github.com/OneDeag/source-sdk-2013-css/`

### Windows

Requirements:
 - Source SDK 2013 Multiplayer installed via Steam
 - Visual Studio 2022 with the following workload and components:
   - Desktop development with C++:
     - MSVC v143 - VS 2022 C++ x64/x86 build tools (Latest)
     - Windows 11 SDK (10.0.22621.0) or Windows 10 SDK (10.0.19041.1)
 - Python 3.13 or later

Inside the cloned directory, navigate to `src`, run:
```bat
create_cstrike.bat
```
This will generate the Visual Studio project `counterstrike.sln` which will be used to build your mod.

Then, on the menu bar, go to `Build > Build Solution`, and wait for everything to build.

The default launch options should be already filled in for the `Release` configuration.

### Linux - 

INSTRUCTIONS ARE PULLED STRAIGHT FROM THE SDK, THESE NEED TO BE UPDATED. WILL NOT WORK AS-IS RIGHT NOW. 

Requirements:
 - Source SDK 2013 Multiplayer installed via Steam
 - podman

Inside the cloned directory, navigate to `src`, run:
```bash
./buildallprojects
```

This will build all the projects related to the SDK and your mods automatically against the Steam Runtime.

You can then, in the root of the cloned directory, you can navigate to `game` and run your mod by launching the build launcher for your mod project, eg:
```bash
./mod_tf
```

*Mods that are distributed on Steam MUST be built against the Steam Runtime, which the above steps will automatically do for you.*

## Distributing your Mod

There is guidance on distributing your mod both on and off Steam available at the following link:

https://partner.steamgames.com/doc/sdk/uploading/distributing_source_engine

## Additional Resources

- [Valve Developer Wiki](https://developer.valvesoftware.com/wiki/Source_SDK_2013)

## License

The SDK is licensed to users on a non-commercial basis under the [SOURCE 1 SDK LICENSE](LICENSE), which is contained in the [LICENSE](LICENSE) file in the root of the repository.

For more information, see [Distributing your Mod](#markdown-header-distributing-your-mod).

## History

The project was originally based on FriskTheFallenHuman's CSS-Base. The repository for that project was deleted and this fork seems to be the only existing version of the code:

https://github.com/blackletum/css-base

CSS-base itself is a fork of another project called CSS-Community:

https://github.com/DeadZoneLuna/css-community

Which itself was based on the SourcePlusPlus CSS Port:

https://github.com/SCell555/Source-PlusPlus
