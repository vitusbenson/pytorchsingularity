Bootstrap: docker
From: python:3

%environment

EXPOSE 1234 6006


%post



apt-get -y update
#apt-get -y install python3 --reinstall
apt-get -y install python3-pip --reinstall

#pip install --upgrade pip
pip3 install numpy
pip3 install torch torchvision tensorflow
pip3 install jupyter matplotlib tqdm Pillow shapely opencv-python pandas scikit-learn imgaug imantics scipy scikit-image

