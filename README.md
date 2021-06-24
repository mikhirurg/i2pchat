<p>
  <a href="https://www.bountysource.com/teams/i2pchat" title="Bountysource">
    <img src="https://img.shields.io/bountysource/team/i2pchat/activity">
  </a>
</p>

# I2PChat (formerly I2P Qt Messenger)

## Donations

For I2PChat based on Flutter (including Android target) and maybe more platforms in the future:

 * BTC: 36GLhgAo8JwdxH1ATjHJ7bLK37mUbKaRHw
 * GOST: GX41zZcqKy81CzyDCmnpRtpCKpR1fwEDet https://gostco.in/

## Status

[![Build status appveyor MinGW32](https://ci.appveyor.com/api/projects/status/0tanjnojnlpksug6?svg=true)](https://ci.appveyor.com/project/wipedlifepotato/i2pchat)
[![Build Status travis linux(xenial)](https://travis-ci.org/wipedlifepotato/i2pchat.svg?branch=master)](https://travis-ci.org/wipedlifepotato/i2pchat)

## Screenshots

![screenshot-roster](https://vituperative.github.io/i2pchat/screenshots/main.png) ![screenshot-chat](https://vituperative.github.io/i2pchat/screenshots/chat.png)

### Features

 * Direct peer-to-peer communications without server requirements
 * File transfer between contacts
 * Control online visibility on a per-contact basis
 * Optional, customizable b32.i2p web page to display profile
 * Emoticon support

### Current news

* July, 2020
  * Set ECIES and ED25519 as default sigtype/encryption
  * Add support for optional web page to display user profile at .b32 address
  * Remove insecure DSA_SHA1 from Signature Types
  * Add ECIES (Ratchet) encryption type to new profiles (UI option coming soon!)

* June, 2020:
   * Fixed crash of close chat window
   * Fixed crash of url link in chat
   * Added $HOME/.i2pchat/ directory support for using from /usr/bin
   * Pre inited optarg
   * Core changes
   * Ci pre-inited. Works for windows now
   * Created .deb package for ubuntu/debian x86_64
   * Created Windows build for 32 bit, which will works on 64 bits
   * Design changes
   * Fix offline message crash
* June, 2020: dr\|z3d starts work on renovating the user interface
* 5 Jan, 2017: Original repo at http://git.repo.i2p/w/I2P-Messenger-QT.git was fully merged here

### Build instructions

 * Install prerequisites:

```
sudo apt-get install qt5-qmake qt5-default build-essential libqt5multimedia5 qtmultimedia5-dev libqt5svg5-dev
```

 * To prepare for compilation, run qmake:
   - Release: `qmake I2PChat.pro "CONFIG += release"`
   - Debug: `qmake I2PChat.pro "CONFIG += debug"`

 * To compile:
   - `make -j NUMBER_OF_PROCESSOR_CORES` e.g `make -j8`
   - or `make` to compile single-threaded


### Downloads (pre-built binaries)

* Latest Windows (Win32/64) build from: <a href="https://ci.appveyor.com/project/wipedlifepotato/i2pchat/build/artifacts">https://ci.appveyor.com/project/wipedlifepotato/i2pchat/build/artifacts</a>

### Running

On Linux, `make` creates `I2PChat` executable in the current folder. Run it with `./I2PChat`.

* You will need to enable the SAM application bridge in your router: for Java I2P via <a href="http://127.0.0.1:7657/configclients">Client Configuration</a> or for i2pd via i2pd.conf's [SAM] section.
* As of version 0.2.31, the DSA_SHA1 Signature type is no longer available. The recommended (and default) Signature Type is now: EdDSA_SHA512_Ed25519
* Select 'Online' from the dropdown menu on the main window. When you first go online, your unique address (Destination) will be created when connecting to SAM
* Your settings and contacts will be stored in `~/.i2pchat/` on Linux-based systems, or `%APPDATA%\Roaming\I2PChat\` on Windows

## License

Licensed under GPLv2.

## Credits

<em>
  Thanks
    * To the German anonymous guy who is the author of original code for I2PQtMessenger AKA i2pchat,
    * to eche|on and kytv for the work on it and preserving the source code for it at various places,
    * to anonymous contributors who took part in the project and commented,
    * to drz3d for community organisz`::::*`zsation skills and work and commits of graphics and commits of code made by more or less anonymous programmers, and
    * to wipedlifepotato for the failures healings/bugfixes healthy patches that wipedlifepotato submitted to drz3d (and drz3d committed them to the codebases and forks of i2pchat, for the community benefit).
    * Special Thanks are also to forgotten unknown contributors and 
    * to others who took part in the i2pchat project!
</em>

## Enjoy!

... &emdash; And Please Be Good! Otherwise Good Creatures Will Find You And Prosecute!
