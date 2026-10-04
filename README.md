# packing-flask-with-docker

> A minimal Flask date-and-time endpoint packaged in Docker.

## Overview

The Flask app returns a greeting with the server’s current date and time. A Dockerfile builds the app image and exposes the application on port 5000.

## What’s in this repo

- A single `/` route
- Container build and run files
- Optional timezone handling depends on the installed packages

## Stack

Python, Flask, Docker.

## Getting started

1. Build the image from the repository root: `docker build -t flask-clock .`.
2. Run it with `docker run --rm -p 5000:5000 flask-clock`.
3. Open `http://localhost:5000` in a browser.

## Notes

The displayed time comes from the container host’s clock. This is a small deployment-learning example, not a production time service.
