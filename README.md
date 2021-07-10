# WordPress on Docker

## git clone

```
mkdir -p ~/containers/
cd ~/containers/
https://github.com/teityura/wordpress.git
cd wordpress/
```

## create .env

```
cat << EOF > .env
MYSQL_ROOT_PASSWORD="`cat /dev/urandom | base64 | fold -w 64 | head -n 1`"
MYSQL_PASSWORD="`cat /dev/urandom | base64 | fold -w 64 | head -n 1`"
EOF
```

## docker-compose up -d

```
docker-compose up -d
```

