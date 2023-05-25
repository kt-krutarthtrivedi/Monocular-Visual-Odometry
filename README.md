# Monocular Visual Odometry using Classical Computer Vision Algorithms
This is an OpenCV 3.0 based implementation of a monocular visual odometry algorithm.

## Algorithm
Uses Nister's Five Point Algorithm for Essential Matrix estimation, and FAST features, with a KLT tracker.
More details are available [here as a report](https://drive.google.com/file/d/1WHl7R2p9dTz9Sk0ZhyWailfwr-hr6_37/view?usp=drive_link)

Note that this project is not yet capable of doing reliable relative scale estimation, 
so the scale informaion is extracted from the KITTI dataset ground truth files.

## Demo Video

[![Demo video](http://share.gifyoutube.com/Ke1ope.gif)](http://www.youtube.com/watch?v=homos4vd_Zs)


## Requirements
OpenCV 3.0

## Compilation instructions
Provided with this repo is a CMakeLists.txt file, which you can use to directly compile the code as follows:
```bash
mkdir build
cd build
cmake ..
make
```

## Run instructions
After compilation, in the build directly, type the following:
```bash
./vo
```
## Before you run
In order to run this algorithm, you need to have either your own data, 
or else the sequences from [KITTI's Visual Odometry Dataset](http://www.cvlibs.net/datasets/kitti/eval_odometry.php).
In order to run this algorithm on your own data, you must modify the intrinsic calibration parameters in the code.

## Performance
![Results on the KITTI VO Benchmark](http://avisingh599.github.io/images/visodo/2K.png)
