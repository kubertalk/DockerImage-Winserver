# DockerImage-Winserver

```
$host-code-add = c:/xxx/code
$container-code-add = c:/code
docker build -t win-vs .
docker run -it -v $host-code-add:$container-code-add win-vs
```
Copy your code files to your $host-code-add,
Go into your container's code address $container-code-add,
```
cl ./hello.cpp \EHsc
./hello
```
You can see "Hello World!" in your screen.

```docker save win-vs -o $shared-server-add\win-vs.tar```

```docker load -i $shared-server-add\win-vs.tar```

