<p align="center"> <a href="variaveis_6.md"> << Meu troco, meu troquinho </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_8.md"> Próximo >> </a> </p>


A partir daqui, irei aproveitar o conhecimento obtido no capítulo anterior. As variáveis que são ``signed`` serão declaradas sem a palavra ``signed``.

# Octal

Para usar variáveis com valores em octal, basta criarmos uma variável e atribuir o valor em octal que desejamos.

```c
#include <stdio.h>

int main(void)
{
	int	octal_var;

	octal_var = 014; // Adicionando o valor 12(em decimal)
	printf("O número em octal é: %o\n", octal_var);
	printf("O número em octal é: %o\n", octal_var + 026); // Realizando uma soma em octal (apenas como exemplo)
}
```

Não existe um tipo específico que funciona apenas em octal, ou que funcione apenas em hexadecimal.

Por isso que colocamos o especificador no printf, assim ele imprime o valor na base correta. Seja octal, ou hexadecimal.

```c
#include <stdio.h>

int main(void)
{
	int	hexadecimal_var;

	hexadecimal_var = 0xc; // Adicionando o valor 12(em decimal)
	printf("O número em hexadecimal é: %x\n", hexadecimal_var);
	printf("O número em hexadecimal é: %x\n", hexadecimal_var + 0xa3b); // Realizando uma soma em hexadeximal (apenas como exemplo)
}
```

Como pode ser visto. O código funciona sem problemas.

Um lembrete é que octal e hexadecimal são entendidos com variáveis ``unsigned int`` pelo printf. Mas como os números não são maiores que 2 bilhões, a gente não vai ter prints estranhos.

Isso pode ser feito se temos certeza que nosso código nunca vai processar algo gigantesco e que poderia gerar erros. Pois, facilita na escrita e a gente já tem uma ideia do resultado esperado.

Por fim, mas não menos importante, vamos falar do tipo de variável que suporta textos.

<p align="center"> <a href="variaveis_6.md"> << Quero um ponto a mais na vida </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_8.md"> Texto, textinho, textão >> </a> </p>
