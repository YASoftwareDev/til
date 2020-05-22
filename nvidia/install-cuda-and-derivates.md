start with check if driver is up to date

this is official instruction:

https://www.tensorflow.org/install/gpu

it is rather awkward, because it first list needed packages and after that give commands to install them.

So I've installed using above one (lines in https://www.tensorflow.org/install/gpu#ubuntu_1804_cuda_101 - but before libinfer section install commands from tensort 6 (!) site) and also below one. I suggest read them and based on them use below instructions (also check for newer version - this document is 2 years old)

https://medium.com/@omar.merghany95/how-to-install-tensorflow-gpu-with-cuda-toolkit-9-0-and-cudnn-7-2-1-on-aws-ec2-ubuntu-16-04-c46b469a7358

also this one looks more specific:

https://towardsdatascience.com/how-to-install-tensorflow-gpu-on-ubuntu-18-04-1c1d2d6d6fd2

path to CUPTI looks obsolete (fd found it in main lib64 folder)

also use note from GG:

one need to install cudnn (required) and tensorrt(recommended) inside the docker:

```
sudo dpkg -i libcudnn7_7.6.5.32-1+cuda10.1_amd64.deb
sudo dpkg -i libcudnn7-dev_7.6.5.32-1+cuda10.1_amd64.deb
sudo dpkg -i libcudnn7-doc_7.6.5.32-1+cuda10.1_amd64.deb
os=ubuntu1804 tag=cuda10.1-trt6.0.1.5-ga-20190913 sudo dpkg -i nv-tensorrt-repo-${os}-${tag}_1-1_amd64.deb
sudo apt-key add /var/nv-tensorrt-repo-${tag}/7fa2af80.pub
sudo apt-get update
# cd /var cd nv-tensorrt-repo-cuda10.1-trt6.0.1.5-ga-20190913 sudo dpkg -i *.deb <- nope ;)
rather (based on: https://docs.nvidia.com/deeplearning/sdk/tensorrt-archived/tensorrt-601/tensorrt-install-guide/index.html)
sudo apt install tensorrt
sudo apt-get install python3-libnvinfer-dev
sudo apt-get install uff-converter-tf
```

test: (mnist compile -  choose alternative for gcc)

```
sudo update-alternatives --config gcc
```

but also:

❯ ipython3

In [1]: import tensorflow as tf
2020-05-04 23:36:47.607048: I tensorflow/stream_executor/platform/default/dso_loader.cc:44] Successfully
opened dynamic library libnvinfer.so.6
2020-05-04 23:36:47.628643: I tensorflow/stream_executor/platform/default/dso_loader.cc:44] Successfully
opened dynamic library libnvinfer_plugin.so.6

