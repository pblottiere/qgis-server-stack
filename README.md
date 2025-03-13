# qgis-server-stack

:warning: THIS IS A MINIMAL TESTING ENVIRONMENT FOR QGIS SERVER DEPLOYMENT, DO NOT USE IN PRODUCTION

Deployment examples:

- `docker-compose`: offers a basic yet complete example for deploying a QGIS
  Server stack, covering everything from the caching mechanism to the web
  client, using Docker Compose.


## docker-compose

![alt text](mviewer.png "mviewer")

QGIS Server stack example:
  - cache: [MapProxy](https://mapproxy.org/)
  - load-balancer: [NGINX](https://www.nginx.com/)
  - web client: [mviewer](https://mviewerdoc.readthedocs.io/fr/stable/)
  - composition: `docker-compose`

```` console
$ docker-compose up --scale qgisserver=2 -d
````

Then:
  - 2 instances of QGIS Server are running
  - cached data is in `mapproxy/cache_data/countries_cache_EPSG3857`
  - web client is available on http://localhost:8080/
