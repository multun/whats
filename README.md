# Python whats

```python
>>> a = 1,
>>> print(a)
(1,)
```

# C whats

`0xap-1` equals `5.0` (double), and is a single token

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


`int (*b);` declares a pointer to an int named b

# C++ whats

Thanksfully, C++ enables you to forward declare a templated sub templated class, later inheriting from its mother templated class.

```cpp
#include <iostream>

template<class T>
struct A {
    template<class U>
    struct B;

    static void lol() {
        B<int>{}.print();
    }
};

template<class T>
template<class U>
struct A<T>::B : A {
    static void print() {
        std::cout << "wtf" << std::endl;
    }
};

int main() {
    A<int>::lol();;
}
```
