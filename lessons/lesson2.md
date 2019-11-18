# Função fopen

Sempre que quisermos trabalhar com um ficheiro, o primeiro passo é abrir ou criar um ficheiro. Um ficheiro não passa de espaço na memória em que os dados são armazenados. Por forma a ganhar acesso aos elementos de um ficheiro, designado por um dado nome, é necessário "abri-lo", usando a função fopen, cujo protótipo está em stdio.h.

O protótipo da função é 

```C
FILE *fopen(const char *filename, const char *mode)
```

Para criar um ficheiro num programa 'C', devemos assim usar a seguinte sintaxe:

```C
FILE *fp;
fp = fopen ("file_name", "mode");
```

Na sintaxe acima, é criado um apontador para ficheiro (uma espécie de variável) definida na biblioteca padrão (no cabeçalho <stdio.h>), que tem que ficar com um nome associado (para futura referência no código, como outro tipo qualquer de variável)

fopen é uma função padrão usada para abrir um ficheiro.
filename é a string que contém o nome do ficheiro. Se for escrito no próprio programa, p.ex. "c:\temp\exp.txt" é necessário escrever "c:\\temp\\exp.txt", dado o significado especial de '\'.

Se o ficheiro não existir, será criado e aberto.
Se o ficheiro existir, será aberto diretamente usando esta função.
fp é um apontador para ficheiro que aponta para o ficheiro indicado e permite proceder a operações de leitura e/ou escrita sobre ele.

Sempre que abrimos ou criamos um ficheiro, é necessário especificar o que pretendemos fazer com o ficheiro (de que forma o queremos usar no nosso programa). Um ficheiro na programação em C pode ser criado ou aberto para fins de leitura / gravação. Um modo é usado para especificar se pretendemos usar o ficheiro para uma coisa ou outra (ou para as duas). A seguir, estão os diferentes valores de modos de abertura que podem ser usados no acesso a ficheiros na programação em C:


"r" - read. Abre o ficheiro para leitura. A função retorna NULL se o ficheiro não existir.Se um ficheiro estiver no modo de leitura, nenhum dado será apagado se o ficheiro já existir.
"w" - write. Abre o ficheiro para escrita, criando um novo ficheiro (e apagando um ficheiro que já existisse com o mesmo nome).
"a" - append. Semelhante a "w" mas apensando os dados escritos ao fim do ficheiro se este já existir.

A função retorna um apontador que é atribuído à variável de ficheiro.

É possível ainda acrescentar ao modo os seguintes caracteres:

+ - O ficheiro passa a ser aberto para leitura e escrita (p.ex. "r+"):
t - Indica que o ficheiro é de texto (acesso sequencial). Não é necessário usar este carácter porque, por omissão, os ficheiros são de texto.
b - Modo binário, permitindo acesso aleatório ao ficheiro.

O nome do ficheiro e o modo são especificados como cadeias de caracteres, portanto devem sempre ser escritos entre aspas.

Exemplo:

```C
#include <stdio.h>
int main() {
FILE *fp;
fp  = fopen ("data.txt", "w");
}
```
O ficheiro é criado na mesma pasta em que se encontre o ficheiro de código.
No entanto, se assim entendermos, podemos especificar o caminho em que desejamos criar ou abrir o ficheiro:

```C
#include <stdio.h>
int main() {
FILE *fp;
fp  = fopen ("D://data.txt", "w");
}
```
