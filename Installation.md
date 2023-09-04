# Install Home Assistant Operating System

[DOWNLOAD THE APPROPRIATE IMAGE](https://www.home-assistant.io/installation/alternative/)



# Docker installation

```cmd
docker pull homeassistant/home-assistant

# docker run -d –name = homeassistant -v your_home_directory:/config –net=host homeassistant/home-assistant

docker run --name home-assist -p 8123:8123 -d homeassistant/home-assistant

docker ps -a
```
