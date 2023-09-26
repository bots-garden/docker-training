## Containerizing an app

```bash
git clone https://github.com/nigelpoulton/psweb.git
cd psweb
docker build -t test:latest .

docker images

docker run -d \
  --name web1 \
  --publish 8080:8080 \
  test:latest

```
