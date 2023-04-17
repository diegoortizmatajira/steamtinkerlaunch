# Steam Tinker Launch (cegc fork)
[![GitHub version](https://img.shields.io/github/v/tag/daailouivan/steamtinkerlaunch?label=version&style=flat-square)](https://github.com/daailouivan/steamtinkerlaunch/releases/latest)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/daailouivan/steamtinkerlaunch?style=flat-square)
[![GitHub license](https://img.shields.io/github/license/daailouivan/steamtinkerlaunch.svg?style=flat-square)](https://github.com/daailouivan/steamtinkerlaunch/blob/dev/LICENSE)

## Overview
This is an **unofficial** fork of [SteamTinkerLaunch](https://github.com/sonic2kk/steamtinkerlaunch) which reimplements support for GameConqueror and CheatEngine with newer SteamTinkerLaunch versions.

These tools were removed from SteamTinkerLaunch v12.0 and later following concerns that invasive anti-cheat programs such as Easy Anti-Cheat would permanently ban users who have these tools or any reference to these tools on their system, following their behaviour on Windows.

For more background on why these tools were removed, see the [SteamTinkerLaunch FAQ](https://github.com/sonic2kk/steamtinkerlaunch/wiki/FAQ#where-did-cheat-enginegameconqueror-go).

Issues encountered when using this fork should **not** be reported on the official SteamTinkerLaunch repository.

## Usage
Using SteamTinkerLaunch as a [compatibility tool](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Steam-Compatibility-Tool) is the intended way of using it with Proton games, which are the primary type of game supported by cheat tools. Once SteamTinkerLaunch is installed, force it as a compatibility tool for your chosen game from the list of compatibility tools. You can also set SteamTinkerLaunch as the default compatibility tool for all applications from the Steam Play settings of the Steam client. Keep in mind that if you force SteamTinkerLaunch as a compatibility tool, Steam will always download the Windows release of the game.

You can also use SteamTinkerLaunch with native Linux games by adding `steamtinkerlaunch %command%` to the game's launch options. Keep in mind that cheat tool support for native Linux games may be limited.

## Command Line
SteamTinkerLaunch has several [command line options](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Command-Line) which can be useful outside Steam, such as for installing modding tools. You can run `steamtinkerlaunch help` for a full list of available commands.

## Installation
This fork of SteamTinkerLaunch should be installed manually. You can grab it from git or from the [releases page](https://github.com/daailouivan/steamtinkerlaunch/releases).

### Dependencies
The general SteamTinkerLaunch [manual installation steps](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Installation#manual-installation) should mostly apply. You must still ensure you have the relevant hard dependencies installed.

As well as these, **_`innoextract` is also required_** for cheat tool functionality. You can install it from your package manager on Linux Desktop.

## Troubleshooting
### Logs
Logs are written into the `LOGDIR` as defined in the [Global Menu](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Global-Menu) or [Global Config](https://github.com/sonic2kk/steamtinkerlaunch/wiki/Configuration-Files#Global-Config) (by default, this is usually `~/.config/steamtinkerlaunch/logs/`). The verbosity of the logfile depends on the `WRITELOG` variable, where `0` is no logging, `1` is less verbosity and `2` is most verbosity.

SteamTinkerLaunch produces a number of logs, including game-specific log files. For logs that have a Steam AppID in them (such as Proton logs), there is usually a symlink for the log file with the game's name to make it easier to identify logs.

SteamTinkerLaunch may also store additional logging information in `/dev/shm/steamtinkerlaunch`.

## Disclaimer
These cheat tools (including text references to them) may cause you to be **permanently banned** in games which use invasive anti-cheat tools such as Easy Anti-Cheat or battlEye. While this fork restores the functionality it is **not** responsible if you get banned for using them.

## License
SteamTinkerLaunch is licensed under the GNU General Public License v3.0. See [LICENSE](https://github.com/daailouivan/steamtinkerlaunch/blob/master/LICENSE) for more information.
