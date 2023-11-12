<p align="center"> <a href="printf_2.md"> << Quero formatar de novo </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_4.md"> Próximo Tipo >> </a> </p>

# Char
### <center>Transformando números em letras </center>

No tópico anterior vimos os números. Agora veremos que letras também podem ser argumentos do printf.

O exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Uma letra qualquer: %c\n", 'A')
	return (0);
}
```

## Mas, por que a letra A está com ``''``?
Os apóstrofos (ou aspas simples, se preferir) são colocados quando queremos apenas um caractere.

Sem os apóstrofos, teríamos esse erro:

<Erro de variável não declarada>

Falaremos sobre esse erro no momento de explicar variáveis. Por enquanto, só basta saber que teremos que colocar apóstrofos para o computador entender que queremos uma letra.

As aspas duplas (chamarei apenas de aspas daqui pra frente), são usadas para indicar textos maiores que 1 caractere. No próximo tópico falo mais sobre isso.

<Exemplo com aspas simples e dupla>

## Tem como imprimir sem os apóstrofos?

Sim! Veja esse exemplo:

<Subistituir A pelo ASCII correspondente>

Como foi dito no sub-título, a printf ``transforma números em letras``. O padrão é dado pela tabela ASCII, facilmente encontrada na web.

Para testar, basta colocar o número e depois a letra que você deseja com os apóstrofos.

<Exemplo com ASCII e a letra misturados>

Usar os apóstrofos ajuda o ser humano porque faz a gente não ter a necessidade de decorar a tabela ASCII. Basta colocar ``'L'`` e isso será substituído pelo número correto.

O ``%c`` faz o printf entender que o número tem que ser printado como um caractere.

Alguns desses caracteres não são printáveis, alguns não aparecem na tela ``mas podemos colocar ele no texto usando a \``. Consulte os colegas e a web para maiores informações. :heart:

[Aqui tem um link pra uma tabela ASCII.](https://nearbus.net/wiki/images/1/1f/AscII_0.png)

# Dúvida natural
Acabei de aprender sobre 2 especificadores que existem no printf (``%d`` e ``%c``). Cada um foi mostrado separadamente, mas eu posso juntar os dois numa mesma frase?

Sim, você pode! :partying_face:

## Misturando as flags
### <center>Porque gostamos de mensagens variadas :sunglasses:</center>

Indo direto ao ponto, veja o exemplo:
```c
#include <stdio.h>

int	main(void)
{
	printf("A letra %c aparece %d vezes nessa mensagem\n", 'a', 6);
	return (0);
}
```

O printf nos permite misturar as flags, contanto que lembremos da regra:

- A primeira ``%`` será substituída pelo primeiro argumento após a mensagem. A segunda ``%`` será substituída pelo segundo argumento após a mensagem e assim por diante.

E como ele printa de modos diferentes para valores diferentes, nós temos que especificar o tipo com a letra após o caractere de ``%``.

Isso termina esse tópico.

Que tal agora aprendermos como fazer uma mensagem inteira ser um argumento da nossa mensagem?

<p align="center"> <a href="printf_2.md"> << Quero formatar de novo </a> &#8195;&#8195;&#8195;&#8195; | &#8195;&#8195;&#8195;&#8195; <a href="printf_4.md"> Qual a mensagem? >> </a> </p>