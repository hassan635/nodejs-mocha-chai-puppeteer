# nodejs-mocha-chai-puppeteer
- Docker is the only pre-req.
- To execute, copy the content of this git repo on your local system.
- Then execute the following command after changing into that directory:
```bash
docker run --rm -it --name node-puppeteer-docker -v $PWD:/home/app -w /home/app -e "PORT=3000" -p 8880:3000  -u node buildkite/puppeteer /bin/bash
```

- Once inside the container, run the following command:
```bash
/home/app/node_modules/mocha/bin/mocha --timeout 15000 tests/ui_test.js
```
Enjoy!