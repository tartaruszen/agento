# agento

The agento project follows the idea extracted by [*Osmotic Computing: A New Paradigm for Edge/Cloud Integration, M. Villari, M. Fazio, S. Dustdar, O. Rana and R. Ranjan*](http://ieeexplore.ieee.org/document/7802525/). It presented the Osmotic Computing in 2016 as a new promising paradigm for the integration between a centralised Cloud layer and Edge/Internet of Things (IoT) layers; whereas its basic principles and enabling technologies were presented in [*Towards Osmotic Computing: Looking at Basic Principles and Technologies, M. Villari, A. Celesti, M. Fazio*](https://link.springer.com/chapter/10.1007/978-3-319-61566-0_86).

## Why agento?
todo


## Getting Started

The instructions below will get you a copy of the project on your local machine for developing and testing.

### Installing

The *requirements.txt* file includes all the project python dependencies.
```bash
$ pip install -r requirements.txt
```

### Running the web server

The following commands will help you to start the web service.

```bash
$ export FLASK_APP=restful.py
$ flask run
```

### How to use it
```bash
$ curl -i -X PUT \
-H "Content-Type: application/json" \
-d '{"time":2, "source":"guest"}' \
http://localhost:5000/api/v1/monitor/mem
```

```bash
$ curl -i -X DELETE \
-H "Content-Type: application/json" \
-X DELETE -d '{"source":"guest"}' \
http://localhost:5000/api/v1/monitor/mem
```

```bash
$ curl -i -X PUT \
-H "Content-Type: application/json"  \
-d '{"image":"redis","port":"","name":"some-redis","host":"","volume":"","privileges":"","command":""}' \
http://localhost:5000/api/v1/deploy
```

```bash
$ curl -i -X DELETE \
-H "Content-Type: application/json"  \
-d '{"name":"some-redis", "image":"redis"}' \
http://localhost:5000/api/v1/deploy
```

## RESTful APIs list
todo