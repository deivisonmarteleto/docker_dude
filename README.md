[![Docker Pulls](https://img.shields.io/docker/pulls/alexanderfefelov/dude.svg)](https://hub.docker.com/r/deivisonmarteleto/docker_dude)
[![Docker Stars](https://img.shields.io/docker/stars/alexanderfefelov/dude.svg)](https://hub.docker.com/r/deivisonmarteleto/docker_dude)
[![](https://images.microbadger.com/badges/version/alexanderfefelov/dude.svg)](https://microbadger.com/images/deivisonmarteleto/docker_dude)
[![](https://images.microbadger.com/badges/image/alexanderfefelov/dude.svg)](https://microbadger.com/images/alexanderfefelov/dude)

Just type

    docker run --name dude \
      --privileged \
      --detach \
      --volume /etc/localtime:/etc/localtime:ro \
      --publish 2211:2211 \
      --publish 2210:2210 \
      --publish 514:514/udp \
      alexanderfefelov/dude

and your Dude is ready. You can stop it with

    docker stop dude

and run it again with

    docker start dude
# docker_dude
