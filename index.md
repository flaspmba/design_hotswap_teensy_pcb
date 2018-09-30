# WORK IN PROGRESS

## Table of Contents
1. [The Layout](#the_layout)
2. [The Matrix](#the_matrix)
3. [The Schematic](#the_schematic)

### The Layout <a name="the_layout"></a>
I used [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/) to design layout for my keyboard.

![keyboard_layout](/images/keyboard_layout_example.png)

There are three reasons why I'm using this strange, pretty ugly layout:
1. The (mostly) ortholinear layout simplifies [the matrix](https://docs.qmk.fm/#/hand_wire) physically on the PCB, making it easier to follow the traces.
2. Using all the standard keys becomes an excuse for me to build my hotswap [footprint library in KiCad.](https://learn.sparkfun.com/tutorials/beginners-guide-to-kicad/creating-a-custom-kicad-footprint-library)
3. I can cover an ortholinear board with a regular 60% keycap set.

After finishing my layout, I copied the JSON:
```json
[{x:1.25},"~\n`","!\n1","@\n2","#\n3","$\n4","%\n5","^\n6","&\n7","*\n8","(\n9",")\n0","_\n-","+\n=",{w:2},"Backspace"],
[{x:0.75,w:1.5},"Tab","Q","W","E","R","T","Y","U","I","O","P","{\n[","}\n]",{w:1.5},"|\n\\"],
[{x:0.5,w:1.75},"Caps Lock","A","S","D","F","G","H","J","K","L",":\n;","\"\n'",{w:2.25},"Enter"],
[{w:2.25},"Shift","Z","X","C","V","B","N","M","<\n,",">\n.","?\n/",{w:2.75},"Shift"],
[{x:1.75,w:1.25},"Win",{w:1.25},"Alt",{a:7,w:6.25},"",{a:4,w:1.25},"Alt",{w:1.25},"Win"]
```
### The Matrix <a name="the_matrix"></a>
Pasting the JSON I copied above, I used [KBfirmware](https://kbfirmware.com/) to create a matrix for me. I'll use this matrix to create the wiring schematic in KiCad.

![kbfirmware_JSON](/images/kbfirmware_paste_JSON.png)

![wiring_matrix](/images/matrix_wiring_example.png)

I need to determine if the sum of columns and rows of my matrix will fit the maximum number of pinouts for the Teensy2.0.
- If it doesn't, then I would have to get creative with my matrix. I have to remember that the matrix is a virtual representation of the keys that doesn't care how they are physically laid out. I typically just create the matrix in [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/) with 1u keys, just to import to [KBfirmware](https://kbfirmware.com/) to layout a matrix for me.
- Thankfully, (15) columns + (5) rows = (20) pinouts, which fits a Teensy2.0, since I'm not planning on anything fancy like LEDs.

I'll be sure to take a screenshot of the matrix so that I have it handy for the schematic portion of KiCad. I'll be back on [KBfirmware](https://kbfirmware.com/) when I'm ready to create the firmware.

### The Schematic <a name="the_schematic"></a>
From this point forward, I basically follow [/u/ruiqimao's Keyboard PCB Guide,](https://github.com/ruiqimao/keyboard-pcb-guide) but with some tweaks to fit my design. The approach I'm taking is essentially taking what I would do if I handwired this board and making it into a PCB.

1. First, I follow the guide's recommendation to download Hasu's component library.


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
