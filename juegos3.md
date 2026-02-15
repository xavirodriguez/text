# Teoría de juegos: cómo la estrategia modela la cooperación

La **teoría de juegos** estudia matemáticamente situaciones en las que el resultado de cada participante depende de sus decisiones y de las decisiones de los demás. No se trata de competir contra un entorno pasivo, sino contra **agentes que también eligen, anticipan y reaccionan**.

Ejemplos cotidianos: el ajedrez, donde cada movimiento responde al rival; una negociación salarial, donde cada parte ajusta su oferta según la otra; o las empresas fijando precios, donde una baja provoca reacciones en cadena.

---

## Componentes básicos

Todo juego se define a través de tres elementos:

1. **Jugadores**: los agentes que toman decisiones.
2. **Estrategias**: el conjunto de acciones posibles.
3. **Pagos o utilidades**: beneficios o costes que recibe cada jugador según la combinación de estrategias.

Estos elementos permiten convertir situaciones reales en modelos formales, analizables y comparables.

---

## Tipos de juegos

La teoría de juegos clasifica los escenarios según distintas dimensiones:

| Dimensión   | Tipos                          | Qué significa                                          |
| ----------- | ------------------------------ | ------------------------------------------------------ |
| Relación    | Cooperativos / No cooperativos | ¿Se permiten acuerdos vinculantes o no?                |
| Momento     | Simultáneos / Secuenciales     | ¿Se decide a la vez o por turnos?                      |
| Información | Completa / Incompleta          | ¿Conoces las reglas y tipos de los demás?              |
| Resultado   | Suma cero / Suma no-cero       | ¿Lo que uno gana lo pierde otro, o pueden ganar ambos? |

La clave: **la racionalidad individual no siempre genera el mejor resultado colectivo**.

---

## El Dilema del Prisionero

Dos sospechosos son detenidos y interrogados **por separado**. Cada uno puede:

- **Confesar (traicionar)**
- **Callar (cooperar)**

No pueden comunicarse entre sí.

### Matriz de pagos

|                | B calla         | B confiesa      |
| -------------- | --------------- | --------------- |
| **A calla**    | 2 años · 2 años | 10 años · 0     |
| **A confiesa** | 0 · 10 años     | 5 años · 5 años |

Menos años equivale a mejor resultado.

### Análisis racional

Para A:

- Si B calla → conviene confesar (0 < 2).
- Si B confiesa → conviene confesar (5 < 10).

El mismo razonamiento aplica a B. **Confesar domina siempre**, resultando en un **equilibrio de Nash (5,5)**.

Paradoja: si ambos callaran (2,2) mejorarían colectivamente, pero la lógica individual lo impide.

---

## Juegos repetidos y cooperación

Cuando el dilema se repite entre los mismos jugadores, cambia la lógica. Ahora se maximiza **la relación futura**, no solo la ganancia inmediata.

### Estrategia Tit for Tat

1. Cooperar primero.
2. Copiar la última acción del otro.

Propiedades:

- Amable: nunca traiciona primero.
- Vengativa: castiga inmediatamente si el otro traiciona.
- Perdonadora: vuelve a cooperar si el otro coopera.
- Transparente: el otro entiende la lógica.

Esta estrategia domina en torneos iterados, porque **la reputación importa**.

### Factor de descuento

[
\delta > \frac{T - R}{T - P}
]

- (\delta) = valor del futuro / paciencia
- T = tentación de traicionar
- R = recompensa mutua
- P = castigo mutuo

Si el futuro pesa lo suficiente, **cooperar es la decisión racional**.

---

## Información incompleta y reputación

Un juego tiene **información incompleta** cuando un jugador desconoce los incentivos o tipos del otro.

- Cada tipo se representa como (\theta_i).
- Cada jugador conoce su tipo, pero no el de los demás.
- Las creencias se representan mediante distribuciones (\mu(\theta)).

En este contexto, la **estrategia óptima** maximiza la utilidad esperada basada en creencias, no en pagos directos.

[
\max*{s_i} \mathbb{E}*{\theta*{-i}}[u_i(s_i, s*{-i}, \theta)]
]

La reputación actúa como **memoria pública dinámica**. Incluso los oportunistas pueden imitar cooperadores para mantener buena reputación, lo que genera cooperación estratégica.

---

## Señalización y cribado

### Señalización

- Actúa quien conoce su tipo.
- Revela su tipo mediante una acción costosa.
- Los tipos se separan si los incentivos son correctos.

### Cribado

- Actúa quien desconoce el tipo del otro.
- Diseña opciones que inducen al otro a autoseleccionarse.
- Funciona mediante contratos o menús, cumpliendo restricciones de incentivo y participación.

Principio: **no se fuerza la información, se diseña para que se revele sola**.

---

## Compromisos creíbles

Un compromiso es **creíble** cuando, tras asumirlo, **desviarse deja de ser rentable**.

Métodos:

- **Autolimitación**: reducir el espacio estratégico disponible.
- **Reglas automáticas**: acciones contingentes ejecutadas sin discreción.
- **Garantías externas**: árbitros o verificadores.

Esto convierte la cooperación en **equilibrio sub-juego perfecto**, estable sin depender de la moralidad.

---

## Equilibrio de Nash vs. óptimo de Pareto

- **Equilibrio de Nash**: estable ante desviaciones individuales.
- **Óptimo de Pareto**: eficiente colectivamente.

En el Dilema del Prisionero:

- Nash: (5,5), estable pero ineficiente.
- Pareto: (2,2), mejor para todos pero inestable.

El conflicto central es **entre estabilidad estratégica y eficiencia social**, no entre egoísmo y cooperación.

---

## Diseño de juegos e instituciones

Para sostener la cooperación, no basta la buena voluntad. Es necesario **estructurar incentivos y restricciones**:

1. Definir actores y tipos.
2. Ajustar la matriz de pagos para favorecer cooperación.
3. Introducir observabilidad y reputación.
4. Garantizar compromisos creíbles.
5. Coordinar expectativas en juegos con múltiples equilibrios (protocolos, normas, señales).

La cooperación depende de la **arquitectura del juego y la institución**, no de la moral de los jugadores.
