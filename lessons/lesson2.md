9.1.2 Abertura de ficheiro

Por forma a ganhar acesso aos elementos de um ficheiro, designado por um dado nome, é necessário "abri-lo", usando a seguinte função cujo protótipo está em stdio.h:

 

FILE *fopen(const char *filename, const char *mode)

 

filename é a string que contém o nome do ficheiro. Se for escrito no próprio programa, p.ex. "c:\temp\exp.txt" é necessário escrever "c:\\temp\\exp.txt", dado o significado especial de '\'. Se for lido do teclado não há problema.

mode é o modo de abertura e pode ter os valores:
"r" - read. Abre o ficheiro para leitura. A função retorna NULL se o ficheiro não existir.
"w" - write. Abre o ficheiro para escrita, criando um novo ficheiro (e apagando um ficheiro que já existisse com o mesmo nome).
"a" - append. Semelhante a "w" mas apensando os dados escritos ao fim do ficheiro se este já existir.

A função retorna um apontador que é atribuído à variável de ficheiro.

É possível ao modo acrescentar ainda os seguintes caracteres:

 

+ - O ficheiro passa a ser aberto para leitura e escrita (p.ex. "r+")
t - Indica que o ficheiro é de texto (acesso sequencial). Não é necessário usar este carácter porque, por omissão, os ficheiros são de texto.
b - Modo binário, permitindo acesso aleatório ao ficheiro.
