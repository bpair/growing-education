FROM nodered/node-red-docker
RUN npm install node-red-contrib-aws-iot-custom-auth node-red-contrib-mysensors node-red-contrib-influxdb npm install node-red-node-serialport
COPY settings.js /data
ENV FLOWS=flows.json
ENV NODE_PATH=/usr/src/node-red/node_modules:/data/node_modules

CMD ["npm", "start", "--", "--userDir", "/data"]