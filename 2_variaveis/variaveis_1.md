<p align="center"> <a href="../1_printf/printf_8.md"> << Volta pro final do printf, plase </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_2.md"> Próximo Tipo >> </a> </p>

# Os tipos de variáveis

Quando conversamos sobre o printf, falamos que os números poderiam ter tipos e que nós usamos as letras para que o printf entenda qual o tipo do número.

E mais, quando colocávamos os valores nos exemplos, a gente tinha 100% de clareza sobre o valor que iria ser impresso.

Exemplos:
```c
printf("A resposta é: %d\n", 42);
```

```c
#include <stdio.h>

int	main(void)
{
	printf("Pedro tem %d anos\n", 37);
	printf("O dobro da idade de Pedro é %d\n", 37 * 2);
	return (0);
}
```

Para entender qual a utilidade de variáveis, imagine que você fez algo de errado em algum código.

```c
#include <stdio.h>

int	main(void)
{
	printf("Pedro tem %d anos\n", 37);
	printf("O dobro da idade de Pedro é %d\n", 21 * 2);
	returxn (0);
}
```
Num código assim, é fácil mexer. Também é fácil de corrigir. Basta alterar o valor que está errado e pronto!

Mas...

- **E se a gente precisasse usar essa fórmula em mais prints?**

Dá pra fazer um simples ``Ctrl + C, Ctrl + V`` e ajustar as mensagens.

Quantas vezes forem necessárias fazer isso.

<print pra confirmar a frase acima>

- **E se eu precisasse mudar algo na fórmula porque está errado?**

Como você está imaginando, você teria que mudar em todos os printfs que você tivesse usado aquela fórmula errada.

<mais um print>

- **Tem algum jeito mais fácil?**

Sim! Podemos criar variáveis:

<Substituir a fórmula problema pela variável que recebe o valor que queremos>

# O rolê das variáveis

Da mesma forma que o printf substitui o ``%d`` pelo número que você manda como argumento, a palavra ``caramba`` será substituída pelo número que definimos na linha ~~.

Vamos detalhar o que aconteceu:

- Primeiro, uma variável foi criada na linha ~~. Chamamos isso de ``declaração`` de variável:

<Parte da declaração da variável>

Para uma variável ser declarada, devemos colocar o ``tipo`` da variável, depois o nome da variável. Isso SEMPRE será nessa ordem.

Com isso, temos uma variável que pode ser usada em vários lugares. :v:

Ela pode ter qualquer nome [desde que respeite as regras de nome de variável (no fim da página).](#regras-de-declaração-de-variáveis)

- Depois da declaração, inserimos um valor nessa variável. Essa parte é chamada de ``atribuição`` da variável:

<Atribuição>

Como foi dito uns parágrafos acima, a variável será substituída pelo valor que ela armazena. Mas qual é o valor que tem na variável?

A ``Atribuição`` diz a resposta. O valor que terá na variável, será o valor que colocarmos depois do igual.

Para atribuir um valor à variável você SEMPRE deve colocar o igual e dizer qual é o valor que a variável terá.

Caso você não atribua nenhum valor à variável, ela fica com um valor aleatório que o sistema que dá. Muitas vezes é o número zero, mas isso não é uma regra que vale sempre e pode gerar alguns erros dependendo do que o seu código faz. 

Por isso, SEMPRE atribua algum valor para suas variáveis.

Nos textos futuros, posso trocar ``atribuir à variável`` por: "armazenar na variável", "colocar na variável", "inicializar a variável" e talvez "inserir na variável". Todos esses termos se referem à atribuição. :heart:

- E por fim, com a variável declarada e com valor atribuído, usamos a variável:

<Usando a variável>

Em alguns contextos, posso acabar misturando "usar" e "chamar" a variável. As duas palavras se referem ao mesmo contexto da imagem. 

Posso também falar "Pegar o valor da variável". Todos esses termos estão se referindo ao que está na imagem acima.

Toma um exemplo simplificado:

<Exemplo simplificado e comentado>

A vantagem é que agora, basta a gente mudar o valor na linha da atribuição que ele será alterado em todos os lugares nos quais usamos a variável.

Não tem mais re-escrita de código, nem duplicação de uma parte difícil de modificar.

Sendo assim, a variável é só um meio de usar um número que já foi definido antes em outro lugar do código, sem precisar ficar escrevendo o mesmo o número de novo.

Recomendo que crie variáveis com o nome que você desejar, troque o que você quiser no código e perceba o que acontece.

Lembre-se apenas de respeitar o tipo quando usar o printf.

Use ``%d`` quando sua variável for ``signed int``, ``%f`` quando for ``signed float`` e assim por diante.

## Mas quais são os tipos que existem?

Veja a tabela:

|Tipo da variável|Pode ser signed?|Pode ser unsigned?
:--:|:--:|:--:|
|int		|✅	|✅
|char		|✅	|✅
|float		|✅	|❌
|long		|✅	|✅
|double		|✅	|❌
|long double|✅	|❌

A tabela foi um meio rápido de explicar que podemos criar variáveis do tipo:
- signed int
- unsigned int
- signed char
- unsigned char
- signed float
- signed long
- unsigned long
- signed double
- signed long double

Sua(s) variável(is) pode(m) ter qualquer um dos 9 tipos.

Os intervalos dos números que podem ser representados e qual o especificador do printf para cada tipo, pode ser vista na [tabela de especificadores]() vista no tópico do ``printf``.

Isso finaliza a introdução às variáveis.

Os próximos tópicos tratam dos tipos de variáveis que temos em C.

## Regras de Declaração de Variáveis

- Primeiro devemos especificar o tipo da váriavel, depois o nome da variável.

  - Nesse exemplo: ``signed int`` (inteiro com sinal) é o tipo e ```` é o nome da variável.

-  Variáveis não podem ter acento, não podem ter espaços, não podem começar com número e não podem ter caracteres especiais além do ``_`` (underline).

	- Exemplos de nomes de variáveis válidas:
		- variavel
		- _teste
		- _teste2
		- mesclando_t3xt0_c0m_num3r02

	- Exemplos de nomes de variáveis errados:
		- 1teste
		- $com(cara@
		- um-teste-qualquer
		- 1234
		- minha variável

<p align="center"> <a href="../1_printf/tipos_de_especificadores.md"> << Tabela de tipos </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="variaveis_2.md"> Próximo >> </a> </p>
