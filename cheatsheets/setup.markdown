Installation
=============


Linux
----------
```
curl -sSL https://get.docker.com/ | sh
```

Windows
----------

1. Docker for Windows:
 https://www.docker.com/products/docker#/windows

1. Docker Toolbox:
 https://www.docker.com/products/docker-toolbox

Command Completion
------------------
```
wget https://raw.githubusercontent.com/docker/docker/master/contrib/completion/bash/docker -O ~/.docker-completion.sh
docker-compose --version (use version in next line, instead of 1.8.0)
wget https://raw.githubusercontent.com/docker/compose/1.8.0/contrib/completion/bash/docker-compose -O ~/.docker-compose-completion.sh
wget https://raw.githubusercontent.com/docker/machine/master/contrib/completion/bash/docker-machine.bash -O ~/.docker-machine-completion.sh
```

```
echo '. ~/.docker-completion.sh' >> ~/.bash_profile
echo '. ~/.docker-machine-completion.sh' >> ~/.bash_profile
echo '. ~/.docker-compose-completion.sh' >> ~/.bash_profile
```
