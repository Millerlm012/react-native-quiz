# pull base image
FROM node:latest

# set our node environment, either development or production
# defaults to production, compose overrides this to development on build and run
ARG NODE_ENV=development

RUN npm i --unsafe-perm -g npm@latest expo-cli@latest

WORKDIR /srv
COPY ./srv/ /srv
RUN rm -r node_modules && npm install

ENTRYPOINT ["npm", "start"]