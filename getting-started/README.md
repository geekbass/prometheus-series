# Getting Started - Pt 1
This contains the code and the commands for Pt 1 of my Blog series on my journey of Prometheus.

See Blog Here for more info:

### Confuring Docker Engine
Configure your Docker Engine for Prometheus metrics. Set daemon.json settings in your Docker Daemon. See instructions here for your version of Docker. 

### Run Prometheus Server in Docker
```sh
docker run -d --name prometheus -p 9090:9090 -v $PWD/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus
```

### Run Grafana in Docker
```sh
docker run -d --name grafana --link prometheus -p 3000:3000 grafana/grafana
```

