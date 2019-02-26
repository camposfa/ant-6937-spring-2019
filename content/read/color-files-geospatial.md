---
title: "Color, Saving Output, and Geospatial Data"
---

## Read

#### Making Effective Use of Color

- **[Wilke, Ch. 4: Color scales](https://serialmentor.com/dataviz/color-basics.html)**
- **[Wilke, Ch. 19: Common pitfalls of color use](https://serialmentor.com/dataviz/color-pitfalls.html)**

<br><br>

#### Saving Plots as Image Files

- **[R4DS, Ch. 28.7: Saving your plots](https://r4ds.had.co.nz/graphics-for-communication.html#saving-your-plots)**

<br><br>

#### Visualizing Geospatial Data

- **[Why all world maps are wrong](https://www.youtube.com/watch?v=kIID5FDi2JQ)**
- **[XKCD Map Projections](https://xkcd.com/977/)**
- **[XKCD Heatmap](https://xkcd.com/1138/)**
- **[Wilke, Ch. 15: Visualizing geospatial data](https://serialmentor.com/dataviz/geospatial-data.html)**

<br>
<hr>
<br>

## Color Resources

![](/img/hcl-palettes-principles-1.png)

- [Color Brewer](http://colorbrewer2.org/): Color advice and a great set of color palettes; r package: [RColorBrewer](https://cran.r-project.org/package=RColorBrewer).
- [CARTOColors](https://carto.com/carto-colors/): Cartography-focused color palettes; r package: [rcartocolor](https://cran.r-project.org/package=rcartocolor).
- [viridis](https://cran.r-project.org/web/packages/viridis/vignettes/intro-to-viridis.html): Small set of very nice color palettes, best for sequential data; r package: [viridis](https://cran.r-project.org/web/packages/viridis).
- [colorspace](http://colorspace.r-forge.r-project.org/articles/colorspace.html): HCL-based color palettes; replicates some of the ones listed above, but also provides some interesting new ones; r package: [colorspace](https://cran.r-project.org/package=colorspace).
- [multiscales](https://github.com/clauswilke/multiscales): Multivariate color scales.
- [dichromat](https://cran.r-project.org/package=dichromat): A package to simulate color blindness.

<br><br>

## Optional further reading about image file formats.

- **[Wilke, Ch. 27: Understanding the most commonly used image file formats](https://serialmentor.com/dataviz/image-file-formats.html)**

<br><br>

## Extra Software and R Packages for Geospatial Data

Last week when we were trying to produce basic maps, some of you were able to get it working right away, whereas others were getting cryptic errors

If map-making is something that interests you, it would be a good idea to make sure that your computer has all the necessary software to do so by following the steps below.

If any of you are still having trouble getting the mapping to work, these steps should also resolve those problems.

1. Install software that enables your computer to compile R packages from their source code.

    - **Windows:** Download and install [Rtools](https://cran.r-project.org/bin/windows/Rtools/) (currently Rtools35.exe).
    - **Mac:** Open terminal and type `xcode-select --install`
<br><br>
2. Back in R Studio, install these packages: `sf`, `maps`, `maptools`, `rgeos`, and `rnaturalearth`.

3. _For Mac people only:_ R doesn’t do all the geographic calculations by itself. It relies on some other software that runs behind the scenes. When people on Windows install `sf`, those pieces of software should be installed automatically. This doesn’t happen on a Mac, so you have to install them manually. The easiest way to do this is with Terminal. Here's what you have to do:

    - Open Terminal
    - If you haven't already, go to [brew.sh](brew.sh), copy the big long command under "Install Homebrew" (starts with `/usr/bin/ruby -e "$(curl -fsSL...`).
    - Paste the command into Terminal, and press enter. This installs Homebrew, which is special software that lets you install Unix-y programs from the Terminal. This will take a while.
    - In Terminal, type this line to install the geographic software: `brew install gdal geos proj`. This will also take a while.