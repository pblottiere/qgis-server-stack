# qgis-server-stack

WARNING: THIS IS A MINIMAL TESTING ENVIRONMENT, DO NOT USE IN PRODUCTION

QGIS Server stack example:
  - cache: [MapProxy](https://mapproxy.org/)
  - load-balancer: [NGINX](https://www.nginx.com/)
  - web client: [mviewer](https://mviewerdoc.readthedocs.io/fr/stable/)
  - composition: ``docker-compose``

```` bash
$ docker-compose up --scale qgisserver=2 -d
````

Then:
  - 2 instances of QGIS Server are running
  - cached data is in ``mapproxy/cache_data/countries_cache_EPSG3857``
  - web client is available on http://localhost:8080/
