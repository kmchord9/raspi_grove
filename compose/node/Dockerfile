FROM nodered/node-red

RUN apk add python3-dev

RUN pip3 install \
    wheel

RUN git clone https://github.com/Seeed-Studio/grove.py && \
    cd grove.py && \
    pip3 install .


RUN npm install \
  node-red-dashboard \
  node-red-node-mysql \
  node-red-contrib-bme280 \
  node-red-contrib-grove-base-hat

USER root

CMD ["node-red"]
