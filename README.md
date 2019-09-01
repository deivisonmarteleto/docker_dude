
# Hello people!

This project is simple, the focus is to help small internet providers run "The dude" in their operations.

# This project has:

- The dude 4 beta3
- Telegram Integration


How simple is it to deploy dude?
---

    docker run --name dude \
      --privileged \
      --detach \
      --volume /etc/localtime:/etc/localtime:ro \
      --publish 2211:2211 \
      --publish 2210:2210 \
      --publish 514:514/udp \
      dmarteleto/docker_dude
      
      
---

and your Dude is ready. You can stop it with

    docker stop dude

and run it again with

    docker start dude

-----------------------------------------------------------------------------------------------------------------------------------------

# For pessistent mode
---
docker volume create dude_data
git clone https://github.com/deivisonmarteleto/docker_dude.git
cd docker_dude
docker-compose build
docker-compose up -d

---

# docker-compose.yml

---

version: '3.7'
    ports:
      - "2211:2211"
      - "2210:2210"
      - "514:514/udp"

NOTE: Admin and no password!
---

# Telegram Integration:
To automate messages sent by a Telegram bot. The process of BOT creation in Telegram needs to be accomplished, with the ID_chat and API data it can put into production.

---

c:/curl.exe --insecure https://api.telegram.org/botxxxxxxxxxxxxxxxxxxxxx/sendMessage -d chat_id=-xxxxxxx -d text="O servico [Probe.Name] no dispositivo [Device.Name] passou para o status [Service.Status] - IP=[Device.FirstAddress]"

---
