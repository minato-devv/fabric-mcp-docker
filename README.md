# Installation 

```sh
git clone https://github.com/q8xj9gs8hs-a11y/fabric-mcp-docker.git # clone this repository
cd fabric-mcp-docker

mkdir -p "${HOME}/.fabric-config" # create the directory that will be mounted onto both containers

docker run -it --rm -v "${HOME}/.fabric-config:/home/appuser/.config/fabric" kayvan/fabric:latest --setup # install the patterns and strategies, choose a vendor and model

docker compose up -d # start both services
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
