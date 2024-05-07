# skyseg-ncnn
* cmake build of [xiongzhu666/Sky-Segmentation-and-Post-processing](https://github.com/xiongzhu666/Sky-Segmentation-and-Post-processing)
* packaged as `skyseg-ncnn` on TUR
* this repo exists only because the original repo by xiongzhu666 does not provide a proper build script

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
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=<path-to-prefix> ..
cmake --build .
cmake --install .
```
