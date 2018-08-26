# Supported tags and respective Dockerfile links

* `latest`, `jupyter-5.6.0`

# Considerations

* Container built on Debian 9 Slim with [miniconda3](https://conda.io/miniconda.html) packed with python3.6, [jupyter notebook (v 5.6.0)](http://jupyter.org/) and [jupyter dashboard](https://jupyter-dashboards-layout.readthedocs.io/en/latest/)


* I use to start the container this way:
```
docker run -d -p 8888:8888 -v $(pwd):/jupyter_files marcoan/jupyter-dashboard
```

* Jupyter can be started like this if you don't want to use a token or a password

```
jupyter notebook --ip="*" --allow-root --no-browser --NotebookApp.token=
```
