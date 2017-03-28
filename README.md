# zedrem

The purpose of this container is to enable editing files that are located within the volumes of a container using [zed](http://zedapp.org/). 

Provided you had a container called `mycontainer`, exporting `/myvolume`, the following command would contact the main rendez-vous [server](wss://remote.zedapp.org:443):

    docker run -it --rm --volumes-from mycontainer efrecon/zedrem /myvolume
    
It would then print out something similar to the following in the terminal, and you should then be able to edit the files in `mycontainer`:

```
In the Zed application copy and paste following URL to edit:

  https://remote.zedapp.org:443/fs/da2d36e2da4d4c9e9d159d74855b5688

Press Ctrl-c to quit.
```
