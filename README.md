# DockerImage-Winserver

```
$host-code-addr = c:/xxx/code
$container-code-addr = c:/code
docker build -t win-vs .
docker run -it -v $host-code-addr:$container-code-addr win-vs
```
Copy your code files to your $host-code-addr,
Go into your container's code address $container-code-addr,
```
cl ./hello.cpp \EHsc
./hello
```
You can see "Hello World!" in your screen.

```docker save win-vs -o $shared-server-addr\win-vs.tar```

```docker load -i $shared-server-addr\win-vs.tar```

