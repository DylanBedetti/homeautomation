version: '2'
volumes:
    
services:
  node-red:
    build: ./node-red
    volumes:
      - 'resin-data:/data'
    restart: always
    privileged: true
    network_mode: host
    labels:
      io.balena.features.supervisor-api: '1'
    cap_add:
      - SYS_RAWIO
    devices:
      - "/dev/mem:/dev/mem"
      - "/dev/gpiomem:/dev/gpiomem"
      - "/dev/i2c-1:/dev/i2c-1"
    ports:
      - 80:80