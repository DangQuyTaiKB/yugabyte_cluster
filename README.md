# Build a YugabyteDB cluster using Docker and Docker-Compose

This project introduces a build using Docker-Compose

## 1. Build a suitable Docker image

Refer to the IMAGE LAYERS of the YugabyteDB official image:
- Start the build from `almalinux:8` and then install the necessary dependencies.
- Download the YugabyteDB compressed package and unzip it, and run `post_install.sh` to install the dependencies required by YugabyteDB
- Expose the ports required by the YugabyteDB service


## 2. Use Docker-Compose to build a YugabyteDB cluster
A YugabyteDB consisting of 3 nodes is built, each node runs a `YB-Master` and a `YB-TServer`, and provides high-availability services through the Raft protocol.

The `docker-compose.yaml` file required for the build has been provided.

Start it with the following command:
``` bash
docker-compose up
```

After successful startup, you can access the UI interface at `localhost:17000` on your local machine.