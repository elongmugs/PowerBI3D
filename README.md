Here is the updated README with the necessary changes:

---

# Important Info When Building from Source-Code

**Used Versions to Build From:**
- `powerbi-visuals-tools@4.2.1`
- `powerbi-visuals-api@3.8.0`
- `Nodejs v20.17.0`

## Power BI 3D

Custom Visual for Power BI to visualize 3D models and connect them to your data. It uses the library three.js
Supports files:
3DM 
GLB ( GLB dont support coloring... yet :))


## Acknowledgement

This custom visual was developed by Diego Apellániz.<br />
Thanks to [McNeel](https://discourse.mcneel.com/t/3dmloader-for-three-js/107702) for the wonderful 3DM loader for three.js.<br />
Thanks to Tizian Alkewitz for the intensive beta testing.

## What's New in Version 1.0.3

- **Export Functionality**: Added the button `Export Model Data to Console` for UUID export without needing to drag data into data fields.
- **Capabilities Enhancement**: Added support for landing pages and empty data views, eliminating the need to drag files into the visual to load the model.

## How to Use the New Features

1. **Load the Model**:
   - Directly load your 3D model from HDD into the custom visual without needing to drag data into Power BI data fields.

2. **Publish to Power BI Online**:
   - In Power BI Desktop, click `Publish` to upload your report to Power BI Online.
   - Choose the appropriate workspace and confirm the publication.

3. **Open Developer Tools**:
   - Press `F12` to open the developer tools in your browser.

4. **Export UUIDs**:
   - Click the `Export Model Data to Console` button on the custom visual.
   - UUIDs of the 3D model will be displayed in the developer tools console.

5. **Copy UUIDs**:
   - Right-click the UUIDs in the console and select "Copy."

6. **Save UUIDs**:
   - Open a new text file, paste the copied UUIDs, and save the file with a `.csv` extension.

7. **Import to Power BI**:
   - Open Power BI and import the CSV file containing the UUIDs.

## How to Use

1. **Add Custom Visual to Power BI**:
   - Download the latest [release](https://github.com/diego-apellaniz/PowerBI3D/releases) of this repository.
   - Download and install [Power BI Desktop](https://www.microsoft.com/store/productId/9NTXR16HNW1T).
   - Open Power BI, create a new file, and go to `Files -> Import -> Power BI Visual from File` and select `PowerBI3D.pbiviz` from the downloaded files.
   - Create a PowerBI3D visual in Power BI by selecting the imported visual from the visualizations panel on the right side. It won't display anything until you connect it to your data and upload the 3D model.

2. **Prepare and Import Data**:
   - Prepare an Excel table with GUIDs of the objects in your 3D model. Additional columns may include categories and values. Ensure all cells of the table are filled.
   - Import the prepared Excel file into Power BI.

3. **Connect 3D Model to Your Data**:
   - In Power BI, use the PowerBI3D visual to connect your imported data. If only GUIDs are provided, the model will be displayed in gray. With additional categories or values, the model will reflect the color palette and gradients based on the provided data.

4. **Import 3D Model in Power BI**:
   - Post-process your 3D model. Remove elements not included in the GUIDs column. Convert all geometry elements to meshes if using a Rhino model.

---

Feel free to adjust any further details as needed!
