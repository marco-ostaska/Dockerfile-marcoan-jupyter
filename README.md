# Supported tags and respective Dockerfile links

* `latest`, `miniconda3`, `notebook5.6.0`

# Contents

* Container built on Debian 9 Slim with [miniconda3](https://conda.io/miniconda.html) packed with python3.6 and [jupyter notebook (v 5.6.0)](http://jupyter.org/)

## Tips to start the Container

###### Starting jupyter notebook without Password or Token

```
docker run -p 8888:8888 -v $(pwd):/jupyter_files marcoan/jupyter-dashboard jupyter notebook --ip="*" --allow-root --no-browser --NotebookApp.token=
```

###### Starting jupyter notebook with jupyter generated token
```
docker run -p 8888:8888 -v $(pwd):/jupyter_files marcoan/jupyter-dashboard jupyter notebook --ip="*" --allow-root --no-browser
```

###### Starting jupyter notebook with self generated token
```
docker run -p 8888:8888 -v $(pwd):/jupyter_files marcoan/jupyter-dashboard jupyter notebook --ip="*" --allow-root --no-browser --NotebookApp.token=<yourtoken>
```
