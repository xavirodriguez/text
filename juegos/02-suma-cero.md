Un **juego de suma cero** describe situaciones en las que la ganancia de un jugador equivale exactamente a la pérdida del otro, de modo que la suma total de recompensas siempre es cero. Es un concepto central en la teoría de juegos porque simplifica el análisis de conflictos estrictamente competitivos.

### Características clave

1. **Equilibrio exacto de ganancias y pérdidas**: Si un jugador gana 30, otro pierde 30.
2. **Estrategias óptimas**: Los jugadores suelen emplear **estrategias minimax**, que buscan minimizar la pérdida máxima posible, anticipando la reacción del oponente.
3. **Generalización**: Von Neumann y Morgenstern demostraron que cualquier juego de suma cero con múltiples jugadores puede reducirse a un juego de dos jugadores o a un juego de n+1 jugadores, donde el jugador adicional refleja la ganancia o pérdida total.

### Diferencia con juegos de suma no nula

- **Suma no nula**: Ambos jugadores pueden beneficiarse o perder simultáneamente. Ejemplo: intercambio comercial donde ambas naciones ganan al intercambiar excedentes de productos.
- La falacia de suma cero consiste en asumir erróneamente que toda interacción competitiva es de suma cero.

### Ejemplo práctico

Matriz de un juego 2x3 de suma cero:

|     | A       | B       | C       |
| --- | ------- | ------- | ------- |
| 1   | 30, -30 | -10, 10 | 20, -20 |
| 2   | -10, 10 | 20, -20 | -20, 20 |

- Jugador 1 elige entre 1 o 2, jugador 2 entre A, B o C.
- Si el primero elige 2 y el segundo B, el primero gana 20 y el segundo pierde 20.
- El razonamiento puramente determinista puede generar ciclos de anticipación mutua.

### Solución probabilística

- Von Neumann introdujo la **aleatorización de estrategias**: cada jugador asigna probabilidades a sus acciones.
- Estrategias óptimas calculadas minimizando la pérdida máxima esperada.
- En el ejemplo, las probabilidades óptimas son:

  - Jugador 1: 1 → 57%, 2 → 43%
  - Jugador 2: A → 0%, B → 57%, C → 43%

- Resultado esperado: jugador 1 obtiene +2,85 puntos por juego.

Esto muestra cómo los juegos de suma cero **transforman la competencia directa en un problema de optimización probabilística**, garantizando estrategias racionales incluso cuando los jugadores se anticipan mutuamente.
