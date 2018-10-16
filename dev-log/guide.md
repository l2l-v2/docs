# Developement Log
## Start RabbitMQ with Docker
Please ensure that you have install docker on your PC.
```bash
# Get image from pub repository
docker pull rabbitmq:management
# Run a rabbitmq instance
docker run -d --hostname my-rabbit --name rabbit -p 5672:5672 -p 15672:15672 rabbitmq:management
# Log in to rabbitmq client in browser
url : localhost:15672
usr:pwd -->guest:guest
```
## Intergration activiti cloud with JHipster.
- A bug related to swagger2 is reported as follow:
```bash
Caused by: java.lang.IllegalStateException: Multiple
 Dockets with the same group name are not supported.
  The following duplicate groups were discovere......
```
  - Exclude `io.springfox`dependencies and only keep them imported from `org activiti.cloud` , the bug seems  to have been fixed.
