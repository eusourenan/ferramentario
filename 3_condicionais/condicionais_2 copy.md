## O "if"

Anteriormente, aprendemos que o if é o meio com o qual começamos a dar ordens para o computador. Dizemos para ele: "Somente execute o código se essa condição for verdadeira".

Vamos retomar o exemplo que usamos no fim do tópico anterior:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	printf ("O número %d é positivo.", numero);
	if (numero < 0)
	{
		printf ("O número %d é negativo.", numero);
	}
	return (0);
}
```

Conforme mostramos antes, esse código acima printa somente a mensagem dizendo que 5 é um número positivo.

A mensagem que diz que o número é negativo, depende de uma condição (o número tem que ser negativo). Somente se essa condição for verdadeira é que será printado na tela a mensagem dizendo que o número é negativo. Vamos testar?

<Print com numero==-5>

Como pudemos perceber, as duas mensagens foram impressas (o que está errado, logicamente). Para consertar esse problema, basta colocarmos mais um if. Afinal, podemos colocar quantos a gente quiser no nosso código ^^. Veja só:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	if (numero >= 0)
	{
		printf ("O número %d é positivo.", numero);
	}
	if (numero < 0)
	{
		printf ("O número %d é negativo.", numero);
	}
	return (0);
}
```

Agora o código está completo! Ele printa a mensagem correta para cada número que você quiser testar. \o/

Para entendermos o que aconteceu, vamos agora aprender como o if é estruturado e como o computador entende ele.

### Estrutura do if

Quando fazemos um if, seguimos uma estrutura assim:

```c
if (condição)
```

A condição é a pergunta que fazemos para o computador. Ela sempre deve estar entre parênteses para que o computador entenda onde a pergunta começa e onde termina.

- **Mais sobre as condições:**
	
	Quando estavam pensando em fazer o if, os programadores queriam fazer perguntas com apenas duas respostas possíveis: sim ou não. É mais fácil de programar sabendo que só há essas duas pssibilidades. ^^

	Para garantir que esse requisito fosse cumprido, os criadores da linguagem C prepararam o if de um modo simples: ela compara somente números.
	
	Isso mesmo que você acabou de ler: o if compara números, apenas números e nada além de números.

	Nos nossos exemplos, comparamos a variável ``numero`` com o valor zero.

	Isso não muda nem em programas avançados. Então matenha isso no seu coração: ``"͟U͟m͟a͟ ͟c͟o͟n͟d͟i͟ç͟ã͟o͟ ͟é͟ ͟u͟m͟a͟ ͟c͟o͟m͟p͟a͟r͟a͟ç͟ã͟o͟ ͟d͟e͟ ͟n͟ú͟m͟e͟r͟o͟s͟.͟"``.

	E como comparamos esse números? Com os operadores aritméticos! Dá uma olhada na tabela com os operadores, ela também explica o que cada um significa:

	|Operador| Significado|
	|:--:|:--:|
	|<	| Menor que ...
	|<=	| Menor ou iqual a ...
	|>	| Maior que ...
	|>=	| Maior ou igual a ...
	|==	| Igual a ...
	|!=	| Diferente de ...

	Apenas para que estejamos familiarizados, veja um exemplo com cada um dos operadores que mencionamos acima:

		if (5 < 5) // 5 é menor que 5
		if (5 <= 5) // 5 é menor ou igual a 5
		if (5 > 5) // 5 é maior que 5
		if (5 >= 5) // 5 é maior ou igual a 5
		if (5 == 5) // 5 é igual a 5
		if (5 != 5) // 5 é diferente de 5

	Esses 6 operadores são todas as possibilidades que os programadores nos deram. Qualquer condição que imaginarmos só pode ser feita usando algum desses 6 operadores.
	
	Pode parecer pouco, porém, temos uma vantagem: aprendendo eles agora, sabemos que eles serão os únicos que existem para todo o sempre.

- **E as chaves que aparecem com o if?**

	As chaves (``{`` e ``}``) são como os parênteses na hora de criar a condição, dizem onde começa e onde termina as instruções.
	
	A diferença é que as chaves dizem onde começam e onde terminam os comandos que serão executados se o if for verdadeiro. Os parênteses ficam então 

	Chamamos de "bloco" o conjunto de códigos que estão dentro das chaves.

	O hábito é tão grande que é comum falarmos que o conteúdo está dentro do escopo do if (ou simplesmente, "dentro do if"). Ainda podemos dizer que o conteúdo "pertence" ao if.

	```c
	if (condição)
	{
		#códigos e mais códigos que serão executados
	}
	```
	
	Vamos para mais um exemplo:
	```c
	#include <stdio.h>

	int	main(void)
	{
		int number = 5;

		if (number == 5)
		{
			printf("Tenho uma mensagem escrita.\n");
			printf("Ela diz que o número é um número primo e é o número 5.\n");
			printf("Tudo isso ao mesmo tempo.\n");
		}
		if (number != 5)
		{
			printf("As coisas mudaram de figura.\n");
			printf("O número é difente do 5. Como pode?!\n");
		}
		return (0);
	}
	```
	No exemplo acima, apenas uma condição será verdadeira. Afinal, ou ``number`` é igual a 5, ou é diferente de 5. Mude o valores, teste à vontade.

### O nome condicional

Essa estrutura é chamada de condicional porque, os comandos dependem da condição do if para serem executados, ou não.

Essa é a introdução às condicionais.
