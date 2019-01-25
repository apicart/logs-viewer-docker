<h1 align="center">
  Logs Viewer
  <br>
  (docker image)
  <br>
  <a href="https://cloud.docker.com/repository/docker/apicart/logs-viewer/general">
    <img alt="" src="https://img.shields.io/docker/pulls/apicart/logs-viewer.svg">
  </a>
</h1>

This image is for the [apicart/logs-viewer](https://github.com/apicart/logs-viewer) package.

## Installation
Minimal configuration for Docker Compose file

1. Create a `docker-compose.yml` file with the following content.
```yaml
version: "3"
services:
    logs-viewer:
        image: "apicart/logs-viewer"
        container_name: "logs-viewer"
        working_dir: "/var/www"
        volumes:
            - "./external-logs:/var/www/var/external-logs"
        ports:
            - "80:80"

```
2. Run `docker-compose up`.
3. The Logs Viewer should be now accessible from [http://localhost](http://localhost).
4. Direct your logs into the external-logs directory on your machine.
5. In case that files cannot be created in the external-logs directory because of the "access denined error" run for example the `chmod -R 777 external-logs` command (the level of privileges is up to you).
