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



