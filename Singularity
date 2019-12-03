Bootstrap: docker
From: pytorch/pytorch:latest

%post



apt-get -y update
apt-get -y install python3 --reinstall
apt-get -y install python3-pip --reinstall

pip install --upgrade pip
pip install numpy
pip install torch torchvision tensorflow
pip install jupyter matplotlib tqdm Pillow shapely opencv-python pandas scikit-learn imgaug imantics scipy scikit-image


%environment

EXPOSE 1234 6006