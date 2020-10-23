# My Ubuntu Setup Manual

## Setup Jenkins from docker

1. install docker

[URL](https://qiita.com/tkyonezu/items/0f6da57eb2d823d2611d)

2. install docker-compose

[URL](https://qiita.com/mochizukikotaro/items/ae7ae1461ea4bf495bd0)

3. prepare docker-compose.yml

ex)

```
version: '3'

services:
  jenkins:
    image: 'jenkins:2.60.3'
    container_name: jenkins
    user: root
    restart: always
    ports:
      - '8080:8080'
      - '50000:50000'
    volumes:
      - ./data/jenkins:/var/jenkins_home
      - /var/run/docker.sock:/var/run/docker.sock
```

[URL](https://qiita.com/gymnstcs/items/e74f98774db45bfbc212)

4. build container

```
docker-compose -f jenkins-docker-compose.yml up
```

5. check localhost

```
http://0.0.0.0:8080
```

## Setup python

1. install pyenv

[URL](https://qiita.com/koooooo/items/b21d87ffe2b56d0c589b)

2. install python

ex) python 3.8.0

```
pyenv isntall 3.8.0
```

3. adjust python version

```
pyenv local 3.8.0
```

