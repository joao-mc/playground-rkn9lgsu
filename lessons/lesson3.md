```C runnable
/*********************************************************************
* ficheiros3.c														 *
* Programa com a estrutura para manipulação de ficheiros em C 		 *
* e que abre ficheiro em modo escrita (w), e escreve no ficheiro 	 *
* usando a função fprintf() 										 *
*																	 *
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
	fp = fopen("ficheiro_palavra.txt", "w");
	  
	//testando se o ficheiro foi realmente criado
	if(fp == NULL)
	{
	printf("Erro na abertura do ficheiro!");
	return 1; //termina a execuçã e retorna erro
  }
  
	printf("Escreva uma palavra para testar gravacao no ficheiro: ");
	scanf("%s", palavra); //lê do stdin (teclado) uma string e guarda-a na variável "palavra"
  
	//usando fprintf para armazenar a string no arquivo
	fprintf(fp, "palavra introduzida: %s\n", palavra); //escreve a string guardada na variável "palavra" no ficheiro apontado por fp
  
	//usando fclose para fechar o ficheiro
	fclose(fp);
	  
	printf("Dados gravados com sucesso!");
	  
	return(0);
}
```
