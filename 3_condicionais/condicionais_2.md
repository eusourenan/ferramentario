## O "if"

Para a explicação, iremos usar o mesmo código-exemplo que o tópico anterior:

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

Você pode perceber que ele não executou a mensagem dizendo que o número 5 é negativo. 

Isso ocorre porque antes de ser feito o print dizendo que o número é negativo, fizemos uma pergunta: ``"O número é negativo?"``.

Para ser mais exato a pergunta foi: ``"5 é menor que zero?"``. A resposta: não. Cinco não é menor que zero.

Com a resposta dessa pergurta, podemos definir o que será executado e o que não será executado. Fazendo códigos mais completos.

Nesse momento, é um passo pequeno que estamos fazendo. Mas na verdade essa ferramenta simples de comparação nos abre um mar de possibilidades.

Podemos fazer códigos complexos, separar ele por partes e decidir que parte dele será executada com base nas condições que escolhermos.

Porque, não importa o quão grande seja seu programa, muito provavelmente terá um ou mais if nele. Saber como usá-lo vai te dar muitas opções de como resolver problemas. Seja de níveis fáceis ou difíceis.

Vamos então destrinchar como funciona os if's.

### Estrutura do if

Quando fazemos um if, seguimos uma estrutura assim:

```c
if (condição)
```

Essa estrutura é formada pela palavra ``if`` seguida de parênteses e a condição deve estar dentro dos parênteses.

A condição será a pergunta que queremos saber naquele exato momento. Obrigatoriamente ela deve ter somente duas respostas possíveis: sim ou não.

- **Sobre as condições:**
	
	Para fazer uma condição em um if, lembre-se: as respostas são feitas com apenas duas respostas possíveis (sim ou não).

	Garantir que isso fosse mantido fez os criadores da linguagem C criarem o if de um modo simples: ela compara números. Isso mesmo que você acabou de ler, números, apenas números e nada além de números.

	No exemplo de código que vimos antes, comparamos a variável ``numero`` com zero.

	Isso não muda nem em programas avançados. Então matenha isso no seu coração: ``"͟U͟m͟a͟ ͟c͟o͟n͟d͟i͟ç͟ã͟o͟ ͟é͟ ͟u͟m͟a͟ ͟c͟o͟m͟p͟a͟r͟a͟ç͟ã͟o͟ ͟d͟e͟ ͟n͟ú͟m͟e͟r͟o͟s͟.͟"``.

	Conseguimos comparar os números com os seguintes operadores:

	|Operador| Significado|
	|:--:|:--:|
	|<	| Menor que ...
	|<=	| Menor ou iqual a ...
	|>	| Maior que ...
	|>=	| Maior ou igual a ...
	|==	| Igual a ...
	|!=	| Diferente de ...

	Vejamos alguns exemplos:

		if (5 < 5) // 5 é menor que 5
		if (5 <= 5) // 5 é menor ou igual a 5
		if (5 > 5) // 5 é maior que 5
		if (5 >= 5) // 5 é maior ou igual a 5
		if (5 == 5) // 5 é igual a 5
		if (5 != 5) // 5 é diferente de 5

	Esses 6 operadores são todas as possibilidades que os programadores nos deram. Aprendendo eles agora, eles serão os mesmo para sempre.

- **E as chaves que aparecem depois?**

	As chaves (``{`` e ``}``) dizem onde o if começa e termina. Isso é feito para o caso de você ter vários comandos que dependem de uma condição.

	De modo técnico, dizemos que o conteúdo está dentro do escopo do if (ou simplesmente, "dentro do if"). Ainda podemos dizer que o conteúdo "pertence" ao if.
	
	Exemplo:
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
