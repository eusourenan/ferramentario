# Condicionais
## Hora de começar a criar lógica de programação

Até aqui, aprendemos a criar variáveis, colocar valor nelas e fazer a impressão do jeito que queremos. Que progresso! :clap::clap::clap::clap::clap::clap::clap:

O que faremos agora é dar os primeiros passos para a lógica de programação. Para fazer esses primeiros passos, vamos fazer nosso programa decidir entre duas mensagens e printar apenas uma.

Veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	printf ("O número %d é positivo.", numero);
	printf ("O número %d é negativo.", numero);
	return (0);
}
```

Se executarmos esse código, vamos ter o seguinte resultado:

<print do código acima>

Como dá pra peceber, o código foi executado com sucesso. MAS, as mensagens são contraditórias e não fazem sentido para quem vai ler.

Isso acontece porque o computador é "um tanto robótico".

Se você mandar ele imprimir, ele imprime e ponto final. Se a mensagem não faz sentido, é apenas porque pedimos para imprimir algo que não deveria ser printado.

Daí, que podemos "dizer para o computador" que se algo ocorre ele imprime, ou não imprime a mensagem. Veja o exemplo:

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
Executando esse código temos:

<Print da execução do código acima>

## O "if"

Como você perceber, ele não executou a mensagem dizendo que o número 5 é negativo. 

Se você trocar o número e colocar um valor negativo no lugar, vai perceber que ele não irá imprimir a mensagem dizendo que o número é positivo. O que faz todo o sentido para nós, humanos.

Isso ocorre porque antes de ser feito o printf, fizemos uma pergunta: ``"O número é positivo?"``

<print do numero \>= 0>

A comparação é uma comparação direta: "5 é maior ou igual a zero?"

Pra essa pergunta, apenas duas repostas são possíveis: Sim e Não. Ou ele é 'maior ou igual a zero', ou ele não é.

Nesse momento, isso é um passo pequeno. Mas na verdade essa ferramenta simples de comparação nos abre um mar de possibilidades.

Podemos fazer códigos complexos, separar ele por partes e decidir que parte dele será executada com base nas condições que escolhermos.

Não importa o quão grande seja seu programa, ele provavelmente terá um if nele. Saber como usá-lo vai te dar muitas opções de como resolver problemas. Seja de níveis fáceis ou difíceis.

Vamos então destrinchar como funciona os if's.

### Estrutura do if

Quando fazemos um if, seguimos uma estrutura assim:

```c
if (condição)
```
Essa estrutura é formada pela palavra ``if`` seguida de parênteses e a condição deve estar dentro dos parênteses.

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

Essa estrutura é chamada de condicional porque, para executar os comandos que estão no escopo do if, a condição tem que ser verdadeira.

Essa é a introdução às condicionais.
