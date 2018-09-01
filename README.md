# arm32v7-debian-qemu

The official arm32v7/debian image extended with qemu-arm-static. See [Dockerfile](Dockerfile).

Allows for building images for ARM on x86. Linux and macOS supported.

## Instructions

1. Register the QEMU build agent:

    ```
    docker run --rm --privileged multiarch/qemu-user-static:register --reset
    ```

2. Extend this image and build as normal

    ```
    FROM jgogstad/arm32v7-debian:jessie
    
    CMD ["bash"]
    ```
