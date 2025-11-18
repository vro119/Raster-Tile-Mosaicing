## Raster Tile Mosaicing

A raster mosaicing task focused on generating a cloudless mosaic image by seamlessly merging multiple georeferenced satellite raster tiles (GeoTIFFs). The code should efficiently combine overlapping tiles with consistent spatial resolution and coordinate reference systems, ensuring smooth transitions between scenes. The final output must be a clean, cloud-free mosaic, properly georeferenced and visualized using Python-based geospatial libraries. The complete workflow should be demonstrated in a Jupyter Notebook (Kaggle/Colab) using the provided sample raster tiles.

### Generated Mosaic Link:
https://shorturl.at/RwD7y


### 1.1. Libraries Used
- **rasterio**: For reading, writing, and manipulating GeoTIFF raster data, including merging and reprojection.
- **numpy**: For numerical operations and array handling during resampling and data processing.
- **matplotlib**: For visualizing raster tiles and the final mosaic.
- **glob**: For file pattern matching to locate GeoTIFF files in the data directory.
- **shutil**: For file operations like copying the output to Google Drive and cleaning up temporary files.
- **subprocess**: For running external commands like gdal_merge.py.
- **google.colab**: For mounting Google Drive in Colab environment (Colab-specific).

### 1.2. Steps to Run the Code
1. **Setup Environment**: Open the `raster_mosaic_workflow.ipynb` notebook in Google Colab or Jupyter Notebook.
2. **Mount Google Drive (Colab)**: Run the cell to mount your Google Drive and set the data directory path.
3. **Install Libraries**: Uncomment and run the pip install cell if needed (though most are pre-installed in Colab).
4. **Verify Data**: Run cells to check the 'data' folder and list files.
5. **Preview and Validate Tiles**: Load and inspect sample tiles for CRS, resolution, and bounds.
6. **Resample Tiles**: Resample all tiles to average resolution using disk-based approach to save RAM.
7. **Mosaic Creation**: Use gdal_merge.py to merge resampled tiles into a single GeoTIFF.
8. **Install GDAL (if needed)**: The notebook checks and installs GDAL in Colab.
9. **Copy Output to Drive**: Run the final cell to copy the `cloudless_mosaic.tif` to your Google Drive.

### 1.3. Summary of Results
The workflow successfully produces a seamless, cloudless mosaic (`cloudless_mosaic.tif`) by resampling input GeoTIFF tiles to a uniform average resolution and merging them using GDAL. The output is a single georeferenced GeoTIFF with consistent CRS and resolution, suitable for visualization and further analysis. The disk-based processing ensures efficiency in memory-constrained environments like Colab, and the final mosaic is copied to Google Drive for easy retrieval.

