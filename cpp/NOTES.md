## COMPILING

In order to compile stuff with opencv, you need to add the argument (including backticks)

`pkg-config --cflags --libs opencv4`

to your compile commad.

Ex:
```
g++ -o foo `pkg-config --cflags --libs opencv` foo.cpp
```
