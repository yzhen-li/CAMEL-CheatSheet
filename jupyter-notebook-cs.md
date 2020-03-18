## Access jupyter notebook remotely

### server side

- start server
```bash
$ jupyter notebook --no-browser --port=XXXX
````
    
- list servers
````bash
$ jupyter notebook list
````

- kill servers
    1. get PID
    ````bash
    $ lsof -n -i4TCP:[port-number]
    ````
    2. kill by PID
    ````bash
    $ kill -9 [PID]
    ````

### local side
````bash
$ ssh -N -f -L localhost:YYYY:localhost:XXXX serveruser@serverhost
````
start a browser and use `localhost:YYYY` as entry point. please note that one needs to reestablish the connection using above command if there is any break or reconnection or change of local network settings.

### Reference
https://ljvmiranda921.github.io/notebook/2018/01/31/running-a-jupyter-notebook/
