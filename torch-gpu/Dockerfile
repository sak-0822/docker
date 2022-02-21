FROM sak0822/torch-gpu:latest

RUN pip3 install jupyterlab
RUN pip3 install numpy pandas
RUN pip3 install torch torchvision

ENV LIBRARY_PATH /usr/local/cuda/lib64/stubs

ARG NB_USER="jovyan"
ARG NB_UID="1000"

RUN echo "auth requisite pam_deny.so" >> /etc/pam.d/su
RUN useradd -m -s /bin/bash -N -u $NB_UID $NB_USER

USER $NB_UID
RUN mkdir "/home/$NB_USER/work"

WORKDIR "/home/$NB_USER/work"

CMD ["jupyter", "lab", "--ip=*", "--no-browser"]
