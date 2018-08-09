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
ssh -NL localhost:2377:/var/run/docker.sock -i C:\Users\dcorley\workspace\secrets\secrets\keys\aws\ssh\usc\its-bsa-dev-1-us-west-2.pem docker@ec2-35-161-99-138.us-west-2.compute.amazonaws.com

or

ssh -NL localhost:2374:/var/run/docker.sock -i its-bsa-dev-1-us-west-2.pem docker@manager.swarm.usc.edu
````
