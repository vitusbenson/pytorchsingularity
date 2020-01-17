Bootstrap: docker
#From: nvidia/cuda:9.0-cudnn7-runtime-ubuntu16.04
From: nvidia/cuda:10.1-cudnn7-runtime-ubuntu18.04
#From: python:3

%environment

#EXPOSE 1234 6006
PATH=${PATH}:${LSF_BINDIR}:/cm/local/apps/cuda/libs/current/bin
LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:/usr/local/cuda-9.0/lib64:/cm/local/apps/cuda-driver/libs/current/lib64
CUDA_PATH=/usr/local/cuda-9.0
CUDA_ROOT=/usr/local/cuda-9.0
https_proxy="https://www-cache.gwdg.de:3128/"
http_proxy="http://www-cache.gwdg.de:3128/"

%post

apt-get -y update
#apt-get -y install software-properties-common
#add-apt-repository ppa:deadsnakes/ppa
#apt-get -y install cuda
#apt -y install python3.8
apt-get -y install python3.8 --reinstall
apt-get -y install python3-pip --reinstall
apt-get -y install libglib2.0-0
apt-get -y install wget
apt-get -y install pv
apt-get -y install git
apt-get -y install libavcodec-dev libavformat-dev libswscale-dev
apt-get -y install libgstreamer-plugins-base1.0-dev libgstreamer1.0-dev
apt-get -y install libgtk-3-dev
apt-get -y install libpng-dev
apt-get -y install libjpeg-dev
apt-get -y install libopenexr-dev
apt-get -y install libtiff-dev
apt-get -y install libwebp-dev

python3 -m pip install --upgrade pip 
python3 -m pip install --upgrade setuptools
python3 -m pip install numpy
python3 -m pip install torch torchvision tensorflow-gpu
python3 -m pip install jupyter matplotlib tqdm Pillow shapely opencv-python pandas scikit-learn imgaug imantics scipy scikit-image
python3 -m pip install git+https://github.com/QUVA-Lab/e2cnn.git
