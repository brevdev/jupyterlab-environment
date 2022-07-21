
Welcome! everything inside of the `work` directory will be preserved, but files created outside this directory will be lost when the server resets. Enjoy using our environment and reach out to our discord for support https://discord.com/invite/qV6CsUjnZ2

## Quickstart 

run brev start on this repo to create a jupyterlab-environment 

```sh
$ brev start https://github.com/brevdev/jupyterlab-environment
```

which has an output similar to 
```
Name flag omitted, using auto generated name: jupyterlab-environment
Workspace is starting. This can take up to 2 minutes the first time.

name jupyterlab-environment
template 4nbb4lg2s ubuntu
resource class 2x8
workspace group brev-test-brevtenant-cluster
You can safely ctrl+c to exit
⣽  workspace is deploying
```


port forward your environment to localhost with

```sh
$ brev port-forward jupyterlab-environment -p 8888:8888
```


then navigate to [http://127.0.0.1:8888/lab?token=mysecretpassword](http://127.0.0.1:8888/lab?token=mysecretpassword)
to access your environment.

This page will sometimes take a while to load. 


## View jupyter notebook logs 

access the shell on your workspace with the `brev shell` commmand 

```sh
$ brev shell jupyterlab-environment 
...
➜  jupyterlab-environment git:(main) ✗ 
```

then print the logs using `docker logs`

```
➜ docker logs jupyterlab
```

to follow log output add the `-f` flag

```
➜ docker logs -f jupyterlab
```
