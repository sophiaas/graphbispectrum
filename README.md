Graph Bispectrum
================

Use the bispectrum on the symmetric group to solve graph isomorphism.


## Setup

```bash
git clone git@github.com:sophiaas/graphbispectrum.git
cd graphbispectrum
virtualenv env
. env/bin/activate
pip install cython
pip install -r requirements.txt
python setup.py build_ext --inplace
nosetests -s tests
deactivate
```

## Docker

A `Dockerfile` and a `docker-compose.yml` are included in the root of the repo.

```bash
docker-compose build
docker-compose run graphbispectrum bash
```
 
 This should give you an interactive shell inside the container.
 The code is mounted in the /code directory.

 ```bash
 cd /code
 python setup.py build_ext --inplace --force
 nosetests -s tests
 ```
