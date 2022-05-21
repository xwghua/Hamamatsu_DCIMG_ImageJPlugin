# Hamamatsu_DCIMG_ImageJPlugin
A simple ImageJ Plugin for reading *.dcimg files.

### Usage
* Download the file and directly put into 
``` [FijiImageJ Directory] -> plugins -> Scripts -> Plugins ```.
* Restart FijiImageJ and look into the reader in the Plugins menu.

### Acknowledgement
* This code is inspired and modified from [orlandi-hamamatsuOrcaTools](https://github.com/orlandi/hamamatsuOrcaTools).
* This code has been demonstrated for Hamamtsu ORCA 4.0 image files.

### Additional problems to be aware
* When you open a "\*.dcimg" file, you will notice that there are four weird pixels located at the very left side of the mid-row of the image. That's because, for some unknown reasons, the bytes representing these four pixels do not corresponding to where they should be in the images. Instead, they bytes representing these four pixels are located at 12 bytes after each image bytes. I cannot find the source code of the "ij" package that ImageJ calls, so I have little idea how to fix it in ImageJ.
* If you do care these four pixels, please turn to the MATLAB version of dcimg reader [dcimg2tiff-dcimg.m](https://github.com/xwghua/dcimg2tiff/blob/master/dcimg.m) for a more accurate results.
