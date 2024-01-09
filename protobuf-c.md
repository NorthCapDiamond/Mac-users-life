# Protobuf-c 

## Way1. Using brew. !May not work! 
```
$ brew install protobuf-c
```

Example of error while using protobuf-c lib from brew:

fatal error: 'protobuf-c/protobuf-c.h' file not found

## Way2. Build it yourself:

- install additional libs:

```
brew install protobuf
brew install pkg-config
brew install autoconf
brew install automake
brew install libtool
```

- clone lib:

```
$ git clone https://github.com/protobuf-c/protobuf-c.git
$ cd protobud-c
```

- make/configure/test:

```
$ sudo ./autogen.sh && sudo ./configure && sudo make && sudo make install
$ make check
```
Docs for you: https://github.com/protobuf-c/protobuf-c

That's it for today)



