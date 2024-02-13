![Python 3.11.7](https://img.shields.io/badge/python-3.11.7-blue.svg)
# Point Cloud Resizer™
Point Cloud Resizer™ is a Python script that allows you to open, modify, and save point clouds in LAS or LAZ format. You can downsample (reduce) the point cloud by specifying a voxel size and then view or save the result in a new LAS file.

This script uses the following Python libraries:

- `tkinter` for the graphical user interface (GUI).
- `laspy` for reading and writing LAS/LAZ files.
- `open3d` for working with point clouds and visualization.
- `numpy` for manipulating numerical data.
- `os` for working with file paths and file management.
- `subprocess` for starting a separate process for visualization.
- `threading` for executing operations in separate threads to maintain GUI reactivity.

## Usage
1. Open the folder where the file `pointCloudResizer.py` is located. In Windows Explorer, select the location bar, similar to step 4 of installation. Instead of copying the location, press the Backspace key (←) on the keyboard when the location is highlighted in blue, type `cmd`, and press the Enter key. This will launch Command Prompt for CAD users in the correct location. To start the application, type `Python pointCloudResizer.py`. A window will open with several buttons.
2. Click the "Open file" button to select a LAS or LAZ file.
3. Choose a voxel size (distance between points) in the "Voxel size" field.
4. Click the "Apply subsampling" button to downsample the point cloud based on the specified voxel size.
5. The point cloud size after downsampling is displayed in the "Point cloud size after subsampling" field, and the subsampling factor is shown in the "Subsampling factor" field.
6. You can preview the downsampled point cloud by clicking the "Preview" button. This opens a 3D visualization window with the point cloud.
7. If you are satisfied with the result, you can save the point cloud in a new LAS file by clicking the "Save" button. This opens a dialog box where you can choose the file name and location.
8. The new LAS file is saved, and a notification appears with the storage location.

## Notes
- This script is designed to work with LAS and LAZ files, commonly used formats for point clouds in the geomatics and 3D scanning industry.
- Make sure you have the `logo.ico` file in the same folder as the script for displaying the icon in the application window.
- If the LAS/LAZ file has an unknown format or cannot be processed, an error message is displayed.
- The point cloud is downsampled using a regular grid based on the specified voxel size. The script normalizes the size of the point cloud based on the original point density.
