to run docker within ubuntu container you need to mount the following directory
-v /var/run/docker.sock:/var/run/docker.sock
this way you can use host machine docker daemon ( docker daemon requires systemd but containers don't have systemd )

also add this option while making the container to avoid errors
--privileged=true
