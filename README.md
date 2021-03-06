A simple program that scans a STL file and determines what each region's layer height should be due to it's slope.

Basic usage: "java -jar varislic3.jar -file fox.stl"
or if you want a larger max layer size: "java -jar varislic3.jar -file fox.stl -max 0.4"

The name is a combination of Slic3r and Autodesk's Varislice (Although it doesn't use Varislice's algorithm, I just thought it had a nice ring to it)

Examples:  
Here is simple dome sliced at 0.3mm
![Here is simple dome sliced at 0.3mm](http://i.imgur.com/mMl0H33.png) 
Here is the same dome sliced at 0.1mm-0.3mm
![Here is the same dome sliced at 0.1mm-0.3mm](http://i.imgur.com/gj5ricW.png)  
  

Same dome but 4x as large to exaggerate details, before varislic3
![Same dome but 4x as large to exaggerate details](http://i.imgur.com/YyvPZ2o.png)
After varislic3
![After varislic3](http://i.imgur.com/pfcBZG4.png)

The program will output a text file containing a table of the layer heights separated by tabs. There is no good way to paste data into Slic3r, so I've included an AutoHotKey script to type in the data. To use it, just place it in the same folder as 'output.txt' and run it. Click the top left cell in the table entry location in slic3r and press Ctrl-Shift-V.

Just as a note, this algorithm is not designed to produce a perfect print. It simply looks at the angles of each polygon and determins what that polygon should be printed at. It works best on organic, smooth surfaces without many pillars near each other (like a forest or a bunch of hills or buildings next to each other) and works less well on inorganic, sharp models. 



[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=79N3QP8WFXFY6)
