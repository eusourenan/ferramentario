<p align="center"><< Anterior &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; Próximo >> </p>


# Inteiros
### <center>Porque outro tipo não seria o mais óbvio pra começar </center>

O printf tem uma parte de printar (o que foi visto no tópico anterior) e também tem a parte de formatar.

Como isso funciona? Explicarei agora.

Antes, nós printamos o texto inteiro e tínhamos certeza que o texto não seria alterado. Por exemplo:
```c
printf ("Hello World\n");
```
sempre irá mostrar a frase ``Hello World``. Você pode executar o programa 100 vezes ou pode executar até ficar satisfeto(a), se não acreditar em mim.

Mas, e se eu quiser um texto que pode mudar o conteúdo que ele imprime? Por exemplo, um printf que printa ``Sua idade é: X``.

É simples! Basta usarmos ``%d`` no lugar do X e definirmos o número que quisermos. Toma aí um exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Sua idade é: %d\n", 42);
	return (0);
}
```

Talvez você esteja se perguntando: "O que acabou de acontecer?". A resposta é s͟u͟b͟s͟t͟i͟t͟u͟i͟ç͟ã͟o.

Ele susbstitui o ``%d`` pelo número que você colocar. Troque o número e execute novamente para ver a mágica acontecendo. A mesma frase, pode printar vários números diferentes.

## '%d'?

As letras que vem após o caractere de ``%`` são chamadas de e͟s͟p͟e͟c͟i͟f͟i͟c͟a͟d͟o͟r͟e͟s, porque você está especificando o ``tipo`` do argumento enviado.

No nosso caso de agora, os argumentos são i͟n͟t͟e͟i͟r͟o͟s.

Por que a letra 'd'? É a abreviação da palavra ``dígito``. Mas ele também funciona com a letra 'i' (abreviação de ``inteiro``).

Da mesma forma que a ``\``, que foi comentada antes, o caractere de ``%`` indica que algo diferente vai ser printado. A diferença entre as duas é que itens escritos com ``\`` são escritos na hora. Por exemplo ``\n``.

Já o caractere de ``%`` indica que o valor será enviado como argumento da função.

Essa é a parte formatada da ``printf``.

## "Mas, e essa vírgula aí?"

Como dito antes, o printf é uma ``f͟u͟n͟ç͟ã͟o`` (explico melhor no tópico 6). Ele é uma função que aceita vários argumentos, bastando separar eles por vírgulas.

O texto que você quer printar, sempre fica como primeiro argumento da função:

<print dizendo que os argumentos são separados por vírgula>

Caso você queira imprimir 2 números basta colocar 2 ``%d`` na frase e os números que você quer imprimir.

<Exemplo de printf com 2 números>

Você pode aumentar o quanto você quiser! Apenas se lembre: o primeiro ``%d`` será o primeiro número após a mensagem, o segundo ``%d`` será o segundo número após a mensagem e assim por diante.

Os números serão colocados exatamente onde você colocar o ``%d``.

Troque o ``%d`` de lugar, mude a mensagem e veja por você.

## Lembrete
``Os especificadores S͟E͟M͟P͟R͟E devem estar no primeiro argumento.``

Mesmo mostrando os outros que existem, essa regra será sempre a mesma.

Vamos ver isso os outros especificadores pra testar isso na prática.

<p align="center"> <a href="printf_1.md"> << Anterior </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_3.md"> Próximo >> </a> </p>
