FROM nvcr.io/nvidia/tensorflow:25.02-tf2-py3

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=America/Los_Angeles

# Fix timezone
RUN ln -fs /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone

# Use the system pip to install requirements into the NGC-optimized environment
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

# Ensure the Jupyter kernel uses the optimized NGC python path
RUN python3 -m ipykernel install --user \
    --name tf-ngc \
    --display-name "TensorFlow NGC (Blackwell)"