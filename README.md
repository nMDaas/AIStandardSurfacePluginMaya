# AI Standard Surface Substance Painter Plugin
This plugin was developed to address the problems with the default Adobe Substance Painter used in Maya.

The default plugin is not a huge problem if you have 1-2 objects with few UV shells. However, using the plugin becomes extremely inefficient if you have multiple objects or a group of objects with multiple shells. 

Some of these inefficiencies are:
* The default plugin only allows you to create one material at a time. If you have a plant group object with 1 stem, 1 pot, 1 soil object, 5 leaves, and 5 stems, you are forced to repeat the same material process creation 13 times
* Once materials are created, it is a tedious process to figure out which object is mapped to which box in the UV layout and assign the correct texture accordingly
    -  The user has to open up the UV Layout window and Hypershade window to assign texture, which clutters the screen
    - The user has to assign textures 13 times to the correct objects

 ## Tool Functionality
 This plugin has the following features:
 * Allows selection of desired folder of textures
 * Allows you to select an object, group of objects, or nested group of objects
 * Creates as many AI Standard Surface textures as contained in the folder selected 
 * Automatically assigns newly created materials to correct objects

## How To Use
* Download code and separate Plugin folder in the downloaded folder
* In the execute.py file, update the line with "folder =" to be the path to the plugin folder on your computer
* Open the "execute_tool.py" file in the Maya script editor
* Run the script

## Plugin Usage Details
 * While exporting texture files from Adobe Substance Painter, make sure you export the files with default names given by the program. Do NOT change these file names to something custom
 * For each texture in the folder, there must be a file for BaseColor, Roughness, Metalness, Height and Normal
 * After following the tool instructions and clicking 'Apply', if you realize you have to reimport the textures, undo. Make sure the material has been removed from the object and that the materials are gone from the Hypershade

 ## Troubleshooting: Materials Created but Have No File Textures Applied or Node/Texture not Found
 * Go to one of the newly created AI Standard Surface materials
 * Locate the BaseColor file for the material
 * Click on the open folder icon next to Image Name and locate the correct texture file on your device
 * After doing this, the material will update to the correct texures. If the other materials also update, great. If they does not, click on each material in the hypershade individually and they will also update to the correct textures

 If the Above Steps Didn't Work:
 * Assign your selected object or group of obejcts to a different texture
 * Edit > Delete By All Type > History
 * File > Optimize Scene Size (Click on the Options Box on the Side)
    - WARNING: This will delete any unused materials. Make sure all the materials you want to keep in your hypershade are at least assigned to a dummy object
    - Make sure the "Rendering nodes" box is ticked
    - Click Optimize
    - Click OK 
* Rerun the plugin the same way. You might also need to repeat the instructions in the section above

## Tool Demo:  

### Demo #1: https://youtu.be/xSYAs8dseuE
