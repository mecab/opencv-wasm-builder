docker-opencv-wasm-builder
==========================
Docker container just to build OpenCV WebAssembly

Usage
=====
```bash
docker build -t opencv-wasm-builder .
docker run --rm -it -v `pwd`/built:/built opencv-wasm-builder
```

Will provide built WebAssembly under `built` directory.

**(Untested)** you can change where the source code comes from by specifying `OPENCV_SOURCE_URL` like the following.

```bash
docker build -t opencv-wasm-builder .
docker run --rm -it -v `pwd`/built:/built -e 'OPENCV_SOURCE_URL=https://github.com/opencv/opencv/archive/x.x.x.zip' opencv-wasm-builder
```

Or by setting a local OPENCV source code folder like the following.

```bash
docker build -t opencv-wasm-builder .
docker run --rm -it -v `pwd`/built:/built -v `pwd`/opencv:/opencv opencv-wasm-builder
```
