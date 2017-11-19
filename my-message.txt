# file
this is a file for my message
    Ubuntu15.10 x64
    Opencv3.1

方法/步骤

    apt-get update

    apt-get upgrade

    apt-get install libqt4-dev libopencv-dev build-essential cmake git libgtk2.0-dev pkg-config python-dev python-numpy libdc1394-22 libdc1394-22-dev libjpeg-dev libpng12-dev libtiff5-dev libjasper-dev libavcodec-dev libavformat-dev libswscale-dev libxine2-dev libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev libv4l-dev libtbb-dev  libfaac-dev libmp3lame-dev libopencore-amrnb-dev libopencore-amrwb-dev libtheora-dev libvorbis-dev libxvidcore-dev x264 v4l-utils unzip 

    下载opencv3.1 

    wget https://github.com/Itseez/opencv/archive/3.1.0.zip

    下载完了 放在 /usr/local

    用 unzip 解压刚才下载文件

    进入opencv-3.1.0

    创建build

    进入 build 

    接下来 就开始干

    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_TBB=ON -D WITH_V4L=ON -D WITH_QT=ON -D WITH_OPENGL=ON ..
    7

    make -j $(nproc)

    和

    make  install 
    8

    /bin/bash -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'

     ldconfig(这一步很重要)
    9

    pkg-config --modversion opencv

    pkg-config --cflags opencv
