FROM nvcr.io/nvidia/l4t-base:r32.2
RUN sudo apt-get update -y 
RUN sudo apt-get install python3-pip -y 
RUN sudo pip3 install -U pip
RUN sudo DEBIAN_FRONTEND=noninteractive apt-get install libhdf5-serial-dev hdf5-tools libhdf5-dev zlib1g-dev zip libjpeg8-dev -y
RUN sudo DEBIAN_FRONTEND=noninteractive apt-get install python3 python-dev python3-dev build-essential libssl-dev libffi-dev libxml2-dev libxslt1-dev zlib1g-dev -yq
RUN CFLAGS="-I/usr/include/hdf5/serial" LDFLAGS="-L/usr/lib/aarch64-linux-gnu" pip3 install -U numpy grpcio absl-py py-cpuinfo psutil portpicker six mock requests gast h5py astor termcolor protobuf keras-applications keras-preprocessing wrapt google-pasta
RUN pip3 install --pre --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v42 tensorflow-gpu
