# caffe-yolov2

## Reference

> YOLO9000: Better, Faster, Stronger

> http://pjreddie.com/yolo9000/

> https://github.com/yeahkun/caffe-yolo

> https://github.com/hustzxd/z0

> https://github.com/hustzxd/z1

> https://github.com/weiliu89/caffe.git

## modifications

1. add reorg_layer

2. convert yolo weights to caffemodel

3. add detection output layer

4. add detection evaluate layer

## Usage

### convert model

`cd examples/indoor/convert`

1. convert yolo.cfg to yolo.prototxt
2. convert yolo weights to caffemodel

`python3 convert_weights_to_caffemodel.py --prototxt yolo.prototxt --weights yolo.weights --caffemodel yolo.caffemodel`

## Windows Installation
### Prerequisites
* Anaconda for python 3.x.
* CMAKE (must be added to PATH).
* Visual Studio Community 2015 or higher.
* NVIDIA cuda and cudnn for GPU operation.

### Build from source
* Configure the build environment (set CPU_ONLY to 0 for GPU build, set the CUDNN_ROOT corresponding to your installation,...etc) in the `scripts/build_win.cmd`
* Run the build script `scripts/build_win.cmd`
* If the build process goes well, the `build/install` directory will hold the build output (python package + caffe windows executables)
* Copy `build/install/python/caffe` directory to anaconda site-packages (ANACONDA_ROOT_DIR/Lib/site-packages)
