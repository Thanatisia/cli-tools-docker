# Dockerfile for CLI collection utilities service 'cli-tools'

## Using latest as base image
FROM debian:latest 

## Information

## Add Environment Variables
ENV VIRTUAL_ENV=/opt/venv
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

## Set Current Working Directory
WORKDIR /usr/src/app

## Copy required files
### Python pip package requirements
COPY ./dependencies/python/requirements.txt ./dependencies/python/requirements.txt

## Update and install packages 
### apt package manager
RUN DEBIAN_FRONTEND=noninteractive apt update -y && \
    apt upgrade -y && \
    apt install -y vim && \
    apt install -y git && \
    apt install -y python3 && \
    apt install -y python3-pip && \
    apt install -y python3-venv && \
    apt install -y yt-dlp && \
    apt install -y gallery-dl && \
    apt install -y ffmpeg

### Setup and Manually compile from source those not in packages

### Install python packages into a virtual environment using requirements.txt
RUN python3 -m venv $VIRTUAL_ENV && \
    $VIRTUAL_ENV/bin/pip install --upgrade pip && \
    $VIRTUAL_ENV/bin/pip install -Ur ./dependencies/python/requirements.txt

## Add Environment Variables after setup

## Execute Commands (decided by user/maintainer/author)

