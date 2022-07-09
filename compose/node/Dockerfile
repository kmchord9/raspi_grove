FROM nodered/node-red

RUN npm install \
  node-red-dashboard \
  node-red-node-mysql \
  node-red-contrib-bme280 \
  node-red-contrib-grove-base-hat

USER root

RUN apk add python3-dev

RUN pip3 install \
    wheel \
    rpi.gpio

RUN git clone https://github.com/Seeed-Studio/grove.py && \
    cd grove.py && \
    pip3 install .

WORKDIR /usr/src/node-red

RUN clone https://github.com/Seeed-Studio/Seeed_Python_DHT.git && \
    cd Seeed_Python_DHT && \
    pip3 install .

CMD ["node-red"]
