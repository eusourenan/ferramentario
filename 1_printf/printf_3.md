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

As aspas duplas (chamarei apenas de aspas daqui pra frente), são usadas para indicar textos maiores que 1 caractere. No próximo tópico falo mais sobre isso.

<Exemplo com aspas simples e dupla>

## Tem como imprimir sem os apóstrofos?

Sim! Veja esse exemplo:

<Subistituir A pelo ASCII correspondente>

Como foi dito no sub-título, a printf ``transforma números em letras``. O padrão é dado pela tabela ASCII, facilmente encontrada na web.

Para testar, basta colocar o número e depois a letra que você deseja com os apóstrofos.

<Exemplo com ASCII e a letra misturados>

Usar os apóstrofos ajuda o ser humano porque faz a gente não ter a necessidade de decorar a tabela ASCII. Basta colocar ``'L'`` e isso será substituído pelo número correto.

O ``%c`` faz o printf entender que o número tem que ser printado como um caracter.

Alguns desses caracteres não são printáveis, alguns não aparecem na tela ``mas podemos colocar ele no texto usando a \``. Consulte os colegas e a web para maiores informações. :heart:

[Aqui tem um link pra uma tabela completa.](https://nearbus.net/wiki/images/1/1f/AscII_0.png)
