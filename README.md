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
array arr2 = array_initd(8, sizeof(int));

int x = 42;
ainsert(&arr, &x);

destroy_array(&arr);
```

### map
```c
map m = map_init(8, sizeof(string), sizeof(int));
map m2 = map_initd(8, sizeof(string), sizeof(int));

string key = string_initd(8, "health");
int value = 100;
minsert(&m, &key, &value);

destroy_map(&m);
```

## License
MIT
