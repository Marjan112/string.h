# string.h
Simple stb-style implementation of string in C.

# Usage
``` c
#include <stdio.h>

#define STRING_IMPLEMENTATION
#include "string.h"

int main() {
    String str = {0};
    string_append_cstr(&str, "Hello, World!");

    printf("%.*s\n", str.count, str.data); // 'str' is not null terminated

    string_append_null(&str);
    printf("%s\n", str.data); // 'str' is now null terminated

    string_free(&str);
    return 0;
}
```

# License
Licensed under MIT License, see the [LICENSE](./LICENSE) file.