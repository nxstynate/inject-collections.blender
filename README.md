#  Batch Collection Link Injector (Beta)

![Blender](https://img.shields.io/badge/Blender-4.5.0-orange.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Status](https://img.shields.io/badge/Status-Beta-red.svg)

![Screenshot 2025-07-26 123547.png](images/Screenshot%202025-07-26%20123547.png)

This Blender addon, "Batch Collection Link Injector," is designed to streamline the process of linking collections from a source `.blend` file into multiple target `.blend` files. It's particularly useful for projects where you need to inject a set of standard collections (like characters, props, or environments) into many different scene files, especially when dealing with a large number of files or a complex directory structure.

> **Note:** This is a beta version. Please back up your files before using this addon, as unforeseen issues could potentially lead to data loss.

## 📜 Table of Contents

- [Disclaimer](#disclaimer)
- [Installation](#installation)
- [How-to-Use](#how-to-use)
- [Dry-Run-Mode](#dry-run-mode)
- [Logging](#logging)
- [Known-Issues--Limitations](#known-issues--limitations)
- [Contributing](#contributing)
- [License](#license)

## ⚠️ Disclaimer

> This is a beta version of the addon. While it has been tested, there may be bugs or unexpected behavior. It is highly recommended to back up your project files before using this tool. The author is not responsible for any data loss or corruption that may occur.

## 🚀 Installation

1.  Download the `inject_collections.zip` file from the repository.
2.  Open Blender and go to `Edit > Preferences > Add-ons`.
3.  Click the "Install..." button and navigate to the downloaded `inject_collections.zip` file.
4.  Enable the "Batch Collection Link Injector" addon by checking the box next to its name.

## 📖 How to Use

The addon's panel can be found in the 3D View's UI panel (press `N` to open it) under the "Batch Linker" tab.

### 1. Select Source File

This section is for selecting the `.blend` file that contains the collections you want to link.

1.  Expand the "Select Source File" section.
2.  Click the "Load Source .blend" button.
3.  Navigate to and select the `.blend` file containing the collections you want to inject.
4.  Once loaded, you will see a list of all the collections from the source file.

![Screenshot 2025-07-26 123705.png](images/Screenshot%202025-07-26%20123705.png)

### 2. Select Root Directory

This section is for selecting the main folder that contains all the project folders where your target `.blend` files are located.

1.  Expand the "Select Root Directory" section.
2.  Click the "Load Root Directory" button.
3.  Navigate to and select the root directory of your projects.
4.  The list below will populate with all the subdirectories found in the selected root directory.

![Screenshot 2025-07-26 123715.png](images/Screenshot%202025-07-26%20123715.png)

### 3. Search Target Files

This section allows you to find the specific `.blend` files within the root directory that you want to inject the collections into.

1.  Expand the "Search Target Files" section.
2.  In the "Query" field, enter a part of the filename that is common to all your target files (e.g., `shot`, `scene`, `animation`).
3.  Click the "Search" button.
4.  The "Targets" list will populate with all the `.blend` files that match your query.

*(Screenshot of the "Search Target Files" section with a list of target files found)*

### 4. Find Matches

This section is where you match the collections from your source file to the subdirectories in your root directory. The addon will attempt to automatically match them based on the collection and subdirectory names.

1.  Expand the "Find Matches" section.
2.  Click the "Find Matches" button.
3.  The "Matches" list will show the collections from the source file and the subdirectory they have been matched with.
4.  You can manually check or uncheck the boxes to control which collections get injected into which subdirectories.
5.  You can use the "Select All Matches" and "Clear All Matches" buttons to quickly select or deselect all matches.
6.  Enable "Use Regex Matching" for more advanced matching using regular expressions.

![Screenshot 2025-07-26 123724.png](images/Screenshot%202025-07-26%20123724.png)

### 5. Inject Collections

This is the final step where the collections are linked into the target files.

1.  Expand the "Inject Collections" section.
2.  Review your selections in the previous steps.
3.  Click the "Inject Collections" button to start the process.
4.  The addon will open each target file in the background, link the specified collections, and save the file.

![Screenshot 2025-07-26 123733.png](images/Screenshot%202025-07-26%20123733.png)

## 🧪 Dry Run Mode

Before committing to the injection, you can perform a "Dry Run." This will simulate the injection process and show you what actions would be taken without actually modifying any files.

1.  Enable the "Dry Run" checkbox in the "Inject Collections" section.
2.  Click the "Inject Collections" button.
3.  The log will show which collections would be injected into which files.

## 📝 Logging

The "Log" panel in the "Inject Collections" section provides detailed information about the injection process. It will show you which files are being processed, which collections are being linked, and any errors that may have occurred. This is useful for troubleshooting and verifying that the process completed successfully.

![Screenshot 2025-07-26 123742.png](images/Screenshot%202025-07-26%20123742.png)

## 🐛 Known Issues & Limitations

*   **Blender Version:** This addon is developed for Blender 4.5.0 and may not be compatible with other versions.
*   **File Paths on Windows:** The script attempts to find the Blender executable on Windows, but it might not work for all installations. If you encounter issues, you may need to adjust the `blender_exec` path in the `inject_collections.py` file.
*   **Error Handling:** While there is error handling in place, it may not cover all possible scenarios. Always back up your files.

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, bug fixes, or improvements, please open an issue or submit a pull request on the GitHub repository.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.