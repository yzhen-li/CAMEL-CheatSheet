## Access jupyter notebook remotely
### server side
    $ jupyter notebook --no-browser --port=XXXX
### local side
    $ ssh -N -f -L localhost:YYYY:localhost:XXXX serveruser@serverhost
start a browser and use `localhost:YYYY` as entry point
### Reference: https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/
