```C runnable
/*********************************************************************
* ficheiros2.c														 *
* Programa com manipulação de ficheiros para leitura e escrita		 *
* 																	 *
*********************************************************************/

#include <stdio.h>

int main() {
	
	FILE *fp1, *fp2;
	
	fp1 = fopen("ficheiro1.txt","r");
	fp2 = fopen("ficheiro2.txt","w");
	
	fclose(fp1);
	fclose(fp2);

	return 0;
}
```



```C runnable
/*********************************************************************
* ficheiros3.c														 *
* Programa com a estrutura para manipulação de ficheiros em C 		 *
* e que abre ficheiro em modo leitura (r), e lê do ficheiro usando   *
* a função fscanf																	 *
*********************************************************************/

/*A função fprintf armazena dados num ficheiro. 
O seu funcionamento é muito semelhante ao da função printf. 
A diferença principal é a existência de um parâmetro com a informação do ficheiro onde os dados serão armazenados
(através da inidcação do nome do apontador para esse ficheiro).

Sintaxe: fprintf(nome_do_pontador_para_o_ficheiro, conteúdo a imprimir, com sintaxe semelhante ao printf)*/

#include <stdio.h>
#include <stdlib.h>

int main(void)
{
	FILE *fp; // cria variável apontador para ficheiro
	char palavra[20]; // variável do tipo string
	  
	//abrindo o ficheiro com tipo de abertura w - para permitir escrita (write)
	fp = fopen("ficheiro_palavra.txt", "r");
	  
	//testando se o ficheiro foi realmente criado
	if(fp == NULL)
	{
	printf("Erro na abertura do ficheiro!");
	return 1; //termina a execução e retorna erro
  }
  
	printf("Vou tentar ler do ficheiro... Aguarde\n");
	
	//lê do ficheiro (através do apontador fp) uma string e guarda-a na variável "palavra"
	fscanf(fp, "%s", &palavra); 
  
  	system("pause");
  	
	//usando fprintf para armazenar a string no arquivo
	printf("palavra lida do ficheiro: %s\n", palavra); //escreve a string guardada na variável "palavra" no ficheiro apontado por fp
  
	//usando fclose para fechar o ficheiro
	fclose(fp);
	  
	printf("Dados gravados com sucesso!");
	  
	return(0);
}

```
