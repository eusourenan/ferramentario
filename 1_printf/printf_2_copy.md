<p align="center"> <a href="printf_1.md"> << O início </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_3.md"> Próximo Tipo >> </a> </p>

# Formatação

A parte de printar [foi vista no tópico anterior](printf_1_copy.md), a parte de formatar a gente não viu ainda. Vamos dar uma olhada então. 🐱‍💻

Na programação, muitas vezes programamos algo geral que vale para múltiplos valores.

Vamos pôr um exemplo: Ana tem uma idade X, Pedro tem o dobro da idade de Ana menos 15, qual idade de Pedro?

Na hora, você pode me responder ``"sei lá! Não sei nem a idade da Ana."`` E você está correto(a).

De forma matemática, você me responderia: ``"A idade de Pedro é 2 * X + 15" e 'X' é a idade de Ana``. 

Então a gente depende da idade de Ana para saber o valor da idade de Pedro. Não dá pra simplesmente colocar isso no printf com o que a gente viu até agora.

O melhor que podemos fazer é: 

```c
#include <stdio.h>

int	main(void)
{
	printf("A idade de Ana é X\n");
	printf("A idade de Pedro é 2 * X - 15\n");
	return (0);
}
```

Mas, e se quisermos o número mesmo, ao invés dessa fórmula escrita?

Usaremos a formatação do printf! :sunglasses:

A formatação no printf é usada para quando temos uma mensagem que pode ter valores diferentes e a gente não sabe logo de cara qual é.

Vamos então colocar uns números ali e ver como isso acontece.

```c
#include <stdio.h>

int	main(void)
{
	printf("A idade de Ana é %d\n", 25);
	printf("A idade de Pedro é %d\n ", 2 * 25 - 15);
	return (0);
}
```

Se executarmos, vamos ter essa mensagem na tela:

<print do código acima>

Talvez você esteja se perguntando: "O que acabou de acontecer?". A resposta é s͟u͟b͟s͟t͟i͟t͟u͟i͟ç͟ã͟o.

Ele susbstitui o ``%d`` pelo número que você colocar. 

No caso da idade do Pedro, o valor é o resultado da conta.

Troque o número e execute novamente para ver a mágica acontecendo. A mesma frase, pode printar vários números diferentes!

E mais, ele substitui na ordem em que os números aparecem. Veja o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("A idade de Ana é %d\nA idade de Pedro é %d\n ", 25, 2 * 25 - 15);
	return (0);
}
```

A resposta é a mesma porque o primeiro ``%d`` foi substituído por "25" e o segundo ``%d`` foi substituído pelo resultado da conta "2 * 25 - 15".

Sempre será assim, o primeiro valor com o primeiro ``%d``, o segundo valor com o segundo ``%d`` e assim por diante.

A vantagem disso é que você pode montar a mensagem que você quiser e essa mensagem vai servir para vários momentos diferentes. Sem precisar, por exemplo, fazer um print para a idade da Ana sendo 1, depois outro com a idade da Ana sendo 2 e assim por diante.

<printf com aquela barra vermelha linkando o primeiro argumento com o primeiro %d>

## "Mas, e essa vírgula aí?"

[Como dito antes](printf_1_copy.md), o printf é uma [f͟u͟n͟ç͟ã͟o](../6_funcao/funcao_1.md). Ele é uma função que aceita vários argumentos, bastando separar eles por vírgulas.

A virgula, portanto, é o meio de o printf saber qual é o primeiro valor, qual é o segundo, qual é o terceiro, e assim por diante.

Você pode colocar quantos ``%d`` quiser!
- Quer apenas 1, tudo bem.
- Nenhum? Tudo certo.
- Quer 15? Dá certo também.

Apenas se lembre: o primeiro ``%d`` será o primeiro número após a mensagem, o segundo ``%d`` será o segundo número após a mensagem e assim por diante. Essa regra nunca muda.

Os números serão colocados exatamente onde você colocar o ``%d``.

Troque o ``%d`` de lugar, mude a mensagem e veja por você.

## E o que é '%d'?

Da mesma forma que a ``\``, que foi comentada antes, o caractere de ``%`` indica que algo diferente vai ser printado. A diferença entre as duas é que itens escritos com ``\`` são escritos na hora. Por exemplo, nosso amado ``\n``.

Já os itens com ``%`` serão substituídos com os valores enviados após a mensagem. O printf vai converter os valores para texto e printar para a gente.

Normalmente, nós colocamos ``%`` nesses casos em que não sabemos o valor exato, mas queremos deixar o lugar marcado pra substituir.

Para uma substituição sem problemas, precisamos colocar a letra depois do ``%``.

As letras que vem após o caractere de ``%`` são chamadas de e͟s͟p͟e͟c͟i͟f͟i͟c͟a͟d͟o͟r͟e͟s, porque você está e͟s͟p͟e͟c͟i͟f͟i͟c͟a͟n͟d͟o o ``tipo`` do argumento enviado.

Por que a letra 'd'? É a abreviação da palavra ``dígito``. Porque os números são escritos com dígitos ao invés de letras.

Mas ele também funciona com a letra 'i' (abreviação de ``inteiro``). Basta mudar ``%d`` por ``%i`` nos códigos que você está testando e você vai ver que ele printa a mesma coisa.

[Uma tabela com alguns tipos](tipos_de_especificadores.md) foi colocada por aqui para você revisar e testar. Iremos falar mais sobre cada tipo por aqui. Por enquanto, saiba que você acabou de ver os números inteiros.

Essa é a parte formatada da ``printf``! :partying_face:

## Lembrete
``Os especificadores S͟E͟M͟P͟R͟E devem estar no primeiro argumento.``

Mesmo mostrando os outros que existem, essa regra será sempre a mesma.

Vamos ver isso os outros especificadores pra testar isso na prática.

<p align="center"> <a href="printf_1.md"> << O Início </a> &#8195;&#8195;&#8195;&#8195; | &#8195; <a href="printf_3.md"> Vamos ver o que é char >> </a> </p>
