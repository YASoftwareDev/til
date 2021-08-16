If you really like to mess a bit your system (by installing packages from newer version).

https://stackoverflow.com/a/67453352/210971

```sh
sudo add-apt-repository 'deb http://mirrors.kernel.org/ubuntu hirsute main universe'
sudo apt install build-essential manpages-dev software-properties-common
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt update && sudo apt install gcc-11 g++-11
```

Just do not run `apt upgrade`, because you will get more packages that you like 
