# docker

These are dockerfiles for PyTorch with gpu(cuda-11.5 cudnn8.3.5).

# How to use?
In order to use, type in your CLI\n
docker build -t <name> <path to Dockerfile>
docker run -it --rm --gpus all <name> bash
  
## or
docker-compose up -d
 
