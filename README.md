README
================

Interactive contents are found in the **Introduction** RMarkdown file.

## 1. Load `lidR` package

We are using the `lidR` package to process liDAR data from Puerto Rico.

``` r
# Code here
```

## 2. Load LAS files

The liDAR data consists of point clouds stored in .las (LAS) files.
These can be loaded into `R` using the `lidR` function `readLAS()`. Use
`readLAS()` to load in one of the `LAS` files from the data folder.

``` r
# Code here
```

## 3. Plot LAS files

The loaded LAS file can be viewed simply using the `plot()` function.
This brings up a 3D viewer that lets you pan and zoom around the LAS
point cloud. Try plotting the point cloud you loaded. The argument
`color` lets you determine which attribute to use to color points. By
default, the Z axis is used for color. Find what other attributes are
available for plotting and change the attribute used for coloring the
plot.

``` r
# Code here
```

## Ground classification

A key problem we are trying to solve is classifying the ground within
the LAS point cloud. From looking at the point cloud plot, you can
probably see where the ground is. We will be employing the function
`classify_ground()` in `lidR` to use an algorithm to identify the
ground. Try doing this for the LAS file you loaded, using the `pmf`
algorithm. Follow the comments in the code chunk for visualizing the
classified point cloud.

``` r
las_gnd <- classify_ground()


# Try plotting the classified points by their classification attribute to view results



# Another way of viewing the results is to plot a cross section.
# I've prepared a function in `functions/cross_section.r` to do this. Try this out.
# See the comments in that script for more details

source("functions/function_plotcross.r")
```

## Bulk data handling

We have many LAS files to process, so it is advantageous to do some
automation. Use the `list.files()` function to read in the names of all
the .las files in the data folder and store them in the vector
`las.names`. Load these file names into the `R` session using a loop and
store them in a list object (`las.list`)

``` r
# create a vector to hold the las file names to be loaded called `las.names`
las.names <- 

# load the .las files in `las.names` using a loop
# Write the loaded files to the list object `las.list`, created below:
las.list <- list()
```

With all the las files loaded, we can process them in bulk. Use any
method you like to perform ground classification on all the las files
loaded in `las.list`.

``` r
# Code here
```

Use the `plot_cross_class` function you tried out above to plot cross
sections for each LAS file. Save the plot of each LAS file as a .png
with a systematic name. You could use the function `ggsave()` for this.

``` r
# Code here
```
