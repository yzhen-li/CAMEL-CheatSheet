## Access jupyter notebook remotely

### server side
    $ jupyter notebook --no-browser --port=XXXX

### local side
    $ ssh -N -f -L localhost:YYYY:localhost:XXXX serveruser@serverhost
start a browser and use `localhost:YYYY` as entry point. please note that one needs to reestablish the connection using above command if there is any break or reconnection or change of local network settings.

### Reference
https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/
