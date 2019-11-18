# Welcome!

This C template lets you get started quickly with a simple one-page playground.

```C runnable
/*********************************************************************
* ficheiros1.c														 *
* Programa com a estrutura básica para manipulação de ficheiros em C *
* (criação de apontador para o ficheiro, 							 *
* abertura do ficheiro com fopen() e fecho do ficheiro com fclose()) *
*																	 *
*********************************************************************/


#include <stdio.h>
#include <stdlib.h>

int main(void)
{
	// criando a variável apontador para o ficheiro (=file pointer)
	FILE *fp;
	
	//abrindo o ficheiro
	fp = fopen("ficheiro.txt", "w");
	
	// fechando o ficheiro
	fclose(fp);
	
	//mensagem para o utilizador
	printf("O ficheiro foi criado com sucesso!");
	
	system("pause");
	return(0);
}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), see the [official documentation](https://tech.io/playgrounds/408/tech-io-documentation).
