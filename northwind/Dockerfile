FROM registry.access.redhat.com/ubi8/nodejs-16-minimal:1

WORKDIR /opt/app-root/src

COPY package.json /opt/app-root/src
RUN npm install --only=prod
COPY server /opt/app-root/src/server
COPY public /opt/app-root/src/public

ENV NODE_ENV production
ENV PORT 8081

EXPOSE 8081

CMD ["npm", "start"]
