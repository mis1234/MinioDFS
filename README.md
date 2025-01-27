# Start Setting Up

0. Install Docker for Ubuntu 24.04

```bash
sudo apt-get update && sudo apt upgrade -y
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

1. Git clone the repository

2. Make sure that /mnt/data is available

```bash
test -d "/mnt/data" && echo "Directory exists" || echo "Directory does not exist"
```

3. Create your own configuration

```bash
cp .env.sample .env
nano .env
```

```bash
cp minio.env.sample minio.env
nano minio.env
```

4. Enable Docker on startup

```bash
sudo systemctl enable docker
```

5. Start the container

```bash
docker compose up -d
```