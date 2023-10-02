# O Início
Para começarmos com o pé direito, vamos com o clássico início no aprendizado nas liguagens de programação: mostrar mensagens no terminal.

Nosso comando para printar as coisas na tela, será o ``printf``. Toma um exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Hello World!\n");
	return (0);
}
```

Crie um arquivo, cole esse texto nele e veja a mágica acontecer.

Se tudo der certo, você verá um print como na imagem:

![image](https://github.com/eusourenan/ferramentario/assets/102669882/0e843f71-bfaa-483f-8c65-5e4db9a4ab8e)

O caracter ``\n`` é interpretado como uma quebra de linha. Sem ela, seu texto seria printado assim:

![image](https://github.com/eusourenan/ferramentario/assets/102669882/099c4749-0e90-49b7-b355-8771e312ffe2)

Por isso, se lembre de colocar o ``\n``.

## Sobre o '\n' ser "1 caracter"

Sim, você leu direito, ele é interpretado como um único caractere.

## Observação
Se você usa algum shell com quebra de linha automática, como o ``zsh``, um símbolo de ``%`` será colocado pra dizer que não houve uma quebra de linha no fim da mensagem.

![image](https://github.com/eusourenan/ferramentario/assets/102669882/daf6df09-0010-4885-892e-9b2afb07b213)

O seu código continua fazendo a impressão sem uma quebra de linha, mas você pode ter a falsa sensação de estar fazendo uma impressão bonita, por isso, fique atento(a).
