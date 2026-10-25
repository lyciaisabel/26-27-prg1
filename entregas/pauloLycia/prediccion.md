# Reto extendido: predicción

## Caso

Debe pagar **232 €** y el cliente paga con **200 €**. Se incumple la condición *"la cantidad entregada es siempre mayor o igual que el importe a pagar"*.

## Predicción (antes de ejecutar)

El cambio será `200 - 232 = -32`. El programa no comprueba nada (no se permite `if`), así que hará las mismas divisiones con un número negativo.

En Java, con `int`, la división `/` trunca hacia cero y el resto `%` conserva el signo del dividendo:

| Denominación | División | Cantidad | Resto |
|---|---|---|---|
| 100 € | -32 / 100 | 0 | -32 |
| 50 € | -32 / 50 | 0 | -32 |
| 20 € | -32 / 20 | -1 | -12 |
| 10 € | -12 / 10 | -1 | -2 |
| 5 € | -2 / 5 | 0 | -2 |
| 2 € | -2 / 2 | -1 | 0 |
| 1 € | resto | 0 | |

Predigo que el programa no dará error y mostrará:

```
0 billete(s) de 100 €
0 billete(s) de 50 €
-1 billete(s) de 20 €
-1 billete(s) de 10 €
0 billete(s) de 5 €
-1 moneda(s) de 2 €
0 moneda(s) de 1 €
```
