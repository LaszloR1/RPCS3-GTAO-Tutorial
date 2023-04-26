# RPCS3 GTAO Tutorial

## The Basics

Download & Install [RPCS3](https://rpcs3.net/download)

Download the OS From [Sony's Website](https://www.playstation.com/en-us/support/hardware/ps3/system-software/)

Download [pkg2zip](https://github.com/mmozeiko/pkg2zip/releases)

Download [Nopaystation](https://nopaystation.com/)
- Download [PS3 Games TSV](https://nopaystation.com/tsv/PS3_GAMES.tsv)
- Download [PS3 DLCs TSV](https://nopaystation.com/tsv/PS3_DLCS.tsv)

## Start the NPS Browser

On the first time setup you will be required to locate pkg2zip and the .tsv files you have downloaded.

Download the following files
- game: `NPUB31154`
- dlc: `BLUS31156` (Optional, but recommended collectors edition extras)

## Install the Game

Start RPCS3 and click `Files > Install Packages/Raps/Edats`
- Install game .pkg
- Install game .rap
- Install dlc .pkg
- Install dlc .rap

## Patch It

Download [rusty-psn](https://github.com/RainbowCookie32/rusty-psn)

- Launch it
- Look up updates with the game's serial number `NPUB31154`
- Download the update(s) (`1.06` recommended, pseudo-online works until `1.12`, **if you want `1.12` you need to download all previous patches as well**)
- Select the downloaded patch(es) in File Explorer and drag it into RPCS3
- Your game version should be `1.06` now

## Un-Patch It
If you installed an update, but you want to go back to 1.0 follow these steps: 
- Right click on the game entry and select Open Install Folder
- Delete the folder
- Hit refresh

## Custom Config (Credit to [@Dark FH](https://www.youtube.com/@DakrFH))

Create custom config for GTA 5 (right click on the game) with the following settings. This is not mandatory, but it improves performance and stability. 
- `GPU > Additional Settings > Write Color Buffers: On`
- `Network > Network Configuration > Network Status: Connected`
- `Network > Network Configuration > Enable UPNP: On`
- `Network > PSN Configuration > PSN Status: RCPN`
- `Advanced > Core > Accurate RSX reservation access: On`
- `Advanced > GPU > Write Depth Buffers: On`
- `Advanced > RSX FIFO Accuracy: Atomic`

##  RCPN Setup

These steps are required to be able to play with others

- `Conifguration > RCPN > Account > Create Account` (do what it says)
- Once done click Test Account it should say: `Your account is valid!`
- If invalid repeat the step 1 again

## Enjoy

Start the game, complete `Prologue` and `Franklin and Lamar` and you should be able to play online. **Characters are temporary** so don't get your hopes up too much.

## Cheating

Since characters are temporary its only fair we cheat a little bit. Money and RP are stored as `4 Byte Big Endians`. If you are using Cheat Engine this type has to be enabled inside `Settings > Extra Custom Types`. You can also set up `300000000 - 380000000` as start and endpoints for the scans.

## Credits
- [@Tervel1337](https://twitter.com/Tervel1337) for discovering this whole rabbit-hole
- [@Dakr FH](https://www.youtube.com/@DakrFH) for the configs