# Start with Theano base image
FROM kaixhin/theano
MAINTAINER Kai Arulkumaran <design@kaixhin.com>

# Install dependencies
RUN apt-get update && apt-get install -y \
  libhdf5-dev \
  python-h5py \
  python-yaml

# Upgrade six
RUN pip install --upgrade six

# Clone Keras repo and move into it
RUN cd /root && git clone https://github.com/fchollet/keras.git && cd keras && \
  # Install
  python setup.py install

# Set ~/keras as working directory
WORKDIR /root/keras
