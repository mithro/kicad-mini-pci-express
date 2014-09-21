KiCad Mini PCI Express (mPCIe) Library
======================

KiCad Library for creating designs with Mini PCI express (mPCIe) cards.
Includes bits for both "host", a board you plug mPCIe cards into and "cards"
themselves.

Library has;
 * Schematic components.
 * PCB module footprints.
 * KiCad templates (eventually).

Currently status is;

 * PCB module for "Dual-Use Socket" which supports "full size" and "half size"
   mPCIe cards.

 * PCB module for a "full size" mPCIe cards (including board edge).
  * Includes markings for "IO connectors" region.
  * Includes "F2" keep outs marked on the bottom silk screen.

 * PCB module for a "half size" mPCIe cards (including board edege).
  * Includes "H2" keep outs marked on the bottom silk screen.

 * Schematic component for mPCIe socket.

TODO list is;

 - [ ] Create a schematic component for a mPCIe card edge.
 - [ ] Add support for "Dual Head-to-Head" sockets
   - [ ] Create a schematic component.
   - [ ] Create a PCB footprint.
 - [ ] Create a project templates for a mPCIe card;
   - [ ] Create SMBus compatible schematic for auto-detection.
   - [ ] Create an example "USB2.0" only mPCIe card.

 - [ ] Actually verify the designs with real parts.
 - [ ] Build something cool.

![PCB footprint examples](pcb-example.png)

Requirements for manufacture
-----------------------------

To get a PCB manufactured which is "mostly" compatible with mPCIe cards you'll
need;

 * 1mm PCB width.
   * Most cheap places seem to do 1.6mm by default.
 * Minimum 0.20mm (~7.87 mils) clearance.
   * 6.00 mils should be fine and supported by most places.
 * Minimum 0.60mm (~23.62 mils) trace element width.
   * Most places should support much better than this.
 * Trace to board-edge clearance 0.55mm (~21.7 mils).

## mPCIe card requirements.

When creating mPCIe cards, your manufacturer will need to satisfy the above
requirements plus a couple of extras.

 * The boards need to be routed / cut out with XXX tolerance.
 * Technically the PCB is suppose to have tapered edges on the side which is
   inserted into the socket. If you don't care about slowly destroying your
   socket then it kind of works. (IE **Don't do this with your $2000 laptop!**)


Contributing
======================

I **love** contributions. Just fork and send me a pull request! 

**If I don't respond to your pull request within a couple of days, please poke
me!**

If you make (or convert) these to Eagle, I'd be more than happy to include a
link to your repository.


Author & License
======================

This library was created by [Tim 'mithro' Ansell](https://blog.mithis.net/) as
he needed a cheap connector for [John Hedditch's](https://github.com/hedj/)
[GreenArrays based SDR RPi Hat](https://github.com/hedj/radio). **WARNING:**
This project *doesn't* use the mPCIe connector for it's intended usage, so
don't use it as an example.

This library is released under the 
[Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0.html).

If you use this library for anything, I'd love an [email](mithro@mithis.com)
with a picture of the project (of course this isn't *required* at all). People
making open source hardware make me happy!
