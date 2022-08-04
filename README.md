# ALGetReservedObjects
Visual Studio Code Extension for AL developers to find out the reserved object numbers of an AL project or workspace.

# Usage
This extension can be executed from the F1 or Ctrl-Shift-P menu with command
"AL GetReservedObjects".

# Process
The extension loops through the open folder or Workspace and their subfolders, finds out all .al files and extracts information what object and object number it has reserved.
Folders that start with dot (for example .alpackages) are skipped.

The result is three files in the root folder:
* ReservedObjects.csv: This file contains object and extension information extracted from .al and app.json file

* ReservedObjectsByExtension.txt: This file contains the reserved obejects in the order they have been found. On top of each section is the extension name.

* ReservedObjectsByObjectType.txt: This file has the objects sorted out by their name and number. Full object types (table, page, codeunit, menusuite, query, enum, report and xmlport) are listed first, and then extended objects (pageExtension, tableExtension, reportExtension, enumExtension).

In the end of later two files is a summary of object types and the number of their occurrences as well as number of found .al files and the count of reserved objects.

# Changelog
* 0.0.3.  Fix documentation, added error messages, added .csv output, added extension name to ReservedObjectsByExtension.txt
* 0.0.2.  Added instructions and changed displayname from "GetReservedObjects" to "AL GetReservedObjects"
* 0.0.1.  Initial publish
