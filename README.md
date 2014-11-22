![the hat](gfx/propellerhat.png) PropellerIDE [![Build Status](https://travis-ci.org/bweir/PropellerIDE.svg?branch=master)](https://travis-ci.org/bweir/PropellerIDE)
============

![the interface](gfx/interface.png "The PropellerIDE interface")

PropellerIDE is an easy-to-use, cross-platform development tool for the Parallax Propeller microcontroller.

Write Spin code, download programs to your Propeller board, and debug your applications with the built-in serial terminal.

- [Download PropellerIDE](https://lamestation.atlassian.net/wiki/display/PI/Downloads)

### Features

- Spin syntax highlighting, auto-complete, code suggestion, and auto-indent
- Unicode editing support
- Auto-detection of connected Propeller hardware
- Collapsible sidebar with function and program views
- Integrated serial terminal

### Planned Features

- Unified tree view showing hierarchy of objects and functinos
- Integrated Spin and Assembly help manual
- Plugin interface for extending the application

PropellerIDE was created using C++ and Qt.

## Building

Current PropellerIDE builds are manual, but the target is to build the application using an Amazon EC2 instance to make cross-platform support as easy as possible.

The following instructions have been prepared using clean EC2 Ubuntu and Windows Server instances.

### Building On Ubuntu

Run an update to ensure your apt repositories are up-to-date.

```
sudo apt-get update
```

Install the required dependencies.

```
sudo apt-get install git make g++ qt5-default zlib1g-dev
```

Checkout the project.

```
git clone https://github.com/lamestation/PropellerIDE.git PropellerIDE
cd PropellerIDE
make checkout
```

Type `make deb` in the project root to build a Debian package.

```
make deb
```

### Building On Windows

The easiest way to build on Windows is with QtCreator itself.

The automated build environment uses the following tools.

* MinGW
* MSYS
* Inno Setup 5
* Qt5

Type `make win` to execute the build.

```
make win
```

### Building On OS X

*Not yet available.*

## Clean Up

Type `make clean` to remove old build files.

```
make clean
```

## Credits

Originally developed by Steve Denson, Dennis Gately, and Roy Eltham.

**Related Projects**: [OpenSpin](https://github.com/parallaxinc/OpenSpin)
