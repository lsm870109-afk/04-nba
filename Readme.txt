
  .--. .--    . .  .     OEdit
  |  | |__  __|   -|-    Version 0.2a (Public Beta)
  |  | |   |  | |  |     February 28, 2004
  `--' `-- `--' '  `-'   Programmed by Arushan

     Website: http://oedit.nd4spdworld.com/

  __________________
_| Welcome To OEdit |_____________________________________________

 OEdit is a program that opens and lets you move vertices of
 some .o and .ord/.orl files which contain model data. These .o
 and .ord/.orl files are found in some of Electronic Art's newer
 games which use the EAGL library.

 [Version 0.2a]

 Although it has been exactly a year since the last release of 
 OEdit, this update is only a minor one. For a list of changes,
 see the "What's New" section below.

 Uninstall previous version or overwrite over version 0.2.
 Don't overwrite over version 0.1.x.
 
 [Version 0.2]

 UNINSTALL ANY OLDER VERSIONS OF OEDIT BEFORE INSTALLING THIS ONE!
 (Control Panel -> Add/Remove Programs)

 This version is a major update. Lots of things were remade, and
 the entire program was totally changed. You cant use it in the same
 way as the old version. For the complete list of changes, scroll 
 down to the "What's New" section and read it carefully.

 There is no external help file with this version. I'm hoping some 
 people can find the time to write tutorials for it. The only help
 for using OEdit I can give is down in the "Using OEdit" section 
 of this readme file.

 A 3D Accelerator card is essential to use this program. If you get
 errors about Direct3D when running OEdit, edit the shortcut for 
 OEdit and add /rgbemulation at the end of the command.

 A big thanks to a few people:
   Addict (http://www.addictarts.com)
   Fede Debla
   FerryvD
   Jeroen Bruurs (http://www.nd4spdworld.com)
   Jille Berends (aka Chillout)
   Oleg M. (http://www.zmodeler.com)
   TheFallen
 ... and Electronic Arts.


 Can't get something to work? Try asking in the forums at
 http://discussion.nd4spdworld.com.

 You will more likely get a quicker reply by asking in the forums
 than emailing me.

  ______________
_| Requirements |_________________________________________________

 - VB6 Runtimes
      - You most likely have them already. If the program does
        not run or gives an error message about MSVBVM60.DLL, 
	download this from Microsoft's website and install it:
	http://www.microsoft.com/downloads/release.asp?releaseid=28337
 - Programs to extract .o files from .viv and .big files.
      - VIVEdit from http://www.addictarts.com
      - bigGUI -- this program is still in beta but opens most
         of the .viv and .big files and supports compression/
         decompression -- a link to download the beta was posted
         at http://www.fifa-city.de/showthread.php?threadid=6195
 - Program to convert .fsh files to .bmp (needed for UV mapping)
      - FSHTOOL http://www.math.polytechnique.fr/cmat/auroux/nfs/
         or http://auroux.free.fr/nfs/
 - DirectX 7.0 or newer

  ____________
_| What's New |___________________________________________________

 [Version 0.2a]

   - Fixed the Direct3D bugs. Now, you don't need /rgbemulation,
     and you can use a HAL or TnL device if your 3D card supports
     it. There is also a small shortcut to let you choose your
     3D Device.

   - Vertex Properties (View->Vertex Properties, or CTRL+P). This
     property dialog replaces the original "Coordinate" section.
     It allows you to set more values than before such as normals
     and vertex colors. Not all files or parts may support all the
     properties. Editing may be slower with the window open, so
     close it if you don't need it.

   - CHANGES IN VIEW ORIENTATION: In the previous version 0.2, the
     X axis was inverted to make life easier for NFS editors. Since
     NFS editors don't use OEdit anymore, the X axis is now non-
     inverted. It doesn't make much of a difference, i.e., all
     your exisiting files will work. However just remember that
     X in the old version is now -X.

   - Registry hacks for Face editors (FIFA). There is a file called
     "FaceEditing.reg" in the OEdit installation folder. Double
     click on it and say Yes. It will make the following changes:
         1. The field of view (FOV) will be made larger, so your
            faces won't look distorted when zoomed in.
         2. It will make the lighting Directional instead of Spot,
            so that zooming in/out will not affect how the face
            looks due to the lighting.
         3. It will invert the Z axis of the perspective view, so
            that moving a vertex in the editing view will move it 
            in the same direction in the perspective view.

   - Improved Error Handling. Most technical errors will not cause 
     OEdit to exit. You can acknowledge the error and continue 
     working.

   - There is an Import menu in the File menu. It has one entry
     -- "Rhino Points File". It may or may not work properly for 
     you. It DOES NOT work for me with a file that is edited
     using Rhino. Maybe you will have better luck.

 [Version 0.2]

   About 90% of OEdit was rewritten. It completely uses DirectX
   for all graphics, so you can expect to see some improvement
   for small to medium sized models but however, it might appear
   to be slower for large models. A Direct3D preview replaces the
   old wireframe view and it updates as you change the model.
   Vertices are no longer moved using the keyboard -- it's all 
   done using the mouse now (support for moving with the keyboard 
   was removed).

   List of additions/subtractions/changes:
   - Totally new .o loading/saving routines. As a result .ord/.orl 
     files CANNOT be directly opened with this version.
   - New tool based editing
       - C n' M (Click and Move)
       - Select
       - Move
       - Scale
       - Rotate
       - Auto (Automatic Tool Selector)
   - Undo support -- only supports one step though.
   - Export support - Currently supported formats are 
         Milkshape 3D ASCII
         Rhino Points File
         VRML File
   - A new selection mode called "Dont Preserve Selection" 
     enables you to select items without keeping the existing 
     selection -- like in most other modelling programs.
   - Multiple texture support. You can load different textures
     and apply them to diffferent parts.
   - Support for loading skeleton.o files from NFSHP2 to change
     rotation centers of wheels, position of lights and the 
     driver. It can also load skeleton data for other models, but
     only if the models and the skeleton are in seperate files.
   - The textured preview mode was replaced with the new Direct3D 
     Perspective view which is in place of the old wireframe view.
   - Has support for multiple languages.
   - A few other misc. things.

  __________________________
_| Notes on Specific Models |_____________________________________

 [Version 0.2]

 .ORD/.ORL FILES
   They cant be directly opened with this version. You need to 
   convert the files to a .O file before it can be opened. See
   the website for a converter.
 
 HIGH POLY MODELS
   OEdit might be slow with very high poly models such as NFS6 
   tracks. If it is slow, try to hide the parts that you dont need
   for modelling to improve the speed. Using the full view mode 
   might also improve speeds. 

 FIFA FACE MODELS
   Dont zoom in too much with the Perspective view, or else the
   face will look distorted like with the Textured Preview in
   the old version.

 SKELETON.O FILES
   These can be loaded through the file menu. You can only load
   one skeleton.o file. Once it is loaded, you need to load a new
   model (or the same model again) to open a new skeleton.o file.
   Skeleton.o files (in NFSHP2) contain data on the position of
   wheels, lights and the driver. If you are moving the wheels, 
   the Y and Z component of the bone must be exactly same for both 
   left and right wheels.

  _____________
_| Using OEdit |__________________________________________________

 [Version 0.2]

 If you have used an older version of OEdit, this newer version 
 might take some practice getting used to. This should help with
 most of the underlying, or hidden things in the program. Simple
 and obvious items such as loading/saving, hiding/showing parts, 
 etc. are not discussed here.

 Make sure you only show the parts that you need for editing. 
 Showing unwanted parts will make OEdit work slower as it has
 to process more data.
 
 First of all, you don't use the keyboard to move vertices 
 anymore, it might be a loss of precision, but it's faster and 
 less time consuming doing it with the mouse.

 The Tools (Action):
   C n' M -- Click and Move (Shortcut key: 1)
     Simple and fast clicking and moving of vertices. It will
     select all vertices that you hover over (and change color).
     Just drag and drop with the mouse to move the vertices.
     Any existing selection will be lost!
   
   Select (Shortcut key: 2)
     Selection tool. Select will enable selection by left-clicking 
     on vertices or by left-clicking and dragging to create a 
     selection rectangle. All the vertices that fall inside the 
     selection rectangle will be selected.

     To deselect vertices, hold down the shift key and perform the
     selection procedure.

     If [Options -> Don't Preserve Selection] is checked, the 
     exisiting selection will be discarded when you make a new 
     selection.

     The Selection Range slider will let you choose the distance
     within which you want to select. This does not affect anything
     when selecting by using a selection rectangle.
   
   Move (Shortcut key: 3)
     Left click and drag to move the selected vertices.
   
   Scale (Shortcut key: 4)
     Left click and drag to scale the selected vertices. Move in 
     the positive vertical or horizontal direction to scale it 
     larger and the negative directions to scale it smaller.

     The scale tool will scale using the geometric center of the 
     selection as the local axis for scaling. To scale using the
     global axis, hold down the SHIFT key.

   Rotate (Shortcut key: 5)
     Left click and drag to rotate the selected vertices. Move in 
     the positive vertical direction to rotate it counter-clockwise
     (CCW) and in the negative vertical direction to rotate it 
     clockwise (CW).

     The rotate tool, like the scale tool will rotate using the 
     geometric center of the selection as the local axis for 
     rotation. To rotate using the global axis, hold down the SHIFT 
     key.
   
   Auto (Shortcut key: 0)
     This is an important tool that can save a lot of time that you
     spend in changing tools. It is usually helpful to use this tool
     with [Options -> Don't Preserve Selection] checked. The Auto
     tool will automatically select a tool for use depending on
     certain conditions:

     If you are not hovering over any vertices
       -> Select Tool (use the selection rectangle)
     If you are hovering over any vertices and...
       If no vertices are currently selected
         -> C n' M Tool
       but if vertices are selected and the Rotate Tool or Scale 
       Tool are not selected
         -> Move Tool

 Direction Options (Shortcut key: ~)
   Direction options are modifiers that work on a few tools,
   specificially the Move tool and the Scale tool. Turning off
   a direction will prevent the vertices being moved in that
   direction.

   The direction tool is also used in the Flip Vertices tool
   (see Other Tools below).

 Other Tools 
   Recalculate Normals
     At times, the model may not contain data which describe how
     light bounces off the object (normals). If this is the case, 
     the Perspective view will show the model as a dull gray color.

     The Recalculate Normals tool will remake the normal data to
     show the model properly. When using this tool, you will be
     asked if you want to use a reverse order for normal 
     calculation. Click on No. If the model doesn't look proper 
     after doing so, use the tool again, and answer Yes this time.

     WARNING: Do not use this if the model looks proper or has 
     normal data as the new data will be saved when the file
     is saved.
   
   Flip Vertices
     This tool will transform the object by flipping the vertices
     by the global axis. Use the Direction Options modifiers to
     select in which way you want to flip the object. Then choose
     a view and select the vertices you want to flip. Then use the
     tool. A view must be active for this tool to work properly
     (the name of the view will be in Red color).

     The Flip Vertices tool doesn't work with the UV Map Editor.
   
   Move to Origin
     This tool is an alternative to entering 0,0,0 in the vertex
     coordinate section. Select the vertices you want to to move to
     the origin and use this tool.
 
 Zooming In and Out
   You should zoom in and out to get a good look at the model and
   know what exactly it is that you are editing.

   For the regular Front, Side, Top views:
     To Zoom In, hold down the ALT key and left click on a view or 
     press CTRL+W. To Zoom Out, hold down the ALT key and right 
     click or press CTRL+Q. The zoom can be reset by selecting a 
     view and pressing ALT+HOME.
   
   For the Perspective view:
     Right click and drag up and down zoom out and zoom in.

 Panning the view (Move the view area)
   When you zoom in some areas will not become visible. When this 
   happens, you can move the view around to another location.

   For all views:
     Hold down the CTRL key and left click and drag. Think of the 
     view as a sheet of paper and the mouse cursor as your hand. It 
     can be reset by selecting a view and pressing CTRL+HOME (does 
     not apply to Perspective view).
 
 Rotating (for the Perspective view)
   Left click and drag to rotate the object. If you want to only 
   rotate in a specific direction, choose the direction using the 
   Direction Option modifiers and hold down the ALT key when 
   rotating.

 The Full View
   If you do not need all the views to see what you are modelling 
   it's a good idea to select the view you want to model using and 
   press CTRL+F or [View -> Full View]. When in the Full View mode, 
   things are generally faster than the standard view.

   You can also use the Full View on the Perspective view. It will
   work pretty fast with the Full View enabled on the Perspective
   view, so you can actually see the entire model in it's textured
   form here. Remember to hide unwanted parts when returning back
   to the normal view.

 Textures
   Textures are usually stored as .fsh images. You need a program
   such as FSHTool to convert it from .fsh to .bmp so that OEdit 
   can load them. OEdit will not let you edit the texture itself.
   You should use a image editing program to do that.

   This version of OEdit supports loading of Multiple Textures. 
   Some models such as cars from NFS6 use two textures (one for the 
   body skin and one for the tire/wheels) and stadiums from FIFA 2003
   use a lot more than 2 textures. OEdit can load up to 15 textures
   but you should keep one slot free if you need to use as much as
   15 textures.

   Use [Texture -> Manage Textures] to load and unload textures.

   By default, all parts will use the texture from the first slot,
   so if there are many parts that use one common texture, load it
   in here to save time. To change the texture used by a part,
   select the part in the Parts section so that it is active, then
   goto [Textures -> Apply To Current Part -> XXXXX]. XXXXX will be
   the texture you want that part to use. You have to find out which
   texture is used for which part.

 UV Map Editor
   The polygons (triangles) of the model are mapped to parts of 
   texture file. The UV Map Editor lets you modify this. You 
   generally do not have to modify it unless you are creating
   a totally new texture. The tools used here are exactly the
   same as the ones discussed before in this file.

  _______________
_| The Shortcuts |________________________________________________

 These are just shortcut commands that may help you while
 using OEdit. You can access some of these commands without 
 the use of the following shortcuts. Tt is recommended that 
 you read through this alteast once.
 
 General
 -------
 Open File: CTRL + O
 Save File: CTRL + S

 Undo: CTRL + Z
 Select All: CTRL + A
 Discard Selection: CTRL + D

 Editing
 -------
 Select Tool: Keys 1-5
 Auto Select Tool: Key 0
 Change Direction Options: ~
 Vertex Properties: CTRL + P

 Views
 -----
 Pan: CTRL + Left Click + Move Mouse
 Zoom: ALT + Left Click (Zoom In)
       ALT + Right Click (Zoom Out)
       CTRL + Q (Zoom In)
       CTRL + W (Zoom Out)
 Reset Zoom: ALT + HOME
 Reset Pan: CTRL + HOME
 Full View: CTRL + F

 3D View
 -------
 Zoom: Right Click + Move Mouse Up/Down
 Scale: CTRL + Right Click + Move Mouse Up/Down
 Rotate: Left Click + Move Mouse
 Full View: CTRL + F

 Textures
 --------
 Manage Textures: CTRL + R
 UV Map Editor: CTRL + T
 
 Invert Line Colors: I

  ___________________________
_| Copyrights and Trademarks |____________________________________

 EA GAMES, the EA GAMES logo, EA SPORTS, the EA SPORTS logo, and
 Electronic Arts are trademarks or registered trademarks of
 Electronic Arts Inc. in the U.S. and/or other countries.

  ____________
_| Disclaimer |___________________________________________________

 THIS SOFTWARE IS PROVIDED "AS IS" WITHOUT ANY WARRANTIES OF ANY
 KIND, EITHER EXPRESSED OR IMPLIED. UNDER NO CIRCUMSTANCE MAY THE
 PROGRAMMER(S) OF THIS SOFTWARE BE HELD LIABLE FOR ANY DIRECT,
 INDIRECT, INCIDENTAL, SPECIAL OR CONSEQUENTIAL DAMAGES ARISING
 OUT OF THE USE OF OR INABLITY TO USE THIS SOFTWARE. USE THIS
 SOFTWARE AT YOUR OWN RISK!

 YOU, AS THE USER OF THIS SOFTWARE, ARE RESPONSIBLE FOR ANY
 COPYRIGHT OR LEGAL MATTERS THAT ARISE FROM THE CREATION OR
 MODIFICATION OF COPYRIGHTED MATERIAL THROUGH THE USE OF THIS
 SOFTWARE. (REMEMBER TO GIVE CREDIT TO THE ORIGINAL AUTHORS
 WHO DID MOST OF THE WORK!)

