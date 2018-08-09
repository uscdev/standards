# Software Development Standards

# Methodology
12 Factor - https://12factor.net/

Language Preferences:
1. Javascript (Typescript or Kotlin are preferred)
2. Java

## Version Control
Git
1. github.com
2. github.usc.edu (GitHub Enterprise)

## Continious Integration Tool
1. Jenkins (jenkins.docker.usc.edu = On-prem, jenkins.cloud.usc.edu = AWS)

## Code Repo (maven/gradle, Docker, raw)
1. Nexus (nexus.docker.usc.edu / nexus.cloud.usc.edu)
Docker registry access: Anonymous = dtr.*   Write access = registry.*

## Packaging
1. Docker

## Orchestration Engine
1. Docker Swarm
2. [Communicating with the Swarm](swarm-communication.md)

## Design, Coding, and Deployment Standards

### Coding style guide
We follow the Google Style guides:
#### Javascript
https://google.github.io/styleguide/javascriptguide.xml
#### Java
https://google.github.io/styleguide/javaguide.html
#### HTML/CSS
https://google.github.io/styleguide/htmlcssguide.html

### Unit testing
- JUnit
- Karma + Jasmine

### Code Quality
- Sonarcube
- 100% Code coverage
- 100% Style compliance
IDEA plugin - http://code.google.com/p/google-styleguide/

### GUI Testing
- Selenium

### Load Testing
- JMeter

### Health Check
- Docker Health Check
- Please include an external health check page for nagios and load balancer http://xyz.usc.edu/unprotected/health.html

### Performance Monitoring
- TBA

### Authentication, Authorization, Attributes
Shibboleth
- Docker skeleton - https://github.com/uscdev/shib-service
- Docker proxy - https://github.com/uscdev/shib-proxy

### Declaration / template preferences
- docker compose

### Smart Reverse Proxy
- docker-flow-proxy - https://github.com/uscdev/compose/tree/master/docker-flow-proxy
- Client compose file - https://github.com/uscdev/compose/tree/master/hello-dual
