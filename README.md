# dockerfiles

```sh
% cd base
% docker build -t otoyo/base .
```

```sh
% cd mysql
% docker build -t mysql:5.7 .
% docker run --name mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:5.7
```

```sh
% cd elixir
% docker build -t otoyo/elixir .
% docker run --name CONTAINER_NAME --link mysql:db-mysql -p HOST_PORT:GUEST_PORT -it otoyo/elixir
```

## Golang

```sh
% docker run --name go -p 53000:3000 --security-opt=seccomp:unconfined --privileged -it otoyo/go
```
