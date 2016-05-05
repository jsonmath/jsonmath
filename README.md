### What is this
jsonmath is json tool. it very sample.


### Base function

> +

> \-

> *

> /

> \>

> <

> \><

> <\>

### function

@ave

### example

**demo1**

```
data: {'a':
  {
    'b1': {'c': true},
    'b2': {'c': false}
  }
}

formula: {"a.*": true}
result: {"a.*": {"a.b1": true}}
```

**demo2**

```
data: {'a':
  {
    'b1': {'c': 30},
    'b2': {'c': 60},
    'b3': {'c': 110}
  }
}

formula: {"a": {"><": ["*.c", 50,100]}}
result: {"a": {
  "><":{
    {"b2.c": 60}
}}

#---------------

formula: {"a": {"<>": ["*.c", 50,100]}}
result: {"a": {
  "<>":{
    {"b3.c": 110
  }
}}

```

**demo3**

```
data: {'a':
  {
    'b1': {'c': 30},
    'b2': {'c': 60},
    'b3': {'c': 110}
  }
}

formula: {'a.[].c': 30}
result: throw error

#---------------
formula: {'a.?[].c': 30}
result: {'a.?[].c': []}
```

**demo4**

```
rule: {"[]": {
  "@ave": "{}.a"
}}
data: [
  {"a": 5},
  {"a": 10},
  {"a": 15}
]
result: ["[]":{
"@ave({}.a)": 10
}]
```



