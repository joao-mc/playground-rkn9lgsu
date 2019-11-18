Um ficheiro pode ser usado para armazenar um grande volume de dados persistentes. Como outras linguagens de programação, o C fornece funções de gestão e manipulação de ficheiros, nomeadamente para:

Criar um ficheiro
Abrir um ficheiro
Ler um ficheiro
Gravar um ficheiro
Fechar um ficheiro

A seguir são referidas as principais funções para manipulação de ficheiros na linguagem C:

Função	Para que serve
fopen ()	Para criar um ficheiro ou abrir um ficheiro existente
fclose ()	Para fechar um ficheiro
fprintf ()	Para escrever um bloco de dados num ficheiro
fscanf ()	Para ler um bloco de dados de um ficheiro
getc ()	Para ler um caracter dum ficheiro
putc ()	Para escrever um caracter num ficheiro
getw ()	Para ler um número intero dum ficheiro
putw ()	Para escrever um número inteiro num ficheiro
fseek ()	Para definir a posição do apontador para uma posição específica
ftell ()	Para retornar a posição atual dum apontador para ficheiro nesse ficheiro
rewind ()	Para colocar o apontador a apontar para o início do ficheiro

O tipo FILE

Para utilizar um ficheiro é necessário começar por declarar uma variável de tipo apontador para FILE (tipo definido em stdio.h):


FILE *f


Todas as operações com o ficheiro realizam-se usando esta variável.
