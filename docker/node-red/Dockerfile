FROM nodered/node-red:3.0.2-14

WORKDIR /data

COPY package.json .
RUN npm install --unsafe-perm --no-update-notifier --no-fund --only=production --build-from-source

WORKDIR /usr/src/node-red