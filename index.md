## Table of Contents
1. [Creating the Layout](#creating_the_layout)
2. [Creating the Matrix](#creating_the_matrix)

### Creating the Layout <a name="creating_the_layout"></a>
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
### Creating the Matrix <a name="creating_the_matrix"></a>
I used [KBfirmware] to create a matrix for me.

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

