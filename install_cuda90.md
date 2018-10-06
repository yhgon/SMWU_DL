
## install cuda 9.0 in COLAB
cuda 9.0 is already installed in COLAB but they are missing some libraries such as cublas, cusolver, cusparse and curand. 
use below script. 

```
!rm -rf cuda-repo*
!wget https://developer.nvidia.com/compute/cuda/9.0/Prod/local_installers/cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64-deb
!apt-get install dirmngr
!dpkg -i cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64-deb
!apt-key add /var/cuda-repo-9-0-local/7fa2af80.pub
!apt-get update
!apt-get install  -y --no-install-recommends  \
 cuda-core-9-0 \
 cuda-cublas-9-0 cuda-cublas-dev-9-0 cuda-cudart-9-0 cuda-cudart-dev-9-0 \
 cuda-cufft-9-0 cuda-cufft-dev-9-0 cuda-curand-9-0 cuda-curand-dev-9-0 \
 cuda-cusolver-9-0 cuda-cusolver-dev-9-0 cuda-cusparse-9-0 \
 cuda-cusparse-dev-9-0 \
 cuda-libraries-9-0 cuda-libraries-dev-9-0 \
 cuda-misc-headers-9-0 cuda-npp-9-0 cuda-npp-dev-9-0 \
 cuda-nvgraph-9-0 cuda-nvgraph-dev-9-0 cuda-nvml-dev-9-0 cuda-nvrtc-9-0 \
 cuda-nvrtc-dev-9-0
!rm -rf cuda-repo*
!rm -rf wget-log*
```
