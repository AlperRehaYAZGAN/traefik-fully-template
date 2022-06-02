### Traefik Wildcard and Regex Host
This is the repository for demonstrating Traefik wildcard and dynamically updatable host and reverse_proxy utilities with single line of code. In addition you can use Traefik AUTO LetsEncrypt SSL configuration. 

#### Usage
Setting up environment.  
```sh
# clone
git clone https://github.com/AlperRehaYAZGAN/traefik-wildcard-and-dynamic-config
cd traefik-dynamic-and-wildcard-config

# create volumes folder to attach access_logs and ssl configs
mkdir volumes 
mkdir volumes/traefik

# Change MY_DOMAIN.com to your custom domain in following files:
# - docker-compose.yaml
# - ./config/traefik-main.yaml
# - ./config/dynamic/traefik-dynamic.yaml

# set your custom static in file ./config/traefik-main.yaml
vim ./config/traefik-main.yaml

# set your custom dynamically changable env in file ./config/dynamic/traefik-dynamic.yaml
vim ./config/dynamic/traefik-dynamic.yaml
```  
  
Start API Gateway  
```sh
docker-compose up -d # wait to run.
curl localhost:80/ # bingo!
```


