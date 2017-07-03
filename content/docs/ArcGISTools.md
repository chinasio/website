# ARCGIS效率工具集

## 1.Create Filled Contours script tool for ArcGIS 10
Contours are lines that connect locations of equal value in a raster dataset. They are useful because they can show the shape of the phenomena represented by the raster surface that may be otherwise difficult to see.

In addition to raster and contour line representations of surfaces, visualizing and symbolizing surfaces as contour polygons (Fig. 1) can provide useful capabilities.  For example, querying the particular polygon can give you the area of elevation values between 100 m and 200 m, or allow you to select the polygon that represents the perimeter of a water body, or summarize all the vegetation types within each contour range.
**工具名称**：CreateFilledContours_10tbx.zip

## 2.Geoprocessing to split elevation into topography and bathymetry
When an elevation raster dataset contains values for both topography and bathymetry, often the best solution to this is to split it into two new rasters:  one for the topography and one for the bathymetry. The reason is that symbolizing this data is difficult. This is because a color ramp that contains appropriate hues for both bathymetry and topography must be adjusted so that it shows the shoreline exactly in the right place, at zero elevation. We have created a geoprocessing model that splits a raster elevation dataset into two datesets based on a split value you assign. Thus, this solution is ideal for small and medium sized elevation datasets as it offers the ability to precisely symbolize the land water interface.  The idea is to split the dataset at zero elevation and the use a land based color ramp for the output topography dataset and a water based color ramp for the output bathymetry dataset.
We have also created a style file (Topo_Bathy.style) that contain color ramps for a variety of elevation models. These are a few of the color ramps already on Mapping Center’s ArcGIS Resources tab and are provided here to get you started.
We will be posting several more blog entries on symbolizing terrain in the coming weeks (including strategies for symbolizing the land water interface on large elevation datasets as well), and will highlight these as well as the other color ramps that are available as in those entries. This is also a good place to note just who the “we” in this case represents, Aileen and I have been working with Witold Fraczek, who is an Application Prototype Specialist here at ESRI with a great deal of experience working with and producing terrain representations. Witold also created the color ramps in Topo_Bathy.style file.

**工具名称：** Elev_and_Bathy.ZIP
