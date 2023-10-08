# O fim
### <center>Desta parte, pelo menos</center>

Essa pequena trajetória em torno do ``printf`` nos mostrou que é possível printar textos de variadas formas.

Você pode muito bem inventar mensagens que serão adaptadas para o contexto que você quiser. Parabéns por isso! :clap::clap::clap::clap::clap:

Para finalizar os tipos que me propus a apresentar, um tipo ainda não mencionado: números reais (que são os números com vírgula). Ou, falando o tipo em inglês: ``float``.

Para imprimir ``floats`` tome o exemplo:

```c
#include <stdio.h>

int	main(void)
{
	printf("Número real qualquer: %f\n", 42.1234);
	return (0);
}
```

O padrão americano é diferenciado. Eles usam vírgulas e pontos trocados.

Nós escrevemos um milhão de dinheiros assim: 1.000.000,00.\
Eles preferem escrever o mesmo milhão assim: 1,000,000.00.

Como a linguagem segue o padrão dos americanos, temos que usar o ponto pra fazer um número real. Se usarmos vírgula, ele vai reclamar com a gente.

<print de erro>

## Finalização com chave de ouro

Imaginando que você não misturou as flags ainda, saiba: é possivel.

<Exemplo de flags misturadas>

Com isso, sua imaginação é que define os limites do que será impresso na tela.

Se quiser mais informações de como o printf funciona clique [aqui](https://www.man7.org/linux/man-pages/man3/printf.3.html).
