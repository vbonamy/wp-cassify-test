FROM node:21-alpine

RUN npm install -g selenium-side-runner

WORKDIR /root

CMD selenium-side-runner -s http://selenium-chrome:4444 /test-sides/01-wp-cassify-setup.side && selenium-side-runner -s http://selenium-chrome:4444 /test-sides/02-wp-cassify-cas-login.side
