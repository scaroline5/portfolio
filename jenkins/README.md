# Jenkins

From inside the jenkins folder, run the command to build the image.

```
docker build -f Dockerfile.yml -t scaroline5/custom-jenkins .
```

Then, run the command to build the container. The environment variable **JENKINS_ADMIN_ID**  will create the "admin" user. Make sure to change **JENKINS_ADMIN_PASSWORD** value to a password of your preference.

```
docker run --name jenkins --rm -p 8080:8080 --env JENKINS_ADMIN_ID=admin --env JENKINS_ADMIN_PASSWORD=password scaroline5/custom-jenkins
```
