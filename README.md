# cli-tools-docker

## Information
```
A debian-based service containing a collection of various useful CLI tools/utilities containerized in 1 place.

The goal of this project/repository/service is to be a go-to all-in-one utility container where
you can just
    1. Startup container
        - Leave it running in the background
    2. When you need to use it
        - Jump into the container with 'docker exec -it [container-name] [shell]'
        - Execute command with the mounted volumes (if necessary) to share files
```

## Documentation
### Packages
+ python      : The python scripting/programming language interpeter
+ python-pip  : The python PyPI package manager
+ python-venv : Python virtual environment package
+ yt-dlp      : A fork of youtube-dl; A video downloader that was created for youtube but can work with other video platforms
+ gallery-dl  : An image downloader
+ spotdl      : Spotify Music Downloader that pulls from youtube (if exists)

## Wiki

### TODO-List and Pipeline
+ [] GitHub Actions and GitHub Container Repository (GHCR) support

## Resources

## References

## Remarks
