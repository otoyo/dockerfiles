### Build Docker Image

```sh
% docker build -t otoyo/anaconda3 .
```

### Run Docker Container

```sh
% docker run --name anaconda3 -p 8888:8888 -it otoyo/anaconda3
```

### Start Jupyter Notebook

```sh
% jupyter notebook --ip=0.0.0.0 --allow-root
```
