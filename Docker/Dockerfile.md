# Dockerfile Cheat-Sheet:

1. FROM: specifies the base image to use for the container.
2. RUN: runs a command in the container.
3. COPY: copies files from host to container.
4. ADD: similar to COPY, but also supports remote file URLs.
5. ENV: sets an environment variable in the container.
6. EXPOSE: specifies the ports that should be exposed by the container.
7. WORKDIR: sets the working directory for the container.
8. CMD: specifies the command to run when the container starts.
9. ENTRYPOINT: similar to CMD, but cannot be overridden by command line arguments.
10. USER: sets the user for the container.
11. VOLUME: creates a mount point for a volume in the container.
12. ONBUILD: triggers a command when the image is used as the base for another build.

Examples:

```
FROM python:3.8-alpine

COPY . /app
WORKDIR /app

RUN pip install -r requirements.txt

CMD ["python", "main.py"]
```

This example creates a container using the python:3.8-alpine image as the base. 
It copies the current directory to /app in the container, sets the working directory to /app, 
installs the dependencies listed in requirements.txt, and runs the command "python main.py" when the container starts.
