# Vulhub - Docker-Compose files for creating vulnerable environments

Vulhub is an open source vulnerability target for the general public. Without extensive knowledge of docker, you can compile and run a vulnerable application image simply by executing two commands.

## Installation
Install docker/docker-compose on ubuntu 16.04:

```bash
# Install pip
curl -s https://bootstrap.pypa.io/get-pip.py | python3

# Install the latest version of docker
curl -s https://get.docker.com/ | sh

# Start the docker service
service docker start

# Install docker-compose
pip install docker-compose
```

Installation of Docker/Docker-Compose may be slightly different on other operating systems. Please refer to the [Docker documentation](https://docs.docker.com/) for other installation methods.

## Usage

```bash
# Pull project
git clone https://github.com/vulhub/vulhub-en.git
cd vulhub-en

# Enter a directory of a vulnerability/environment
cd flask/ssti

# Automated environment compilation
docker-compose build

# Start the environment
docker-compose up -d
```

There is corresponding documentation in each environment directory, please read the README.md file for information on vulnerability/environment setup and testing.

After the test is complete, delete the environment

```
docker-compose down
```

 It is recommended that you purchase a VPS with at least 1GB of memory to build vulnerability test environments. The `your-ip` mentioned in the documentation refers to the IP address of your VPS. If you are using a virtual machine to build a test environment, `your-ip` refers to your virtual machine IP, not the IP inside the docker container.

**All environments in this project are for testing purposes only and should not be used as a production environment!**

## Notice

Precautions:

1. To prevent permission errors, it is best to use the root user to execute the docker and docker-compose commands.
2. Docker partial image does not support running on machines such as ARM

## Contribution

This project relies on docker. Any exceptions that occur during compilation and running are thrown by docker and related programs. Please find the cause of the error yourself.

If it is determined that the Dockerfile is written incorrectly (or the code is wrong in vulhub), then [submit an issue](https://github.com/vulhub/vulhub/issues). For further help with compilation errors, please refer to [this documentation](https://github.com/GlitchWitchIO/vulhub-en/wiki/compilation).

Thanks list：[Contributors List](contributors.md)

## License

Vulhub is released under the [GPL-3.0 license](LICENSE).

## Translation

This fork is the unofficial English translation of [vulhub/vulhub](https://github.com/vulhub/vulhub). It is maintained by [@GlitchWitchIO](https://github.com/GlitchWitchIO).
All non-translation related issues should be reported to the original repository.

Currently the translation is ![Progress](http://progressed.io/bar/1) complete
