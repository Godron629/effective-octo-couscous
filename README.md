# PlanetGram Tutorial 

This tutorial uses a Jupyter Notebook. 

I built this notebook in a docker environment, recommended by https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html

To use this notebook, run the following docker command. 

```
docker run --rm\
	-p 8888:8888\
	-e JUPYTER_ENABLE_LAB=yes\
	-v "${PWD}":/home/jovyan/work\
	jupyter/datascience-notebook:33add21fab64
```

This will: Pull and build the `jupyter/datascience-notebook:33add21fab64` comprised of Python 3 and other scientific libraries, and start the jupyter webserver, port-forwarding local port 8888 to container port 8888.

Once the image has been pulled and built, navigate in your web browser to https://127.0.0.1:8888 to use the notebook called 'planet_gram.ipynb'.

