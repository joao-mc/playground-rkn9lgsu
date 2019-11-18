# Welcome!

This C template lets you get started quickly with a simple one-page playground.

```C runnable
#include <stdio.h>

int main() {
    FILE *fp;
    fp= fopen("file1.txt", "w");
    if(fp==NULL)
        printf("Erro na escrita do ficheiro\n");
	printf("Hello World!");
}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), see the [official documentation](https://tech.io/playgrounds/408/tech-io-documentation).
