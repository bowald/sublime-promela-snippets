Sublime Text Editor 2 / 3 - Promela Snippets
===========================================

Promela snippets for Sublime Text 2 / 3. This is **as of now not finished** and is intended for my personal use. However feel free to contribute or use the snippets how ever you like.



Install
-------

### Requirements

The snippets are binded to scope.promela, which means they are only active when you edit a promela file. The easiest way to add a promela scope to sublime is to install [corbanmailloux's](https://github.com/corbanmailloux) [promela_spin](https://github.com/corbanmailloux/sublime-promela-spin)

### Sublime Text 2 / 3 - Manual installation

Clone this repo into your Sublime package folder.
On Mac the default path is: ```/Users/YOUR_USERNAME_HERE/Library/Application Support/Sublime Text 3/Packages/```


Snippets
--------

### [apr] active proctype function

```c
active proctype ${1:p}() {
  ${2:/*body...*/}
}
```


### [at] atomic

```c
atomic {
  ${1:/*body...*/}
}
```


### [de] definition

```c
#define ${1:name} ${2:value}
```


### [do] do loop

```do
do
  :: ${1:condition} -> ${2:break}
  :: ${3:else} -> ${4:loop}
od
```


### [if] if

```c
if
  :: ${1:condition} -> ${2:something}
  :: ${3:else} -> ${4:stuff}
fi
```


### [in] init

```c
init {
  ${1:/*body...*/}
}
```


### [ina] init used for starting processes

```c
init {
  atomic {
    ${1:/*body...*/}
  }

  _nr_pr == 1 -> ${2:assert($3:condition)}
}
```

### [inl] Inline function

```c
inline ${1:name} (){
  ${2:/*body...*/}
}
```


### [pf] print

```c
printf("${1:msg}${2:\n}");
```


### [pr] Proctype block

```c
proctype ${1:p}() {
  ${2:/*body...*/}
}
```

License
-------

Copyright 2015, Johan Bowald  <johan@bowald.se>

MIT