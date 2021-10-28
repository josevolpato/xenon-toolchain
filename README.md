# xenon-toolchain
English | [Español](LEEME.md) | [Português brasileiro](LEIAME.md)

## Description
Xenon toolchain for Xbox 360 homebrew development.

## Precompiled binaries releases (64 bits only)
* [Windows](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-windows-x86_64-pc-msys2.7z)
* [Linux](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-linux-x86_64-pc-linux-gnu.7z)
* [Mac OS X](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-macosx-x86_64-apple-darwin.7z)

## Manual build script instructions
*** Pay attention to avaliable user permissions on /usr/local/ directory ***

### Windows
1. Install [MSYS2](https://www.msys2.org/)
2. Update MSYS2 packages:</br>
   `pacman -Syu`
3. Open MSYS2 terminal and install build dependencies:<br>
   `pacman -S wget gcc make gmp-devel mpfr-devel mpc-devel base-devel`
4. Change to THIS directory:<br/>
   `cd /this/directory/location/`
5. Run Build Script:<br/>
   `./build-xenon-toolchain`
6. Add this lines to your login script (bash.rc, zsh.rc, System variables, etc) and reload your terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
7. Test your environment:<br/>
  ```
  xenon-gcc
  ```
  You should have received this message:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Linux
1. Open a terminal and update your distro packages:
     - Arch / Manjaro:  
    `sudo pacman -Syu`
     - Debian / Ubuntu / Mint:  
    `sudo apt-get update`
2. Install build dependencies:
    - Arch / Manjaro:  
    `sudo pacman -S wget gcc make base-devel`
    - Debian / Ubuntu / Mint:  
    `sudo apt-get install wget gcc make build-essentials`
3. Change to THIS directory:<br/>
   `cd /this/directory/location/`
4. Run Build Script and wait until it finishes:<br/>
   `./build-xenon-toolchain`
5. Add this lines to your login script (bash.rc, zsh.rc, System variables, etc) and reload your terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
6. Test your environment:<br/>
  ```
  xenon-gcc
  ```
  You should have received this message:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Mac OS X
1. Install [homebrew](https://brew.sh/)
2. Install build dependencies:<br/>
   `brew install gsed wget gcc make`
3. Change to THIS directory:<br/>
   `cd /this/directory/location/`
4. Run Build Script and wait until it finishes:<br/>
   `./build-xenon-toolchain`
5. Add this lines to your login script (bash.rc, zsh.rc, System variables, etc) and reload your terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
6. Test your environment:<br/>
  ```
  xenon-gcc
  ```
  You should have received this message:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Proceed with libxenon building
After download or build the toolchain, you'll like to build
[libxenon](https://github.com/josevolpato/libxenon) too!

## References and acknowledgements
[MSYS2](https://www.msys2.org/)  
[GCC](https://gcc.gnu.org/)  
[Binutils](https://www.gnu.org/software/binutils/)  
[Newlib](https://sourceware.org/newlib/)  
[Homebrew](https://brew.sh/)  
[ge0rg](https://github.com/ge0rg/libxenon)  
[Free60](https://github.com/Free60Project)  
[Xenia](https://github.com/xenia-project/libxenon)  
[acabey](https://github.com/acabey/libxenon)  

## License
![license](https://img.shields.io/badge/license-GLP-green)