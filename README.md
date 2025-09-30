# Copy-and-Rename-Files-usig-Uipath

### Name: Preethi J
### Reg no: 212223220080

# Aim:
To design and execute an automation process in UiPath that copies files from a source location and renames them in the destination folder according to given requirements.

# Procedure:
1. Open UiPath Studio.
   - Create a new Process project (e.g., CopyAndRenameFiles).

2. Define Variables.
   - sourcePath → string → path of the source folder.
   - destinationPath → string → path of the destination folder.
   - files → array of string → to store all file paths.

3. Activities Sequence.
   * Assign Activity
     - files = Directory.GetFiles(sourcePath) → fetch all files.

   * For Each Activity
     - Input: files
     - Type Argument: String

   * Inside For Each → Copy File Activity
     - From: item (current file in loop)
     - To: Path.Combine(destinationPath, "Renamed_" + Path.GetFileName(item))
(This copies and renames the file with a prefix Renamed_).

4. Run the Workflow.
UiPath will loop through each file, copy it to the destination folder, and rename it.
