# Cardano-Audit-Coincashew

This script audits Cardano Node setup with Coincashew guide. 
It can be run on any non-Coincashew Cardano setup, but it will only perfom security checks.

It runs the following checks :

- Cardano-node latest version verification
- Cardano new P2P bootstrap check
- Environment Variables
- Systemd cardano-node file verification and parsing
- Cardano startup script verification and parsing
- Node operation mode (Block Producer ? Relay ?)
- Topology mode (p2p enabled)
- Topology configuration
- Keys
- SSHD hardening
- Null passwords check
- Important services running
- Firewalling rules extract
- KES expiry and rotation alert
- sysctl.conf hardening check

![Capture d’écran 2023-04-10 à 20 40 11](https://user-images.githubusercontent.com/113426048/231139235-a2969e14-1e80-4f16-936c-92b7afeb339e.png)

![Capture d’écran 2023-04-10 à 20 40 28](https://user-images.githubusercontent.com/113426048/231141468-f25c790a-a76c-4fd6-bc3a-955a5ed03f8c.png)

![Capture d’écran 2023-06-06 à 13 51 31](https://github.com/Kirael12/Cardano-Audit-Coincashew/assets/113426048/37dbad9c-4730-4cad-ba3a-47937c76e7ca)

![Capture d’écran 2023-06-06 à 13 52 22](https://github.com/Kirael12/Cardano-Audit-Coincashew/assets/113426048/07da0ad8-08e9-4780-ab8a-66898e1a4f19)


# Pre-Requisites :

Cardano Node setup with Coincashew Guide : https://www.coincashew.com/coins/overview-ada/guide-how-to-build-a-haskell-stakepool-node)
If You are not using a Coincashew setup, you can still run the script : it will perform security audit checks

# How to use

The script must be run with sudo an -E flag (to include env variables)

```shell
sudo -E ./audit-coincashew.sh
```

# Changelog

v5.0.0 (march 2024)

- Added new Cardano P2P checks for relays
- Added new Cardano P2P checks for block producer
- Added topology bootstrap check
- Several code improvements

v4.0.0

- Updated new Cardano github path

v3.0.0

- Added Cardano Node latest version verification
- Added Cardano Cli latest version verification
- Added option for non coincashew users
- Several code improvements

v2.0.1

- Minor bug correction

v2.0.0

- Improved Cardano config parsing accuracy
- Improved KES files detection and checks
- Added KES expiry calculation and alerts
- Added sysctl hardening check

v1.0.2

- KES files permission check update

v1.0.1

- Minor bug corrections

v1.0.0

Initial release

# Future improvements

- Adapt the script to run on different setups (not only coincashew)
