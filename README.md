# Amiga 500 Bill of Material

This project contains the Bill of Material for building an own **Amiga 500+ Rev. 8A** mainboard. It is optimized for the [Rämixx500](https://github.com/SukkoPera/Raemixx500) Version 2 by SukkoPera.

<div style="text-align:center;font-size:130%;font-weight:bold">
<a href="https://shred.github.io/a500-bom/">Read the Bill of Material here!</a>
</div>

## Contribute

This list is meant to be a community work. Our goal is to have a canonical list that people can rely on when ordering parts for building an own Amiga 500+ mainboard.

However, this list may not be free of errors. If you have found one, please [open an issue](https://github.com/shred/a500-bom/issues), send a patch, or [send me a message](https://www.a1k.org/forum/index.php?members/6632/) at the A1K.org forum.

## Technical Background

The main file of this project is the `a500-bom.yml` file. It contains the bill of material as YAML file, so it can be easily diffed by git and read by programs.

A Python tool called `generate.py` generates the website. You can find the generated web site in the `docs` directory. The converter needs these Python packages installed on your system:

* [PyYAML](https://pypi.org/project/PyYAML/)
* [Jinja2](https://pypi.org/project/Jinja2/)
* [jinja-markdown](https://pypi.org/project/jinja-markdown/)
* [XlsxWriter](https://pypi.org/project/XlsxWriter/)

## Sources

The following sources have been used:

* Amiga 500 Rev 8A Schematics
* SukkoPera: [Rämixx500](https://github.com/SukkoPera/Raemixx500)
* [Amiga PCB Explorer](https://www.amigapcb.org/)
* [Part list](https://github.com/SukkoPera/Raemixx500/issues/22) by BrandonQuest

## Disclaimer

This is not an official list! It was collected and reviewed by Amiga enthusiasts.

Although we strive to make the information in this project as helpful and accurate as possible, it is provided "as is" and without warranties of any kind either expressed or implied. **Use it at your own risk!**

## Kudos

I would like to thank these people from the [www.A1K.org Amiga Board](https://www.a1k.org) for their help: psydown.

## License

This project is distributed under the terms of [GNU General Public License (GPLv3)](https://www.gnu.org/licenses/gpl-3.0.en.html#content).
