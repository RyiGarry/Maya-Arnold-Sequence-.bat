I spent a fair amount of time in the documentation for Arnold + Maya, trying to figure out how to get batch rendering or single licence command line rendering working. For some reason, the docs are sparse and it was quite hard to figure out (unlike Blender command line rendering). This is a simple Excel file that helps render multiple files with a single instance of Maya Arnold - meaning you don't have to have a separate Arnold licence or use a farm.. as long as you're happy with it rendering each file one-by-one.

It assumes that all the files are in the same directory, but saves then to another folder named after the .mb file name. Only the yellow cells need changing depending on file locations and other variables. This is info re the render flags in cell B31: https://help.autodesk.com/view/ARNOL/ENU/?guid=arnold_for_maya_rendering_am_Batch_Render_Flags_html

The sample .xlsx here also is optimised for GPU rendering. When GPU rendering in Arnold, it seems to only able to render around 15-20 frames before quitting in command line render - here each line only renders 15 frames before restarting the render. Make sure to use a closing slash in the 'File Location' cell (B20).

To make it work, all you have to do is copy the formulas in column B to column A - using 'paste values' to convert to text. Then copy into a text file and save as a .bat. Run that .bat from Command Prompt.
