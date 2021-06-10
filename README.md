# PlanetGram Tutorial 

This tutorial uses a Jupyter Notebook. 

I built this notebook in a docker environment, using an image recommended by https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html

## Setup

To use this notebook, run the following docker command:
```
docker run --rm\
  -p 8888:8888\
  -e JUPYTER_ENABLE_LAB=yes\
  -v "${PWD}":/home/jovyan/work\
  jupyter/datascience-notebook:33add21fab64
```

This will: Pull and build the `jupyter/datascience-notebook:33add21fab64` comprised of Python 3 and other scientific libraries, and start the jupyter webserver, port-forwarding local port 8888 to container port 8888.

Once the image has been pulled and built, you will see the following output: 
```
    To access the server, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/jpserver-6-open.html
    Or copy and paste one of these URLs:
        http://1e86a8c120c6:8888/lab?token= ... 
        http://127.0.0.1:8888/lab?token= ... 
```

Copy the URL starting with `http://127.0...` into your web browser, navigate to the `/work` directory and open the notebook called 'planet_gram.ipynb'.

## Next Steps
For my 'secret effect' I would have liked to create a sphere and map the image onto the sphere - but since I did not understand the code used in various online examples, I did not do this.  

I struggled to apply a color map to an image that was already in RGB format. I tried to do this for quite some time, but ultimately couldn't make it work and converted the image to greyscale prior to applying the color map. This worked, but left a somewhat unexplainable step in the tutorial. 

If this was something 'in the real world', I would like to lean less heavily on the PIL library, and discover and explain how these operations could be done using only the image raster and NumPy. Perhaps this is not necessary, but would be good mental exercise. 

