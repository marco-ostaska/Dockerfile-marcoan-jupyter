# Supported tags and respective Dockerfile links

* `latest`, `jupyter-5.6.0`, `dashboard`

# Considerations

* Container built on Debian 9 Slim with [miniconda3](https://conda.io/miniconda.html) packed with python3.6, [jupyter notebook (v 5.6.0)](http://jupyter.org/) and [jupyter dashboard](https://jupyter-dashboards-layout.readthedocs.io/en/latest/)

* the idea here was to have an easy jupyter container, just to type `localhost:port` in the web browser, no token or password needed
  * The container will start jupyter with this command:
  ```
  jupyter notebook --ip="*" --allow-root --no-browser --NotebookApp.token=
  ```

* I use to start the container this way:
```
docker run -d -p 8888:8888 -v $(pwd):/jupyter_files marcoan/jupyter:dashboard
```
