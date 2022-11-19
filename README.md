# Inter-VM Telemetry

This is an initiation project for the STAR group in UC3M.

The aim of this project is to send telemetry data from one virtual machine
(in practice, a rocket) to another one (in practice, a base station) and
visualize the data through a web app.

## Project structure

The "virtual machines" will compose of docker containers for the sake of
reproducible builds. They are separated into two different containers:

#### `base_station`

This container will receive and display the data received from the `rocket` in
a web application.

#### `rocket`

This container will generate the data that will be sent to the `base_station`
to display.

## Running the project in docker

To run the project in the docker containers, you can execute

```bash
$ docker compose up --build
```

to build and run the containers. You can also omit the `--build` flag to not
build when not wanted.

It is recommended to run the projects individually during development to
avoid docker copy and build times.
