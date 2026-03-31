# core

A generic data structures library written in pure C.

## Structures
- `string` — dynamic string type with a full API
- `array` — generic dynamic array
- `map` — generic dynamic map with type-erased keys and values

## Building
```bash
gcc core.c -o corelib
```

## Usage

### string
```c
string s = string_init(64);
string s2 = string_initd(64, "Hello, World!");

destroy_string(&s);
destroy_string(&s2);
```

### array
```c
array arr = array_init(8, sizeof(int));

array arr2 = array_initd(8, sizeof(int), (int[]){1, 2, 3, 4, 5});

int a = 8;
ainsert(&arr, &a);

destroy_array(&arr);
destroy_array(&arr2);
```

### map
```c
map m = map_init(8, sizeof(char), sizeof(int));

map m2 = map_initd(8, sizeof(char), sizeof(int),
    (char[]){'a', 'b', 'c'},
    (int[]){1, 2, 3});

destroy_map(&m);
destroy_map(&m2);
```

## License
MIT
