# Installation 

```sh
# clone this repository
git clone https://github.com/q8xj9gs8hs-a11y/fabric-mcp-docker.git
cd fabric-mcp-docker


# create the directory that will be mounted onto both containers
mkdir -p "${HOME}/.fabric-config"
# install the patterns and strategies, choose a vendor and model
docker run -it --rm -v "${HOME}/.fabric-config:/home/appuser/.config/fabric" kayvan/fabric:latest --setup

# or if you already have the configuration files
cp ${HOME}/.config/fabric ${HOME}/.fabric-config


# start both services
docker compose up -d
```

Configure your `mcp.json`:

```json
{
  "mcpServers": {
    "fabric": {
      "url": "http://localhost:8000/message"
  }
}
```

# LICENSE

MIT
