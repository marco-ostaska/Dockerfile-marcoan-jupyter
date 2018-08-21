FROM debian:9-slim

ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV PATH=/opt/miniconda3/bin:$PATH

RUN apt update && apt install -y wget \
   bzip2 \
   && apt clean all \
   && rm -rf /var/lib/apt/lists/* \
   && wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh \
   && chmod 775 Miniconda3-latest-Linux-x86_64.sh \
   && ./Miniconda3-latest-Linux-x86_64.sh -p /opt/miniconda3 -b \
   && rm -rf Miniconda3-latest-Linux-x86_64.sh \
   && conda install jupyter -y \
   && conda install jupyter_dashboards -c conda-forge -y \
   && conda clean --all -y

EXPOSE 8888

VOLUME "/jupyter_files"

WORKDIR "/jupyter_files"

CMD ["/bin/bash"]

ENTRYPOINT jupyter notebook --ip="*" --allow-root --no-browser --NotebookApp.token="abcd1234"
