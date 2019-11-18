Exemplo 1:

Apresentar o conteúdo de um ficheiro de texto assinalando as linhas que contenham o texto "printf". Indicar também o número total de linhas e o número de linhas com "printf".

'''C runnable
#include <stdio.h>
#include <stdlib.h>

#define MAX_BUF 120

int main(int argc, char* argv[])
{
	FILE *f;
	int n1=0;
	int n2=0;
	char filename[80];
	char buf[MAX_BUF];

	printf("Indique nome do ficheiro:");
	gets(filename);

	f=fopen(filename,"r");
	if (f==NULL) 
	{
		printf("Erro na abertura do ficheiro");
		return 1;
	}
	while (! feof(f)) 
	{
		fgets(buf,MAX_BUF, f);
		n1++;
		if (strstr(buf, "printf")>0) {
			n2++;
			printf("> %s", buf);
		}
		else
			printf("* %s", buf);
	}
	fclose(f);
	printf("\n\nO ficheiro tem %d linhas, das quais %d com \"printf\"\n",n1,n2);
	return 0;
}

'''
