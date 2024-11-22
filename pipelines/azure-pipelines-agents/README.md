# Resources
- [Run a self-hosted agent in Docker](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker)

# Build and start the container

## Docker
Build: `docker build -t boinc/client -f Dockerfile.base-ubuntu .`
Run: `docker build --tag "azp-agent:linux" --file "./azp-agent-linux.dockerfile" .`

## Docker Compose
Docker Compose builds the image automatically if it doesn't exist.

Run: `docker compose --project-name azure-pipelines-agents --file ./compose.yml up --detach --remove-orphans`