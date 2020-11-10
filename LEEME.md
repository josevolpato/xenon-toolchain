# xenon-toolchain
[English](README.md) | Español | [Português brasileiro](LEIAME.md)

## Descripción
Herramientas de compilación Homebrew para Xbox360.

## Versiones de binarios precompilados (solamente 64 bits)
* [Windows](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-windows-x86_64-pc-msys2.7z)
* [Linux](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-linux-x86_64-pc-linux-gnu.7z)
* [Mac OS X](https://github.com/josevolpato/xenon-toolchain/releases/download/v1.0/xenon-toolchain-macosx-x86_64-apple-darwin.7z)

## Instrucciones de script de compilación manual
*** Preste atención a los permisos de usuario disponibles en el directorio /usr/local/ ***

### Windows
1. Instalar [MSYS2](https://www.msys2.org/)
2. Actualizar paquetes de MSYS2:</br>
   `pacman -Syu`
3. Abra el terminal MSYS2 e instale las dependencias de compilación:<br>
   `pacman -S wget gcc make gmp-devel mpfr-devel mpc-devel base-devel`
4. Cambiar a ESTE directorio:<br/>
   `cd /this/directory/location/`
5. Ejecutar el script de compilación:<br/>
   `./build-xenon-toolchain`
6. Agregue estas líneas a su script de inicio de sesión (bash.rc, zsh.rc, Variables del sistema, etc) y recarga tu terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
7. Prueba tu entorno de desarrollo:<br/>
  ```
  xenon-gcc
  ```
  Deberías haber recibido este mensaje:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Linux
1. Abra el terminal y actualice sus paquetes de la distro:
     - Arch / Manjaro:  
    `sudo pacman -Syu`
     - Debian / Ubuntu / Mint:  
    `sudo apt-get update`
2. Instalar dependencias de compilación:
    - Arch / Manjaro:  
    `sudo pacman -S wget gcc make base-devel`
    - Debian / Ubuntu / Mint:  
    `sudo apt-get install wget gcc make build-essentials`
3. Cambiar a ESTE directorio:<br/>
   `cd /this/directory/location/`
4. Ejecutar el script de compilación:<br/>
   `./build-xenon-toolchain`
5. Agregue estas líneas a su script de inicio de sesión (bash.rc, zsh.rc, Variables del sistema, etc) y recarga tu terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
6. Prueba tu entorno de desarrollo:<br/>
  ```
  xenon-gcc
  ```
  Deberías haber recibido este mensaje:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Mac OS X
1. Instalar [homebrew](https://brew.sh/)
2. Instalar dependencias de compilación:<br/>
   `brew install gsed wget gcc make`
3. Cambiar a ESTE directorio:<br/>
   `cd /this/directory/location/`
4. Ejecutar el script de compilación:<br/>
   `./build-xenon-toolchain`
5. Agregue estas líneas a su script de inicio de sesión (bash.rc, zsh.rc, Variables del sistema, etc) y recarga tu terminal:<br/>
  ```
  export DEVKITXENON=/usr/local/xenon
  export PATH=$DEVKITXENON/bin:$PATH
  ```
6. Prueba tu entorno de desarrollo:<br/>
  ```
  xenon-gcc
  ```
  Deberías haber recibido este mensaje:<br/>
  ```
  xenon-gcc: fatal error: no input files
  compilation terminated.
  ```

### Continuar con la construcción de libxenon
Después de descargar / construir la cadena de herramientas, le gustará construir [libxenon]() también!

## Referencias y agradecimientos
[MSYS2](https://www.msys2.org/)  
[GCC](https://gcc.gnu.org/)  
[Binutils](https://www.gnu.org/software/binutils/)
[Newlib](https://sourceware.org/newlib/)
[Homebrew](https://brew.sh/)  
[ge0rg](https://github.com/ge0rg/libxenon)  
[Free60](https://github.com/Free60Project)  
[Xenia](https://github.com/xenia-project/libxenon)  
[acabey](https://github.com/acabey/libxenon)  

## Licencia
![license](https://img.shields.io/badge/license-GLP-green)