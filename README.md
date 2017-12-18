# homebridge-sonos-starter
[Homebridge](https://github.com/nfarina/homebridge) Accessory to start presets via [node-sonos-http-api](https://github.com/jishi/node-sonos-http-api).

## Usecase
Automate regular playback in Homekit e.g. start a favorite playlist or radio in a specific room at a specific volume with Siri.

## Prerequisites

[Homebridge](https://github.com/nfarina/homebridge) and [node-sonos-http-api](https://github.com/jishi/node-sonos-http-api) are installed.

## Installation

Clone this repository, change into that forlder and execute the following
```
npm install
npm link
```

## Configuration

Add accessory to `~/.homebridge/config.json` of [Homebridge](https://github.com/nfarina/homebridge) like this:

```
...
"accessories": [
    ...
    {
        "accessory": "SonosStarter",
        "name": "Morning Music",
        "apiBaseUrl": "http://localhost:5005",
        "preset": "workday-morning"
    },
    ...
```

- `accessory` needs to be `SonosStarter`
- `name` is the name that HomeKit will use
- `apiBaseUrl` is the base URL where [node-sonos-http-api](https://github.com/jishi/node-sonos-http-api) lives
- `preset` is the [node-sonos-http-api](https://github.com/jishi/node-sonos-http-api)-preset that should be started

## Finally

Restart [Homebridge](https://github.com/nfarina/homebridge) and that's it. Tested with node 6 on a raspi.
