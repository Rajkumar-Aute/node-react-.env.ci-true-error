# node-react-.env.ci-true-error
Node Build error - Stop Treating warnings as errors because process.env.CI = true

Error while building the code in node in docker container / CICD Pipeline

Node check Node version is compatability and dependannt packages in package.json

Solution

add CI=falce in the running command.

npm cache clean --force \
rm -rf node_modules package-lock.json \
npm install \
CI=false \ 
npm run build-dev
