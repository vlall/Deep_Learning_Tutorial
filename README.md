# Deep_Learning_Tutorial
Setup Deep Learning environment on GPU using Cuda/Caffe. There aren't many good tutorials on setting up GPU environment from scratch.

###Installation and Testing

```
$ sudo apt-get install build-essential
$ wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_7.0-28_amd64.deb
$ sudo dpkg -i cuda-repo-ubuntu1404_7.0-28_amd64.deb
$ sudo apt-get update
$ sudo apt-get install cuda 
$ vi ~/bash_profile
  add 2 lines [1] $ export PATH=/usr/local/cuda-6.5/bin:$PATH
              [2] $ export LD_LIBRARY_PATH=/usr/local/cuda-6.5/lib64:$LD_LIBRARY_PATH'
$ source ~/.bash_profile
Check version:
$ cat /proc/driver/nvidia/version
$ nvcc -V
if you see " The program 'nvcc' is currently not installed. You can install it by typing:
sudo apt-get install nvidia-cuda-toolkit", then make sure your bash profile is correct.
$ cuda-install-samples-7.0.sh <working directory>
$ cd <working directory>/NVIDIA_CUDA-7.0_Samples
$ make
$ cd bin/x86_64/linux/release
$ ./deviceQuery
$ ./bandwidthTest
```
