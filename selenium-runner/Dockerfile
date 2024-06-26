FROM node:21-alpine

RUN npm install -g selenium-side-runner

WORKDIR /root

CMD selenium-side-runner -s http://selenium-chrome:4444 /test-sides/01-* \
    && selenium-side-runner -s http://selenium-chrome:4444 /test-sides/02-* \
    && selenium-side-runner -s http://selenium-chrome:4444 /test-sides/03-* \
    && selenium-side-runner -s http://selenium-chrome:4444 /test-sides/04-* \
    && selenium-side-runner -s http://selenium-chrome:4444 /test-sides/05-* \
    && selenium-side-runner -c "browserName=firefox" -s http://selenium-firefox:4444 /test-sides/05-* 