## Intro

This guide expects you to be a bit familiar with [Cheat Engine](https://github.com/cheat-engine/cheat-engine), at least to the extent that you know how to look for values. If you are new to this whole concept check out this video: [Ultimate Cheat Engine Beginner Tutorial Part 1 | GH102](https://www.youtube.com/watch?v=_THZIUELKrw)

## The Basics

Most values in the game are stored as `4 Byte Big Endians`, this is not enabled in Cheat Engine by default so go to  `Settings > Extra Custom Types` and enable it there.

You also need to enable `Settings > Scan Settings > MEM_MAPPED`.

To speed up your searches you can set up `300000000` - `341FFFFFF` as start and endpoints for the scans.

Common things and their types

- Money `4 Byte Big Endian`
- Bank `4 Byte Big Endian`
- RP `4 Byte Big Endian`
- Snacks `4 Byte Big Endian`
- Vehicles `4 Byte Big Endian + HEX`

## Money

Money and Bank are the easiest to change. Just look up the value, withdraw/deposit until you can narrow it down to 2 Addresses. One of the addresses will be the real address that let's you change your money, other one is a dud.

## RP

RP is a bit more tricky to change. You can only increase your RP, to do that you can use these activities: `Gang Attack Kills`, `Losing a Wanted Level`, `Robbing a Store`, `Completing a Stunt Jump`, `Delivering a Simeon Car`, `Any Job`.

You can see your current RP by pressing `D-Pad Down`. You should see `0/500` when you first start out. The value you are interested in is on the left side of the slash.

You keep doing scan until you get <20 addresses. From there you have to figure out which one is the real one, all others are duds.

A good way to find the real Address is to select half of the Addresses, change it to a different value. If it reverts back instantly then none of the selected ones is the real one. You can delete them all. If the RP stays then delete the other half. Repeat until you have a single Address.

If you would like to get a specific rank here's a [List of RP for each Level](rp.txt)

After you have modified your RP you need to make it stick, you can do that by doing any of the mentioned activities above. If you don't do it the next time you die you'll revert back to your original level.

## Vehicles (Credit to [@Tervel1337](https://twitter.com/Tervel1337))

You are able to get [almost any vehicle](https://twitter.com/Tervel1337/status/1652247298833805312) into your garage via this method. Emergency, Military are Blacklisted, meaning you can't store them, but you can get a [lot of interesting vehicles](https://twitter.com/RealLaszloR1/status/1652656901920784385) in there.

Here's a [List of Vehicle Hashes](https://gist.github.com/QuynhVir/f2f28fcc921d4f207280534f9326d7cf), you will use the `NAME` and `HEX` rows from here.

Even if you do all of the following steps correctly you might still crash. Tread lightly, do not be discouraged, just restart your game and try again. 

- Get a vehicle off of the street (anything that isn't too High-End for LSC)
- Go into LSC, select `Loss/Theft Prevention`
- Look up your Vehicle in the Hash List and copy it's Hex
- Tick the Hex checkbox in Cheat Engine and scan for your Value
- Take all the Addresses and put them in your table
- Find the Hex of the Vehicle you would like to get
- Update all of the Addresses with the new Vehicle's Hex
- Buy Tracker and Full Coverage
- Change back all of the values to the original vehicle's Value
- Leave LSC
- Switch sessions

If you have done everything correctly you should be in your new vehicle. If you are in the old one get a different car and repeat the steps above.

Some vehicles will say they cannot be stored after you have done this. In that case buy random car, leave your car behind, call the Mechanic and get your random car delivered, drive home. If your Vehicle isn't in the garage then the game was right, it is blacklisted, but most of the time it will be in there. Provided you didn't try to get one of the Blacklisted vehicles mentioned above.

## Snacks

You can also change the amount of Snacks you have. Just keep eating/buying them until you can narrow it down to 2 Addresses. One of them is a dud as usual.

## Extra

In my experience Addresses will be reused. I have saved all of the different Money and RP Addresses I have encountered through numerous sessions. I came across 2 Money and 3 RP Addresses where one would always be valid. You might just get away with saving these Addresses instead of trying to figure out all the pointer stuff.

## Credits
- [@Tervel1337](https://twitter.com/Tervel1337) for figuring out you can get cars the same way as on PC
- [@DakrFH](https://www.youtube.com/@DakrFH) for helping with this guide in general