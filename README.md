# cool
**Centroid Origin Optimising Localiser**


**OVERVIEW:**
cool is a Python package for: 

*i) Fitting 2D Gaussians in an elliptical (toroidal) shape and identifying the centre 

*ii) Finding the centre of a set of point localisations and measuring the weighted mean distance (radial distance in this case, but can be adapted) Originally designed to work with SMLM data, the point localisations have Gaussian distributed probability densities and this parameter is used to weight each point's contribution to the radius. 

**REQUIREMENTS:**

 1. Several Python packages are used:

  * Numpy
  * PIL or pillow -- PIL has been deprecated and is interchangeable with a PIL-friendly fork, pillow for new installations
  * matplotlib
  * math
  * copy
  * time
  * Mrc or mrcfile -- Mrc has been deprecated and is interchangeable with mrcfile
  * tifffile
  * scipy
  * gaussfitter -- gaussfitter requires installation of the astropy and astropy_helpers packages available at https://github.com/keflavich/gaussfitter

 2. Elliptical ring are fit from tiff files

 3. Elliptical rings are fit from initialised centroid estimates summarised in a single csv file per image

 4. SMLM data has the following format in columns
''' 
#0 - NA
#1 - X pos nm
#2 - Y pos nm
#3 - Localisation accurancy
#4 - Localisation accurancy
#5 - sigma of PSF
#6 - sigma of PSF
#7 - number of detected photons
#8 - frame number
'''
**INSTALLATION:**

The code is Python 2 compatible and can be run as is - it is soon to be adapted to a full packages

**CONFIGURATION:**

Some variables are configurable:

 * DATASET: filename
 * LMPIXELSIZE: pixel size of SMLM image
 * SIGMA2FWHM:necessary to calculate the ratio of the FWHM of sigma from psf (columns 5,6)
 * WINDOW - first instance: Root size of square regions to isolate elliptical rings
 * DISTANCE: Upper limit of radial distances measured (nm)
 * ACCURACY:  Lower limit of localisation accuracy (nm)
 * REGION: Root size of square regions to isolate elliptical rings and SMLM clouds
 * WINDOW - second instance: Root size of square regions to isolate SMLM clouds
 * WIN: Size of SMLM images (pixels)

**KNOWN ISSUES:** 

Many!




