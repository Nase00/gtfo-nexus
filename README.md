This repository is **deprecated**, please refer to https://github.com/Nase00/gtfo

# GTFO Nexus
*Host controller for GTFO modules*

## -> [Action Items](./ACTION_ITEMS.md)

## Configuration

*Note: This configuration is still a work-in-progress and subject to change*

Hardware:
- Raspberry Pi 2 Model B v1.1 running JESSIE (other models and distros likely work, but are untested)
- Raspberry Pi-compatible **long-range** WiFi dongle
- ~1ft ethernet cable
- *n* number of [Particle Photons](https://store.particle.io)
- RGB LEDs

## Setup

#### Photon Boards
1. Setup each device to Particle's cloud service.
2. Load the [VoodooSpark firmware](https://github.com/voodootikigod/voodoospark) onto each board.
3. Load the boards' access tokens and device id's into environment variables.

#### Raspberry Pi
1. Load Debian JESSIE variant onto Raspiberry Pi.
2. Configure SSH and other desired settings.

*Steps 3-5 are optional, follow them if no other reliable WiFi hotspots are available*
3. Make certain the Raspiberry Pi has an internet connection working via `eth0`
4. [Install a DHCP server and turn `wlan0` into a WiFi access point](http://raspberrypihq.com/how-to-turn-a-raspberry-pi-into-a-wifi-router/).
5. Install and run this software via:

```
git clone https://github.com/Nase00/gtfo-nexus.git
cd gtfo-nexus
node gtfo.js
```
