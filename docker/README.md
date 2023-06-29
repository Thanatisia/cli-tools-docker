# cli-tools Docker

## Setup
### Dependencies
+ docker
+ docker(-compose) : Optional; Not necessary as of the latest docker

### Pre-Requisites

### Installing

### Starting up
- Obtaining Image

- Manually Build Image
    ```console
    docker build -t thanatisia/cli-tools .
    ```

- Startup container
    - Using 'docker'
        ```console
        docker run -itd thanatisia/cli-tools
        ```
    - Using 'docker-compose'
        ```console
        docker-compose up -d
        ```

- Start container
    - Using 'docker'
        ```console
        docker start cli-tools
        ```
    - Using 'docker-compose'
        ```console
        docker-compose start
        ```

- Stop container
    - Using 'docker'
        ```console
        docker stop cli-tools
        ```
    - Using 'docker-compose'
        ```console
        docker-compose stop
        ```

- Shutdown container
    - Using 'docker'
        ```console
        docker rm cli-tools
        ```
    - Using 'docker-compose'
        ```console
        docker-compose down
        ```

- Restarting container
    - Using 'docker'
        ```console
        docker restart cli-tools
        ```
    - Using 'docker-compose'
        ```console
        docker-compose down && docker-compose up -d --build
        ```

- Executing commands
    - Using 'docker'
        ```console
        docker exec -it cli-tools /bin/bash -c "your-command"
        ```

## Wiki

## Resources

## References
+ [pythonspeed - Activate virtual environment in Dockerfile](https://pythonspeed.com/articles/activate-virtualenv-dockerfile/)

## Remarks

