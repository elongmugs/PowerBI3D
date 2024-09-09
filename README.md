

# Important Info When Building from Source-Code

**Used Versions to Build From:**
- `powerbi-visuals-tools@4.2.1`
- `powerbi-visuals-api@3.8.0`
- `Nodejs v20.17.0`

## Power BI 3D

Custom Visual for Power BI to visualize 3D models and connect them to your data. It uses the library three.js.
Supported file formats:
- **3DM**
- **GLB**

## Acknowledgement

This custom visual was developed by Diego Apellániz.<br />
Thanks to [McNeel](https://discourse.mcneel.com/t/3dmloader-for-three-js/107702) for the wonderful 3DM loader for three.js.<br />
Thanks to Tizian Alkewitz for the intensive beta testing.

## What's New in Version 1.0.4

- **Model Type Tracking**: Added a new `modelType` property to track whether the model loaded is `3dm` or `glb`, allowing for different handling of model types.
- **New Export Button**: A new **"Export Model Data to Clipboard"** button is added to make it easier to export model data such as position, geometry, and material information. For `3dm` models, the `UUID` is exported, and for `glb` models, the `Name` is exported and renamed as `UUID` for consistency.
  
---

## How to Use Power BI 3D

1. **Add Custom Visual to Power BI**:
   - Download the latest [release](https://github.com/diego-apellaniz/PowerBI3D/releases) of this repository.
   - Install [Power BI Desktop](https://www.microsoft.com/store/productId/9NTXR16HNW1T).
   - Open Power BI, create a new file, and go to `Files -> Import -> Power BI Visual from File`. Select `PowerBI3D.pbiviz` from the downloaded files.
   - Create a PowerBI3D visual by selecting the imported visual from the visualizations panel. Upload a 3D model file to begin using it.

2. **Prepare and Import Data**:
   - Prepare a data table with UUID or Names of the objects in your 3D model. You can include additional columns like categories and values for more advanced visualizations.
   - Import this table into Power BI.

3. **Connect Data to Your 3D Model**:
   - In Power BI, use the PowerBI3D visual to connect your imported data. If only UUID´s are provided, the model will be displayed in gray. If categories or values are added, the model will reflect the colors or gradients based on the data.

4. **Post-process Your 3D Model**:
   - Ensure that the 3D model is ready for Power BI by removing unnecessary elements and converting geometry to meshes where needed (especially if using Rhino models).

---

## How to Use the Export Feature (Version 1.0.4)

1. **Load a 3D Model**:
   - Ensure you load a supported 3D model (`3dm` or `glb`) into the custom visual.
   
2. **Locate the Export Button**:
   - Find the **"Export Model Data to Clipboard"** button in the user interface.

3. **Export the Model Data**:
   - Clicking the button will automatically extract data from the loaded model. For `3dm` models, `UUID` is exported. For `glb` models, the object name is exported but renamed to `UUID` when copied.

4. **Save and Use the Data**:
   - Open a new **Notepad** and paste the data, then save the file as a `.csv` file.
   - Use the exported data for further analysis in other tools like Excel or Power BI.

5. **Import Data into Power BI**:
   - To import the CSV file into Power BI, press **Get Data** and select **CSV**. If Power BI generates columns named "Column 1", "Column 2", etc., go to **Transform Data** and click **Use First Row as Headers**.
![image](https://github.com/user-attachments/assets/41fd7a63-c9e8-4bb4-986a-085fb4251619)
