# skyseg-ncnn
* cmake version of xiongzhu666/Sky-Segmentation-and-Post-processing
* supports Linux only
* made for Termux TUR pacakge

## Description
```
Apply sky segmentation ncnn model on input image(s) and output mask image(s). 
Adapted from https://github.com/xiongzhu666/Sky-Segmentation-and-Post-processing by Ronald Y

Usage: skyseg-ncnn [input] [output]

Arguments: 
    input       input file or folder
    output      output file or folder
```

## Dependencies
* OpenCV
* ncnn

## Build
```bash
cmake .. && cmake --build .
cmake --install .
# cmake --install . --prefix="<location-to-install>"
```
