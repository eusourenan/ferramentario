# Float

Bom, o padrão é o mesmo que já conhecemos:
```
tipo_da_variável nome_da_variável
```
 Partiu pro exemplo:

```c
#include <stdio.h>

int	main(void)
{
	float	variavel;

	variavel = 12.3456;
	printf("Quero dinheiro, mas só tenho R$ %f\n", variavel);
	return (0);
}
```

Sim, você viu direito, não tem a palavra ``signed``.

<Mostar erro usando signed float>

A palavra ``signed`` só pode ser explicitada nos tipos int, char e long

Isso é por conta de como as variáveis funcionam por debaixo dos panos.

[Daqui o que falta é explicar o funcionamento de bits dos tipos por debaixo dos panos] [seria bom pegar desenhos pra explicar]