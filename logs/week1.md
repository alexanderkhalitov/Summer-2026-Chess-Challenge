# Weekly Devlogs: Week 1 (Setup)
As part of the chess challenge, we're to complete weekly devlogs on progress made during the week. No code is written yet, so this week is dedicated to the setup of the tools that I'll use for development and testing of my software.

There are a great deal of assemblers for the 6502/6510/C64, with decades of development and pedigree behind them. Bumbershoot software made a great [comparison of a few prominent options](https://bumbershootsoft.wordpress.com/2016/01/31/a-tour-of-6502-cross-assemblers/) and the takeaway is that there isn't a best or worst option. Assembly isn't a language with a defined specification, however, and so all the extensions and features that assemblers add tend to produce mutually-incompatible syntax. I chose [64tass](https://tass64.sourceforge.net/) because I own an actual Commodore 64, and the idea of being able to write the same assembly code on my modern computer and on the real hardware is very appealing. 64tass can be built from source from the Sourceforge project, but pre-built binaries are available for a variety of environments. I'm running Debian, so I can install 64tass like so:

`sudo apt-get install 64tass`

I also took the liberty of installing a VSCode extension of 64tass syntax highlighting.


We'll also need an emulator to test our written software. [VICE](https://vice-emu.sourceforge.io/index.html) is the gold standard. There are a few little snags with VICE, however - because the C64 ROMs are not libre, the emulator is distributed without them. On Debian, VICE can be installed through an apt package as well:

`sudo apt-get install vice`

However, because of the dependence on non-free ROMs, VICE is packaged in the `contrib` branch, which must be enabled. See [here](https://gist.github.com/ChristopherA/680b4eeeeb6e9e4c7fc59c010a23b6cd) for more info.

As for where to get the Kernal *[sic]* and BASIC ROMs, I'm going to back them up from my real hardware. I am not suggesting or condoning piracy of these ROMs, but I am going to make the observation that they are probably freely available for download with a little searching. I can also help with the process of legal acquisition of these ROMs.

With my development software set up, next week I'll start actually writing code.
