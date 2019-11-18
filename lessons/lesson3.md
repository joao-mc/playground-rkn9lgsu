9.1.3 Fecho de ficheiro
 

Logo que terminam as operações com um ficheiro é de boa norma "fechá-lo", o que acarreta a escrita de informação ainda pendente no "file buffer" e a libertação do espaço de memória deste.
O fecho de um ficheiro é efectuado com a seguinte função de stdio.h:

 

int fclose(FILE *f)

 

A função retorna 0 se bem sucedida e a constante simbólica EOF (-1) em caso de erro.

 

o           o          o

 

Esquema da sequência de operações com um ficheiro:

 

    FILE *f;

 

    f=fopen("filename","...");

            /* Operações de leitura e escrita, explicadas a seguir */

 

    fclose(f);
