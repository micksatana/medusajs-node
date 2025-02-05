This repository aims to help Medusa.js community to create production docker image based on Node.js latest LTS version

## How to build

Copy the `.dockerignore` and `Dockerfile` to a Medusa project folder.

Run docker build command

```sh
docker build -t medusajs-node:latest .
```

You can test run the image locally by injecting `.env` file.

```sh
docker run --rm -it --env-file=.env --network=host medusajs-node:latest
```

`--network=host` assuming you have Postgres installed and run either locally, or with a docker container which has its port exposed in the host network.
