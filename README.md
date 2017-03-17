# dockerfiles

```sh
% cd base
% docker build -t otoyo/base .
```

```sh
% cd dev
% docker build -t otoyo/dev .
% docker run --name CONTAINER_NAME -p HOST_PORT:GUEST_PORT -it otoyo/dev
```
