# (DRAFT) [JLCPCB][1] SMT Assembly service - Raspberry Pico RP2040 KiCAD Design

In this article, we will explore how to get a KiCAD design fabricated and assembled by [JLCPCB][1] SMT Assembly service.
We'll use [RPi Pico Debugger Shoe][2]as a starting template.


## Prerequisites

* [KiCAD 6][3]
* [KiCAD JLCPCB tools][4]

If you're reading this article, you'll probably have KiCAD installed on your computer.
But if not, download and install [KiCAD 6][3] from the official website.

> The following contents of this article is tested with KiCAD version 6. Older versions or Nighty builds are not tested.

There are several plugins to export JLCPCB compitible fabrication files (Geber, BOM, CPL).
As we can see in the table, [KiCAD JLCPCB tools][4] has the best reputation and community support (at this time of writing).

GIthub Repository | Author | Star | Fork | Contributors | Last Updated
------------------|--------|------|------|--------------|-------------
[KiCAD JLCPCB tools](https://github.com/Bouni/kicad-jlcpcb-tools) | Bouni bouni@owee.de | 244 | 28 | 10 | Feb 2022
[KiCad JLCPCB BOM Plugin](https://github.com/wokwi/kicad-jlcpcb-bom-plugin) | Wokwi <https://wokwi.com/> | 110 | 25 | 3 | 2021
[KiJLC](https://github.com/fullyautomated/KiJLC) | Fully Automated <https://fully.automated.ee/> | 12 | 8 | 2 | 2021
[KiCad BOM CPL Plugin](https://github.com/prrvchr/KiCad-BOM-CPL-Plugin) | prrvchr prrvchr@gmail.com | 3 | 2 | 1 | 2020

Install [KiCAD JLCPCB tools][4] on KiCAD as described in the doc.
* open KiCAD
* go to menu **Tools** > **Plugin and Content Manager**
* in the Plugin and Content Manager dialog, click **Manage** button
* in the opened Manage Repositories dialog, click **+** button
* copy and paste the following repository metadata URL `https://raw.githubusercontent.com/Bouni/bouni-kicad-repository/main/repository.json`
* click **Save** button
* click the dropdown named **KiCad official repository** and select **Bouni's KiCad repository**
* click **Install** button of **KiCAD JLCPCB tools** item on the left panel
* close the Plugin and Content Manager dialog

If installation worked, you could see a blue JLCPCB tools icon on the toolbar of PCB Editor.

## Design the PCB with RP2040

> _Immature poets imitate: mature poets steal._ by T.S. Eliot

Just like graphics designers start from templates and software developers start from boilerplates, hardware designers can also start from a template or existing designs.
There are already plethora of resources we can use, including [the ofiicial Raspberry Pico design][5].
To help you to choose the right startpoint, the following table summarizes some open-source hardware designs at the time of this writing.

Project/Board Name | Author | Resource | Designed with| Note
-------------------|--------|------------|--------------|-----
Raspberry Pico | Raspberry Pi Foundation | [Design File][5] | Allegro | The official hardware design of Raspberr Pico
Pro Micro RP2040 | SparkFun Electronics | [GitHub][6] | Eagle | Arduino Pro Micro footprint
Thing Plus RP2040 | SparkFun Electronics | [GitHub][7] | Eagle | Feather footprint
ItsyBitsy RP2040 | Adafruit Industries | [GitHub][8] | Eagle | ItsyBitsy footprint
RPi Pico Debugger Shoe | Shawn Hymel | [GitHub][9] | KiCAD | Raspberry Pico footprint



---

[1]: https://jlcpcb.com/HOT "JLCPCB Official Website"
[2]: https://github.com/ShawnHymel/rpi-pico-debugger-shoe "RPi Pico Debugger Shoe by Shawn Hymel"
[3]: https://www.kicad.org/download/ "KiCAD Official Download Page"
[4]: https://github.com/Bouni/kicad-jlcpcb-tools "KiCAD JLCPCB Tools plugin by Bouni"
[5]: https://datasheets.raspberrypi.com/pico/RPi-Pico-R3-PUBLIC-20200119.zip "Raspberry Pico Design File"
[6]: https://github.com/sparkfun/SparkFun_Pro_Micro-RP2040 "SparkFun Pro Micro RP2040"
[7]: https://github.com/sparkfun/SparkFun_Thing_Plus-RP2040 "SparkFun Thing Plus RP2040"
[8]: https://github.com/adafruit/Adafruit-ItsyBitsy-RP2040-PCB "Adafruit ItsyBitsy RP2040 PCB"
[9]: https://github.com/ShawnHymel/rpi-pico-debugger-shoe "RPi Pico Debugger Shoe"
