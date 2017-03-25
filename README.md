# dockerfiles

```sh
% cd base
% docker build -t otoyo/base .
```

```sh
% cd elixir
% docker build -t otoyo/elixir .
% docker run --name CONTAINER_NAME -p HOST_PORT:GUEST_PORT -it otoyo/elixir
```
