# docker

These are dockerfiles for PyTorch with gpu(cuda-11.5 cudnn8.3.5).

# How to use?
In order to use this, type in your CLI,
docker build -t \<container_name\> \<path to Dockerfile\> &&
docker run -it --rm --gpus all --ports 8888:8888 \<container_name\>
  
## or
docker-compose up -d
 
