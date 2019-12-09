Bootstrap: docker
From: nvidia/cuda:9.0-cudnn7-runtime
#From: python:3

%environment

#EXPOSE 1234 6006
PATH=${PATH}:${LSF_BINDIR}:/cm/local/apps/cuda/libs/current/bin
LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:/usr/local/cuda-9.0/lib64:/cm/local/apps/cuda-driver/libs/current/lib64
CUDA_PATH=/usr/local/cuda-9.0
CUDA_ROOT=/usr/local/cuda-9.0
export https_proxy="https://www-cache.gwdg.de:3128/"
export http_proxy="http://www-cache.gwdg.de:3128/"

%post



apt-get -y update
#apt-get -y install cuda
apt-get -y install python3 --reinstall
apt-get -y install python3-pip --reinstall

python3 -m pip install --upgrade pip 
python3 -m pip install numpy
python3 -m pip install torch torchvision tensorflow-gpu
python3 -m pip install jupyter matplotlib tqdm Pillow shapely opencv-python pandas scikit-learn imgaug imantics scipy scikit-image



%post
