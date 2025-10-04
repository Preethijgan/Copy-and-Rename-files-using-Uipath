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

<img width="1919" height="1013" alt="Screenshot 2025-10-04 195157" src="https://github.com/user-attachments/assets/af566aa2-a450-4194-9cb2-5a512ba6dd75" />
<img width="1912" height="1023" alt="Screenshot 2025-10-04 195217" src="https://github.com/user-attachments/assets/c6155458-4c33-432e-a407-e84095b559e2" />

# Output:

## Source:
<img width="1919" height="1079" alt="Screenshot 2025-10-04 195122" src="https://github.com/user-attachments/assets/5bc564c2-44fd-4129-b904-cca99e8a5ade" />

## Destination:
<img width="1919" height="1079" alt="Screenshot 2025-10-04 195130" src="https://github.com/user-attachments/assets/512d3a92-a91a-41eb-9a88-75691768556d" />

# Result:
All files from the Source Folder are successfully copied to the Destination Folder. Each copied file is renamed by appending the current timestamp.


