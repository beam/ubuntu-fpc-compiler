***Pull builder image and compile transgui***

```
git clone https://github.com/transmission-remote-gui/transgui.git source-code
docker run -itv `pwd`/source-code:/source-code andrewbeam/ubuntu-fpc-compiler:19.10
>> make clean && lazbuild -B transgui.lpi && make && make zipdist
>> exit
ls source-code/Release
```

***Build own builder image and compile transgui***

```
git clone https://github.com/transmission-remote-gui/transgui.git source-code
docker-compose build ubuntu-fpc-compiler
docker-compose run ubuntu-fpc-compiler
>> make clean && lazbuild -B transgui.lpi && make && make zipdist
>> exit
ls source-code/Release
```
