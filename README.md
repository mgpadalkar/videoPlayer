# Video Player using OpenCV

This is an old code that I created sometime in 2010. While working on video shot detection, I needed a tool to perform frame-by-frame visual analysis. However, I wasn't aware of any that existed at that time and created one with Matlab. To sharpen my skills with C and OpenCV, I re-created the same, taking lessons from the [best available book on these topics](https://www.oreilly.com/library/view/learning-opencv/9780596516130/).

[![My Video Player using OpenCV](https://img.youtube.com/vi/XcoPG87O9LY/0.jpg)](https://www.youtube.com/watch?v=XcoPG87O9LY)

The control panel, buttons, text fields, slider, video screen, etc. which are all sub-regions of a big image, are implemented in C using the OpenCV library. The comments included in the code were useful to automatically generate [this page](https://mgpadalkar.github.io/videoPlayer/doxygen/) using [Doxygen](https://www.doxygen.nl/index.html)

* Tested with:
   - Ubuntu 16.04.7 LTS (GNU/Linux 4.15.0-142-generic x86_64)
   - [OpenCV 2.4.3](https://sourceforge.net/projects/opencvlibrary/files/opencv-unix/2.4.13/)


* How to compile?
  - The code can be compiled as follows:
  ```bash
  g++ video_player.c -o video_player `pkg-config --cflags --libs opencv`
  ```

  - To play a video pass the path of the video as the argument
  ```
  ./video_player some_video.avi
  ```

  - I compiled OpenCV-2.4.13 from source using the command
  ```bash
  unzip opencv-2.4.13.zip
  cd opencv-2.4.13
  mkdir build && cd build
  cmake -DWITH_CUDA=OFF ..
  make
  make install
  ```

