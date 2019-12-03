Bootstrap: docker
#From: nvidia/cuda:9.0-cudnn7-runtime
From: python:3

%environment

#EXPOSE 1234 6006
PATH=${PATH}:${LSF_BINDIR}:/cm/local/apps/cuda/libs/current/bin
LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:/usr/local/cuda-9.0/lib64:/cm/local/apps/cuda-driver/libs/current/lib64
CUDA_PATH=/usr/local/cuda-9.0
CUDA_ROOT=/usr/local/cuda-9.0

%post



apt-get -y update
apt-get -y install cuda
#apt-get -y install python3 --reinstall
apt-get -y install python3-pip --reinstall

pip3 install --upgrade pip
pip3 install numpy
pip3 install torch torchvision tensorflow-gpu
pip3 install jupyter matplotlib tqdm Pillow shapely opencv-python pandas scikit-learn imgaug imantics scipy scikit-image



%post
