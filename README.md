# Python wats

```python
>>> a = 1,
>>> print(a)
(1,)
```

# C wats

`0xap0` equals `10f`

`$` is a valid identifier

`void typedef oops;` is valid

```c
struct $ {
    struct $ *$[0];
} typedef $;

a($ a[*], $ b[1][*]);
a($ a[42], $ b[~-1][*]);
a($ a[*], $ b[0][24]);

a($ a[42], $ b[0][24]) {
    printf("%d\n", sizeof(a));
    printf("%d\n", sizeof(b[0]));
}

main() {
    a(0, 0);
}
```

 - compiles with `{gcc,clang} --std=c99`
 - changing array sizes in the definition of a keeps gcc happy but makes clang give up (gcc is wrong here)
 - prints `sizeof(void*)` and 0
