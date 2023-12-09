# if / else if / else

Até aqui, conseguimos fazer if de várias formas diferentes, agora podemos fazer com que ele trabalhe com condições simples e podemos fazer ele juntar dois blocos como se fosse um.

Porém, a mente humana trabalha com um mundo complexo e que não para de evoluir. Esta evolução constante deixa uma dúvida na mente: e se eu tiver algo mais complexo, como vou resolver?

No caso do if, aprendemos que podemos fazer as condições diretamente, entendemos que podemos estruturar eles com um "if-else", o que faz o sistema interpretar duas condições numa única estrutura.

E sobre essa construção de ifs, temos que pensar em mais uma possibilidade: E se tivermos que verificar mais de uma possibilidade com apenas uma única estrutura?

Para termos um código prático e usar os conhecimentos que temos até o momento, poderíamos fazer uma pergunta: o número é diferente, ou o número é igual a 5? 

Responder a pergunta nos traz o seguinte código:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	if (numero == 5)
		printf("O número é igual a 5\n");
	else
		printf("O número é diferente de 5\n");
	return (0);
}
```

Mas, existe outra maneira de saber se o número é diferente, ou igual a 5. Elas são:

- O número é menor que 5;
- O número é maior que 5;
- O número é igual a 5.

Para responder essa pergunta, teríamos que fazer 3 comparações. Com nossos conhecimentos atuais, faríamos mais ou menos assim:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	if (numero < 5)
		printf("O número é menor a 5\n");
	if (numero > 5)
		printf("O número é maior que 5\n");
	if (numero == 5)
		printf("O número é igual a 5\n");

	return (0);
}
```

E como foi relatado no tópico anterior, o computador vai fazer todas as comparações, mesmo se já tiver passado pela resposta correta.

### **Else if**

Os nossos amigos criadores da linguagem C tiveram uma ideia para conseguir juntar as 3 comparações em uma única estrutura, a criação de mais uma comparação (mais um if) depois da palavra ``else``. Veja como fica a solução do código acima:

```c
#include <stdio.h>

int	main(void)
{
	int	numero = 5;

	if (numero < 5)
		printf("O número é menor a 5\n");
	else if (numero > 5)
		printf("O número é maior que 5\n");
	else
		printf("O número é igual a 5\n");

	return (0);
}
```

Para entendermos melhor essa estrutura, irei escrevê-la em português:

```
se (numero < 5)
	printf("O número é menor a 5\n");
senão se (numero > 5)
	printf("O número é maior que 5\n");
senão
	printf("O número é igual a 5\n");

```

O ``else if (senão se)`` é apenas uma forma de conseguir fazer mais perguntas e juntar todas as possibilidades em uma única estrutura.

Assim que uma condição for verdadeira, todas as outras condições serão ignoradas e o computador vai executar o resto do código.

Temos agora toda uma estrutura que verifica várias possibilidades. Tantas quanto você precisar!

Caso você queira verificar mais que 3 possibilidades, você pode montar a estrutura dessa forma:

```c
if (condição1)
{
	...
}
else if (condição2)
{
	...
}
else if (condição3)
{
	...
}
else if (condição4)
{
	...
}
else if (condição5)
{
	...
}
else if (condição6)
{
	...
}

// Mais quantas condições você quiser

else // Última condição (será verdade caso nenhuma acima seja verdadeira)
{
	...
}
```

A primeira condição sempre é feita com um ``if``. As do meio sempre com um ``else if`` e a última com um ``else``. 

Repare que não falei "sempre termina com else", pois você não precisa obrigatoriamente terminar a estrutura inteira com um else, por exemplo:

```c
if (condição1)
{
	...
}
else if (condição2)
{
	...
}
else if (condição3)
{
	...
}
else if (condição4)
{
	...
}
else if (condição5)
{
	...
}
else if (condição6)
{
	...
}
```

É uma estrutura válida e que você pode usar tranquilamente. Ela te permite verificar todas as condições e garantir que você não execute nada, caso todas as verificações sejam falsas.

Essa é praticamente a finalização sobre o if, para concluírmos com chave de ouro, que tal ver if dentro de if?
