# cli-tools Docker

## Table of Contents
+ [Setup](#setup)
+ [Customization](#customization)
+ [Wiki](#wiki)
+ [Resources](#resources)
+ [References](#references)
+ [Remarks](#remarks)

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

## Snippets and Examples
- Using an installed utility in container
    - Using yt-dlp
        ```console
        docker exec -it cli-tools yt-dlp {options}
        ```
    - Using the python interpreter
        ```console
        docker exec -it cli-tools python {options}
        ```
    - Using the python-pip package manager
        ```console
        docker exec -it cli-tools pip
        ```
- Data Backup and Recovery
    - Backup
        - Backing up apt packages
            ```console
            docker exec -it cli-tools apt list --installed | tee -a /target/path/to/list.log
            ```
        - Backing up python packages (if you installed anything manually)
            ```console
            docker exec -it cli-tools pip freeze list | tee -a /target/path/to/list.log
            ```
    - Recovery
        - Notes
            + Please mount all package list files into the container before proceeding
        - Recovering/Re-installing all backed up apt packages from a file (using dpkg)
            ```console
            docker exec -it cli-tools xargs apt install < [packages-file-name]
            ```
        - Recovering/Re-installing all backed up python packages from a file
            ```console
            docker exec -it cli-tools pip install -Ur [package-file-name]
            ```

## Customization
### Project filesystem files and directories
- Directories
    + Virtual Environment: /opt/venv
    + Startup working directory: /usr/src/app

### Examples 
- docker
    - Run with volume mounts
        ```console
        docker run -itd -v "/path/to/[host-system-volume]:./[container-volume-name]" thanatisia/cli-tools 
        ```
- docker-compose
    - Mount Volumes
        - Syntax
            ```yaml 
            volumes:
                # [host-system-volume]:[container-volume]:[permissions]
                - "/path/to/[host-volume-name]:./[container-volume-name]`
            ```
        - For yt-dlp
            ```yaml
            volumes:
                # [host-system-volume]:[container-volume]:[permissions]
                - "/path/to/[host-volume-name]:./yt-dlp`
            ```

## Wiki

## Resources

## References
+ [pythonspeed - Activate virtual environment in Dockerfile](https://pythonspeed.com/articles/activate-virtualenv-dockerfile/)

## Remarks

