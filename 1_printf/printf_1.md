# O Início
Para começarmos com o pé direito, vamos com o clássico início no aprendizado nas liguagens de programação: mostrar mensagens no terminal.

``Printf`` é uma função que é muito conhecida e consagrada nas linguagens de programação. É uma abreviação de "print formatted", que siginifica ``imprimir formatado``.

Por convenção minha, usarei a palavra "printar" ao invés de "imprimir".

Com tudo dito, nosso primeiro ato será usar a ``printf`` para printar as coisas na tela. Toma um exemplo:

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

``` Qualquer texto pode ser colocado no lugar do "Hello World", sinta-se a vontade para testar.```

O caracter ``\n`` é interpretado como uma quebra de linha. Sem ela, seu texto seria printado assim:

![image](https://github.com/eusourenan/ferramentario/assets/102669882/099c4749-0e90-49b7-b355-8771e312ffe2)

Por isso, se lembre de colocar o ``\n``.

## Observação
Se você usa algum shell com quebra de linha automática, como o ``zsh``, um símbolo será colocado pra dizer que não houve uma quebra de linha no fim da mensagem.

![image](https://github.com/eusourenan/ferramentario/assets/102669882/daf6df09-0010-4885-892e-9b2afb07b213)

![Alt text](image.png)

O seu código continua fazendo a impressão sem uma quebra de linha, mas você pode ter a falsa sensação de estar fazendo uma impressão bonita, por isso, fique atento(a).

## Sobre o '\n' ser "1 caractere"

Sim, você leu direito, ele é interpretado como um único caractere. Pra escrevê-lo usamos a ``\`` e o ``n`` (sim, dois caracteres). A ``\`` é usada para representar alguns caracteres especiais (o que será explicado mais na frente). Por hora, ``\n`` é uma quebra de linha e fará a impressão mais bonita, caso queiramos.

![image](https://github.com/eusourenan/ferramentario/assets/102669882/24abb721-eb51-478d-b080-6ac439ea9dc0)

![image](https://github.com/eusourenan/ferramentario/assets/102669882/e9610ba3-a272-4e4b-8ae5-3f1db0aabbc9)

É posível mandar imprimir caracteres especiais (como o nosso amigo \n). Mas também é possível mandar outros tipos de dados para serem impressos (Afinal, o printf formata o quê?). Veja os próximos tópicos e se emocione. 💝
