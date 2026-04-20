MultiStack — MultiBuild (Formerly known as MultiBoard) Tile Stacker

A free, browser-based tool for stacking MultiBoard tiles into a single print job. Upload your tile STL, choose how many high, and get a ready-to-slice BambuStudio project file back in seconds.

**[Open the tool](https://mrj0ne5cths.github.io/multistack)**

---

The problem it solves

[MultiBoard](https://www.multiboard.io/) is a modular 3D-printed wall organization system. If you need 6 of the same tile, you'd normally print them one at a time — or manually duplicate and arrange them in your slicer. MultiStack automates the stacking: it places N copies of your tile directly on top of each other with a small separation gap, so they all print in one job and pull apart cleanly when done.

---

Workflow

1. Download your MultiBoard tile STL from [multiboard.io](https://www.multiboard.io/)
2. Open MultiStack in your browser
3. Upload the STL
4. Choose how many tiles high (2–20)
5. Adjust the inter-tile gap if needed to match single layer height (default 0.20mm)
6. Download the `.3mf` project file
7. Open in BambuStudio → slice → send to printer

Nothing is uploaded to any server.** The entire tool runs locally in your browser.

---

How it works

MultiStack reads your STL geometry directly in the browser and builds a BambuStudio-compatible `.3mf` project file containing one mesh and N placed instances — each stepped up by the tile height plus your chosen gap. When you open it in BambuStudio you'll see all the tiles stacked vertically, ready to slice as a single print.

The separation gap causes the printer to deposit a single layer of "air" between each tile, just enough for them to be pulled apart by hand (or the help of a flat tool) when the print is done.

---

Requirements

- **Slicer:** BambuStudio (May work in others, but this is where I've confirmed it)
- **Printer:** Bambu Lab printers (X1C, P1S, P1P, A1, etc.)
- **Browser:** Chrome or Firefox
- **Input:** Any stackable MultiBoard tile `.stl`

---

Tips

- Check the 3D preview in BambuStudio before slicing, all tiles should appear stacked vertically on the plate
- The default 0.20mm gap works well for most tiles. Increase it if tiles are fusing together, decrease if they're separating too easily
- Tall tiles stacked many high can exceed your printer's Z limit, check before printing

---

About MultiBuild 

MultiBuild (Formerly known as MultiBoard) is designed by [Jonathan Odom](https://www.multiboard.io/). MultiStack is an unofficial community utility and is not affiliated with or endorsed by the MultiBuild project. If you're able, please support Jonathan's efforts as he has designed something really incredible with this project.

---

License

MIT — free to use, fork, and share.
