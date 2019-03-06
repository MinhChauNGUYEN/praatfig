# praatfig
Simple example scripts to learn to produce great figures with Praat 

Intended for training at LPP (Laboratoire de Phonétique et Phonologie), March 2019.

## Requirements
- Obviously, **Praat** is required. Find the latest version at http://www.praat.org.
- **Short audio segment(s)**: For practice, you can use the sound of this demo or you can extract an segment from your own data (exactly 0.600 sec is recommended duration for this demo script. Otherwise you need to adjust the script for more suitable scale). The electroglottalgraphic signal (EGG) can be included. 
- **Notepad++** for final cleaning EPS graphics file. 
- [**Eps viewer**](https://epsviewer.org/) for considering output figure.

## Usage
1. **Prepare input files and put them in the same folder with the script 'praatfig' (extension .PraatScript)** 

The praatfig is named **sactone.PraatScript** in this demo. 
The inputs files are depend on what you want to display in the figure. In this demo we need: (i) audio file (extension `.wav`), (ii) spectrogram (extension `.Spectrogram`), (iii) pitch (extension `.pitch`). You can also have intensity, formant, or pulse. The way to prepare these inputs is that: 
- (On window *Object Praat*) open sound file > select `view and edit`
- (On toolbar of the new window for view and edit) select object which you want to display, for instance here we select `Spectrum`/ `Extract visible spectrogram`. 
- (On window *Object Praat*) an new file is created named **Spectrogram untitled**, you need to save this file by selecting `Save`/ `Save as text file...`. 
- You can extract other objects by the same process. 

2. **Update input information in available script, adjust the script until you satify with the figure.**
When using the script for many sound files, we should make a copy of the `.PraatScript` file and change the information of **Loading the data** in command `Read from file...` and **exporting the output file** in command `Save as EPS file...`. Other modification is also possible if it's necessary.

3. **Clean up the EPS graphic figure by Notepad++**
- Open the output file in **Notepad++**, 
- Find the **text** (legends) or **chiffre** (axes's points) that need to be modified or deleted (shortcut: `Ctrl + F`)
- Make manual changes.
- At the same time you need to consider the figure by EPS viewer to make sure your changes are correct. 

For example, in this demo, there are four places hane been modified: round time to 0.6 sec (not 0.6007); and remove three chiffres '0.1917', '-0.1801', '0' (on vertical axes of acoustic signal).

## Behind the script 
### You can understand and write the scripts yourself.
The script is actually a record of all the actions that you can do on **Praat Objects** and **Praat Picture**. In other words, without a script you are still be able to make a figure by using functions on those two windows of Praat. 
So, *why we need script?* The answer is that it's much easier and faster to produce many figures with the same scales (mass production). Therefore, after the first figure by manual produce, you can store all the actions as a script using `Paste history`.

### A rule-of-thumb order for plotting an object on **Praat Picture**
- Choosing the position (There are two choices: `Select outer viewport` or `Select inner viewport`) 
- Drawing the objects with details: spectrogram/ audio sound/ pitch/ formants, etc
- Setting axes and legends
- Save the file as `.eps`/ `.pdf`/ `.png`

### Some notes
1. Outer viewport vs Inner viewport 
Both of them are the ways to determine where your next drawing will occur by selecting the part of the Picture window. While the outer viewport includes the margins, the inner viewport does not. It's corresponding to the action you select the viewport by dragging your mouse arcoss the window **Praat Picture**. Althoght they can be used interchargeable, `Select inner viewport` offer an easier view for drawing the main objects such as *spectrogram, audio,* etc; whereas `Select outer viewport` is easer for setting information surround (including axes and legends), or choosing the entire figure for saving. 

2. With vs without box or axes 
 When drawing any object, there is an option is **Garnish**. If you select this option (correspoding to `"yes"` on the script), the box or the axis and the legends with will be created automatically which is good for drawing one single object. When you would like to combine two or more than two objects (spectrogram + audio + pitch, for instance), it will be better to draw without **Garnish**, then later we can use command `Draw inner box` to make the box and set the axes and legends exaclty where and what we want. This way is cleanser and no conflict between objects.
 
3. Save as `.eps` is highly recommended 
> An EPS file is a graphics file saved in the Encapsulated PostScript (EPS) file format. It may contain 2D vector graphics, bitmap images, and text. 
After saving the output figure with `.eps` format, we can easily clean up the figure by **Notepad++**. For instance, modify the legends, delete unnecessary index of automatic axes, etc.

## Futher references
1. For futher information of **Praat Picture** and so on, visit: http://www.fon.hum.uva.nl/praat/manual/Picture_window.html
2. Thanks to the [CREM archive](https://archives.crem-cnrs.fr/archives/items/CNRSMH_I_1900_001_004/) for allowing use of the 1900 recordings of Vietnamese.
