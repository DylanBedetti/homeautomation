FROM nodered/node-red

# RUN apt-get update && apt-get install -yq --no-install-recommends \
#   rpi.gpio \
#   python-dev \
#   python-rpi.gpio \
#   libatomic1 \
#   && apt-get clean && rm -rf /var/lib/apt/lists/*

# Defines our working directory in container
WORKDIR /usr/src/app

# This will copy all files in our root to the working  directory in the container
# COPY ./app ./

# server.js will run when container starts up on the device
CMD ["bash", "/usr/src/app/start.sh"]