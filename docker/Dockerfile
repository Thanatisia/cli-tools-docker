# Dockerfile for CLI collection utilities service 'cli-tools'

## Using latest as base image
FROM debian:latest 

## Information

## Set Current Working Directory

## Update apt package manager and install packages
RUN DEBIAN_FRONTEND=noninteractive apt update -y && \
    apt upgrade -y && \
    apt install -y python3 && \
    apt install -y python3-pip && \
    apt install -y yt-dlp && \
    apt install -y gallery-dl 

## Setup and Manually compile from source those not in packages
