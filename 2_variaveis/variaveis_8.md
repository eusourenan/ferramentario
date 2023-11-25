<p align="center"> <a href="variaveis_7.md"> << Octal e Hexadecimal </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_4.md"> Próximo >> </a> </p>

# String

Declaramos números de tudo quanto foi jeito, vimos os pequenos, médios, grandes e até com ponto, mas agora é um novo momento: HORA DE VER TEXTO NA VARIÁVEEEEEEEELLLL!!!!  (Vai Brasil!!! \o/)

Se não acredita, veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	signed char	*variavel;

	variavel = "Tem uma string na variável";
	printf("Qual a mensagem?\nR: '%s'\n", variavel);
	return (0);
}
```

Somente para mostrar que pode ser ``signed`` ou ``unsigned`` eu coloquei a declaração explícita. Mas um simples ``char *variavel`` resolveria o problema.

- Por que não ser ``signed string`` ou ``signed str``? 

	Sendo bem sincero, foi uma escolha das pessoas que fizeram a liguagem.

Para entender bem essa lógica, guarde isso no seu coração: ``string é uma sequência de caracteres``.

Quando temos um char, temos uma única letra que é inserida em uma única variável.

```c
char	letra = 'L';
```

Como string é uma sequência, é como se em uma única variável eu pudesse guardar várias letras.

```c
char	*frase = "Olha o tanto de letras que existe nessa string!";
```

- **E se eu quisesse uma string com apenas uma letra?**

	Os criadores da linguagem pensaram nisso. Basta usar aspas(") quando for string e apóstrofo (') quando for apenas uma única letra. Isso quer dizer que:

	```c
	char	letra = 'a';
	```
	e
	```c
	char	letra = "a";
	```

	São duas coisas completamente diferentes para a linguagem C.

	- Aspas indicam que o conteúdo é uma string. Apóstrofos indicam que o conteúdo é apenas uma letra.

Usar o asterisco indica que você quer uma string, e indica que sua variável consegue guardar muitas letras.

Se o asterisco não for usado, a linguagem C vai entender que você tem apenas uma única letra, que sua variável é apenas um simples char. Quando isso acontece, fazer 

```c
char	letra = "a";
```

é impossível. Vai dar erro na hora de compilar.

O certo é:
```c
char	*letra = "a";
```

Para facilitar o entendimento:

|Tipo| Pode receber com apóstrofo? | Pode receber com aspas? |
|---	|	:---:|:---:|
|char	|✅		|❌
|char *	|❌		|✅

Entender essas diferenças de apóstrofo, aspas e o que elas significam, facilita o entendimento dos ponteiros (que explicarei mais tarde).

# Observação

Como você percebeu ali em cima, eu fiz a declaração e a atribuição na mesma linha. Na linguagem C, você pode fazer isso.

Você pode até declarar várias variáveis na mesma linha.

```c
#include <stdio.h>

int	main(void)
{
	int n1, n2, n3, n4; // Declarando várias variáveis na mesma linha

	n1 = 1;
	n2 = 2;
	n3 = 3;
	n4 = 42;
	printf("%d, %d, %d e %d são os números que existem nesse programa.", n1, n2, n3, n4);
	return (0);
}
```

Você também pode declarar e atribuir, tudo na mesma linha. basta separar as variáveis por vírgula (,) e terminar a declaração com ponto-e-vírgula (;).

```c
#include <stdio.h>

int	main(void)
{
	int n1 = 1, n2 = 2, n3 = 3, n4 = 42; // Declarando e atribuindo valor em várias variáveis na mesma linha

	printf("%d, %d, %d e %d são os números que existem nesse programa.", n1, n2, n3, n4);
	return (0);
}
```

Deixar isso pro final foi minha forma de não misturar as coisas na sua mente. Declarar é uma coisa, atribuir é outra coisa, usar a variável é uma terceira coisa.

Agora que já entendemos o que cada coisa é separadamente, te mostro que você pode juntar todas. Na linguagem C isso é permitido. :v:

# Finalização
Com essa parte de variáveis concluída, você consegue declarar, atribuir e printar qualquer tipo de variável em C.

Tente criar suas mensagens com os variados tipos, assim você se habitua e enraíza o conhecimento. Pratique enquando o próximo assunto não vem.

O próximo assunto o que veremos são as condicionais (o famoso ``if``). Mas por hora, "Isso é tudo Pê-Pê-Pessoal."

<p align="center"> <a href="variaveis_7.md"> << Base oito, e dezesseis </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="../3_condicionais/condicionais_1.md"> Bora tacar um if no código >> </a> </p>
