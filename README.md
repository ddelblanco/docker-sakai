Docker Sakai
--------------------------
Docker setup for deploying the Sakai LMS

This work expands on the great work of the Hypothesis team and vbhayden to fix issues with the original repository and allow for targeted versions of Sakai during deployment.

### TL;DR
This is a Docker Compose deployment. You need Docker and Docker compose installed in your machine.


1. `git clone https://github.com/ddelblanco/docker-sakai`
2. `cd docker-sakai`
3. `git clone https://github.com/sakaiproject/sakai`
(Optional, change branch)
5. `sudo docker-compose up -d --build`

The first time this command is run the Docker image for Sakai will be built,
which can take 10 minutes or more. Additionally when the Sakai starts for the
first time it will spend several minutes initializing.

## Logging into Sakai

Once the Sakai container image has been built and the container is created,
you can access Sakai by browsing to http://localhost:8080/portal.

The default admin user is `admin` and the password is `admin`.

## Troubleshooting

If you have problems building or running the Docker container on macOS, you may
end to increase the memory allowance for Docker Engine up from the default of
2GB to 3GB or more.

This can be done in the "Advanced" section of Docker for Mac's Preferences UI.

## References

[Quick Start from Source](https://github.com/sakaiproject/sakai/wiki/Quick-Start-from-Source)
