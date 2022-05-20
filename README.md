# ParaLLEl-N64-XboxOne
This is a modified version of the [ParaLLEl-N64](https://github.com/libretro/parallel-n64) libretro core that is intended to be used with Xbox One and Series consoles. All credit goes to the libretro Team, and all of the [contributors](https://github.com/libretro/parallel-n64/graphs/contributors) behind the core, as well as [JustMeDaFaq](https://github.com/JustMeDaFaq) for the [ANGLE](https://github.com/google/angle) implementation.

The main changes to the core are the following:

- The radius used in the emulate_game_controller_via_libretro.c file is set to a value of 80, which limits the emulated analog stick range. This can have some negative impact on games, such as making it impossible to jump out of water in Super Mario 64. I changed this to a value of 100, which allows the analog stick to reach the full range of an N64 stick while still allowing for more subtle and slow movements.
- A new ANGLE directory has been added, making it simple to build this core without needing to provide any additional files.

**Click here to read the original ParaLLEl-N64 README file.**

# Build Instructions

**Prequisites**:

- [MSYS2](https://www.msys2.org/) with the [mingw-w64-x86_64-toolchain](https://packages.msys2.org/group/mingw-w64-x86_64-toolchain) packages installed.
- **Optional**: Either [Git for Windows](https://gitforwindows.org/) or the [Git](https://packages.msys2.org/package/git) package for MSYS2.

**Step 1: Getting the source code**

You can either use the command `git clone https://github.com/GABO1423/ParaLLEl-N64-XboxOne.git` with a command prompt, or download the source code as a zip file directly from GitHub:

![image](https://user-images.githubusercontent.com/35014183/164373033-25607e57-24c5-4987-91bc-3e43c7f02387.png)

**Step 2: Setting up the build**

Once the source code is downloaded, go into the ANGLE directory and unzip the ANGLE Library.7z file. You should end up with two folders: `lib` and `include`.
Next, open MSYS2 (make sure you open the MINGW 64-bit variant).

![image](https://user-images.githubusercontent.com/35014183/164373294-7e12f238-b013-40df-b686-1ef24c541d9d.png)

Then use the `cd` command to navigate to where the code is located.

**Step 3: Begin the build**

Simply type `make` on MSYS2, press Enter, and watch it build! You should end up with a file called "mupen64plus_next_libretro.dll" if everything goes correctly.
