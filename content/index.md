# Table of Contents

<div class="toc"><ul>
  <li><a href="index.html">Introduction</a> &ndash; this page</li>
  <li><a href="a500-bom.html">The Bill of Material</a> &ndash; what you are probably here for</li>
  <li><a href="csv.html">CSV Export</a> &ndash; for Mouser Electronics</li>
  <li><a href="a500-bom.xlsx">Excel File Download</a> &ndash; for your spreadsheet application</li>
  <li><a href="https://github.com/shred/a500-bom">GitHub Project Page</a> &ndash; feel free to contribute</li>
  <li><a href="other.html">Other Bill of Materials</a> &ndash; if you liked this one</li>
</ul></div>

# Introduction

This is the Bill of Material for a replica Amiga 500+ Rev 8A. It is optimized for the [Rämixx500](https://github.com/SukkoPera/Raemixx500) Version 2 by SukkoPera.

## Read Me First!

If you want to build your own Amiga, be aware that the machine was designed in the late 1980s.

While almost all of the standard components are still available, some components are very rare by now. You will need _all_ of the listed components (except of those marked optional). We recommend that you try to get the components marked as <span class="rare">Rare</span> first, so you won't waste your money on standard components if you fail to get all the rare ones.

The original Amiga board does not require SMD soldering. The Rämixx500, and some of the replica replacements of rare parts, require SMD soldering and are not recommended for soldering novices.

**If you build a Rämixx500, make sure to read the corresponding section below. Also read the Rämixx500 documentation carefully!**

This bill of material only comprises of the components required for the mainboard itself. For a complete Amiga 500 you need:

* This **Amiga 500 mainboard**, assembled and tested.
* **Amiga 500 computer case**, original or replica.
* **Amiga 500 keyboard** with your desired keyboard layout. There are replica keycaps in different colors for Mitsumi keyboards, and there are also replica keyboards.
* **Amiga mouse** or replica.
* **Amiga 500 floppy disk drive** plus the respective wires, or a [FlashFloppy](https://github.com/keirf/flashfloppy) compatible floppy drive emulator.
* **Power supply**, a modern replica is recommended.
* An **Amiga 500 metal shield set** (with insulation sheet) is recommended, but not strictly required.

## Rare Components

The easiest way to get most of the rare components is to strip them from an old or broken Amiga 500. Some components can also still be found in retro shops, at online auction sites or on e-commerce platforms.

A few more hints:

* **CPU**: You can also use a MC68010 CPU, it is a bit faster and more compatible to WHDLoad. It is safe to use a CPU that is rated for more than 8 MHz, but your Amiga won't run faster with it. If you can only get a PLCC chip, use a PLCC to DIP adapter board.
* **Agnus 8375**: This part is very rare and expensive, but **do not use other Agnus types**, they have a different pinout and will get damaged! There is an [adapter](https://github.com/LIV2/Diet-Agnus-A500-plus) for the more common Agnus 8372, but your system is then limited to 1MB of Chip RAM of course.
* **Custom Chips**: If you can only get a PLCC chip, use a PLCC to DIP adapter board.
* **RAM**: You can use any 44256 type DRAM with a 256Kx4 organization and an access time of 120ns or faster.
* **ROM**: Either use an original one, or burn a 27C400 yourself (provided you have a license). New licensed ROMs are available from Cloanto or Hyperion Entertainment.
* **Video Hybrid**: There is a [replica board](https://github.com/SukkoPera/OpenAmigaVideoHybrid), but it requires SMD soldering.
* **RTC**: You can replace the OKI MSM6242B with an RTC72421A. If you do so, do not populate Y9, C911, and TC9 (this one is difficult to find anyway). The RTC72421A does not need to be calibrated.
* **Power Connector**: The 5-pin square DIN connector is a "Power Dynamics DS-215". It is long out of production, but maybe knowing the type will help you find it.
* **D-Sub DB-23 Connectors**: It may be surprising because the other D-Sub connectors are still available, but the DB-23 ones are really rare. Unfortunately one of them is the video output. You can skip them if you don't intend to use external floppy drives and use a RGB-to-HDMI converter.

## Capacitors

For the electrolytic capacitors, you should prefer to use polymer hybrid aluminum types with a higher voltage rating and a maximum temperature of at least 85°C, to extend their lifetime. Generally, you should get the best quality that money can buy, to avoid leaking in a couple of decades.

C324 and C334 can be bipolar capacitors to enhance audio quality.

## Battery

This Bill of Material includes a NiCd battery as buffer for the RTC. These batteries tend to leak over the years, and certainly killed a lot of classic Amiga 500s. It is advisable to use a different type of energy source, like a button cell.

**Caution:** Do not use a non-rechargeable battery without the necessary hardware modifications!

## Sockets

This list contains sockets for all chips in DIP and PLCC packages for your convenience. It is of course up to you if you want to use all of them.

On an original Amiga 500 board, only the CPU, the ROM, and the custom chips are socketed. The PLCC socket is required (you cannot solder Agnus directly to the board), but the other sockets are optional.

We generally recommend to use turned pin sockets. However, if you plan to use expansions (such as accelerators or HDMI converters) or PLCC to DIP adapters, standard sockets might be a better choice, as the pin headers might not fit into turned pin sockets.

The DRAM chips (U16~U23) require ultra low profile sockets. Otherwise the chips will collide with the keyboard.

## Rämixx500

The _Rämixx500_ board has some modifications compared to the original Commodore board. At the bottom of the parts list, you will find all additional parts that are needed for building a Rämixx500.

* **Agnus 8375**: Instead of the 390544-01 and 390544-02 types, you can also use some 318069-10 or 318069-11 types with the Rämixx500. In this case (and only then), C99 needs to be populated. **Other Agnus types still cannot be used** without an adapter.
* **Line Filter**: The Rämixx500 board provides an alternative footprint for a line filter that is still available.
* **Coin Battery**: Instead of the accumulator, the Rämixx500 provides a holder for a coin battery. Instead of R913, a diode must be placed in D913.
* **MPF102**: Instead of Q321 and Q331 in a TO-92 package, you can use MMBFJ113 in SOT23 package (Q921, Q931). Only populate one type, not both!
* **Power Connector**: The Rämixx500 board also accepts standard round DIN-6 or DIN-8 connectors. However this requires a modification to your power supply cable.
* **Sync Signal Buffer**: If you populate U94 and C94, cut the JP99H and JP99V jumpers and check that they are actually cut.
* **Floppy Switcher**: Before populating J90, cut the two marked traces and check that they are actually cut.
* **Kickstart Switcher**: Before populating J91, J92 and J93, cut the marked traces between each of the middle pins and check that they are actually cut.

Again: **Read the Rämixx500 documentation carefully!** There are a few things that need your attention. If you just blindly solder in all the components, you will damage your hardware.

## Disclaimer

This is not an official list! It was collected and reviewed by Amiga enthusiasts.

Although we strive to make the information in this project as helpful and accurate as possible, it is provided "as is" and without warranties of any kind either expressed or implied.

In other words: You might spend a lot of money, and end up with a non-functioning mainboard or a cardboard box full of useless components.

**Use at your own risk!**

## Contribute

This list is meant to be a community work. Our goal is to have a canonical list that people can rely on when ordering parts for building an own Amiga 500 mainboard.

However, this list may not be free of errors. If you have found one, please [open an issue](https://github.com/shred/a500-bom/issues), send a patch, or [send me a message](https://www.a1k.org/forum/index.php?members/6632/) at the A1K.org forum.

## License

This project is distributed under the terms of [GNU General Public License (GPLv3)](https://www.gnu.org/licenses/gpl-3.0.en.html#content).
