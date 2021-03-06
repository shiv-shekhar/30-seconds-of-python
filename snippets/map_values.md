---
title: map_values
tags: dictionary,function,intermediate
---

Creates a dictionary with the same keys as the provided dictionary and values generated by running the provided function for each value.

- Use `dict.keys()` to iterate over the dictionary's keys, assigning the values produced by `fn` to each key of a new dictionary.

```py
def map_values(obj, fn):
  ret = {}
  for key in obj.keys():
    ret[key] = fn(obj[key])
  return ret
```

```py
users = {
  'fred': { 'user': 'fred', 'age': 40 },
  'pebbles': { 'user': 'pebbles', 'age': 1 }
}

map_values(users, lambda u : u['age']) # {'fred': 40, 'pebbles': 1}
```
