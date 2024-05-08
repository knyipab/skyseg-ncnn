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

## Test result
```bash
curl -o demo.jpg -L https://lh3.googleusercontent.com/pw/AP1GczNsgYY61QHlnYai--x-scRy_QJbkqGyASQN39lcL5ZD_AcMitUQqQ8mWy8Bf_FruvknK0_Pw77VqO84FtGU4z8OZMWP2qWAkRnqHUrZYESZiuFNKpCHEzXCpQ6fdeT1wbiJuCgtbcea_60ym7NAzwxN=w943-h1257-s-no-gm

skyseg-ncnn demo.jpg demo-sky.jpg
```
It works also for night sky. 

![demo](https://github.com/termux-user-repository/tur/assets/46513942/3f602087-2e7e-4e43-b5eb-08b7a4c81cc9)

![demo-sky](https://github.com/termux-user-repository/tur/assets/46513942/f1853e9d-be17-4ae5-a367-74c3ac1a111e)
