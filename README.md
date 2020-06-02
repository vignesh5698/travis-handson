express cloud-native
cd cloud-native/
cat package.json 
npm install
sudo npm install
npm start
ls
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/Dockerfile
cat Dockerfile 
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/.dockerignore
docker build -t nodeserver -f Dockerfile 
docker build -t nodeserver -f Dockerfile .
sudo docker build -t nodeserver -f Dockerfile .
docker images 
sudo docker images 
docker run -i -p 3000:3000 -t nodeserver
sudo docker run -i -p 3000:3000 -t nodeserver
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/Dockerfile-tools
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/run-dev
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/run-debu
wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/run-debug
ls
nano run-dev 
nano run-debug 
docker build -t nodeserver-tools -f Dockerfile-tools .
sudo docker build -t nodeserver-tools -f Dockerfile-tools .
docker run -i -v "$PWD"/package.json:/tmp/package.json -v "$PWD"/node_modules_linux:/tmp/node_modules -w /tmp -t node:10 npm install
sudo docker run -i -v "$PWD"/package.json:/tmp/package.json -v "$PWD"/node_modules_linux:/tmp/node_modules -w /tmp -t node:10 npm install
docker run -i -p 3000:3000 -v "$PWD"/:/app -v "$PWD"/node_modules_linux:/app/node_modules -t my-nodejs-application-tools /bin/run-dev
docker run -i -p 3000:3000 -v "$PWD"/:/app -v "$PWD"/node_modules_linux:/app/node_modules -t nodeserver-tools /bin/run-dev
sudo docker run -i -p 3000:3000 -v "$PWD"/:/app -v "$PWD"/node_modules_linux:/app/node_modules -t nodeserver-tools /bin/run-dev

wget https://raw.githubusercontent.com/CloudNativeJS/docker/master/Dockerfile-run
sudo docker build -t nodeserver-run -f Dockerfile-run .


