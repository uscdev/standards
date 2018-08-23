# Docker container standards

1. `uscdev/centos` shoudld be your base container if at all possible.

2. Always do a full patch on your container (in your Dockerfile): `RUN yum update && yum upgrade`

3. Have a healthcheck page at `/unprotected/health.html` for any web servers. The page should return:

````
<html>
<body>
Okay
</body>
</html>
````

4. Have a docker healthcheck (in your Dockerfile):

````
HEALTHCHECK CMD curl -f http://localhost/unprotected/health.html || exit 1
````

