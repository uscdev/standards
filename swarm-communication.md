# Communicating with the swarm

We use two methods to communicate with a swarm:

## 1 - Certificate bundle

Set docker variables:
````
export DOCKER_HOST=tcp://dcorley-swarm-mgr01.usc.edu:2376
export DOCKER_CERT_PATH=/home/yourname/path/client-certs
export DOCKER_TLS_VERIFY=1
````

Place certs in directory: `/home/yourname/path/client-certs`

## 2 - SSH Pipe

Set local docker variables
````
Linux:
export DOCKER_HOST=:2377
Windows
$Env:DOCKER_HOST = ":2377"
````

Create the pipe:
````
ssh -NL localhost:2374:/var/run/docker.sock -i its-bsa-dev-1-us-west-2.pem docker@manager.swarm.usc.edu
````
