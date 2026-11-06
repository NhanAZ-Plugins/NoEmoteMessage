# NoEmoteMessage

Mute Bedrock emote announcements for players joining Axolotl-PM

[![CI](https://github.com/NhanAZ-Plugins/NoEmoteMessage/actions/workflows/build.yml/badge.svg)](https://github.com/NhanAZ-Plugins/NoEmoteMessage/actions/workflows/build.yml)
[![Latest release](https://img.shields.io/github/v/release/NhanAZ-Plugins/NoEmoteMessage)](https://github.com/NhanAZ-Plugins/NoEmoteMessage/releases/latest)
[![License](https://img.shields.io/github/license/NhanAZ-Plugins/NoEmoteMessage)](https://github.com/NhanAZ-Plugins/NoEmoteMessage/blob/master/LICENSE)
[![Discord](https://img.shields.io/discord/986553214889517088?label=Discord&logo=discord&logoColor=white&color=5865F2)](https://discord.gg/j2X83ujT6c)


## Requirements and compatibility

- Axolotl-PM with plugin API `5.0.0`.
- PHP 8.1 or newer in the Axolotl-PM 5 toolchain.

The [build workflow](.github/workflows/build.yml) pins the Axolotl-PM source used for PHPStan at maximum level. Runtime evidence for a particular server version belongs to the corresponding verified build or release. Compatibility with every Axolotl-PM 5.x release has not been established.

## Installation and behavior

Download `NoEmoteMessage.phar` from a verified [GitHub release](https://github.com/NhanAZ-Plugins/NoEmoteMessage/releases), place it in the server's `plugins/` directory and restart the server. The plugin has no configuration, commands, permissions or external plugin dependencies.

When the server sends a `StartGamePacket`, the plugin sets `levelSettings->muteEmoteAnnouncements` to `true`. This affects the recipient's client setting. It does not delete messages that other plugins send through separate APIs.

## Building and testing

The [build workflow](.github/workflows/build.yml) runs PHPStan at maximum level, builds and inspects the PHAR with [DevTools](https://github.com/AxolotlBucketLabs/DevTools), and uploads the verified artifact. A clean server startup confirms the plugin loads. Seeing the announcement change requires a Bedrock client test.

## License and support

NoEmoteMessage is licensed under [GPL-3.0](LICENSE). For help, use [NhanAZ Discord](https://discord.gg/j2X83ujT6c).
