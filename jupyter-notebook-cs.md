## Access jupyter notebook remotely

### server side

- start server
    $ jupyter notebook --no-browser --port=XXXX
    
- list servers
    $ jupyter notebook list

- kill servers
-- get PID
    $ lsof -n -i4TCP:[port-number]
-- kill by PID
    $ kill -9 [PID]

### local side
    $ ssh -N -f -L localhost:YYYY:localhost:XXXX serveruser@serverhost
start a browser and use `localhost:YYYY` as entry point. please note that one needs to reestablish the connection using above command if there is any break or reconnection or change of local network settings.

### Reference
https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/
