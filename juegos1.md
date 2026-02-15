## 🎯 ¿Qué es la teoría de juegos?

La **teoría de juegos** analiza matemáticamente situaciones de **interacción estratégica**: contextos donde tu resultado depende de **tus decisiones y de las decisiones de otros**.

No compites contra un entorno pasivo, sino contra **agentes que también eligen, anticipan y reaccionan**.

Ejemplos directos:

- Ajedrez: cada movimiento responde al del rival.
- Negociación salarial: cada parte ajusta su oferta según la otra.
- Empresas fijando precios: una baja provoca respuestas en cadena.

---

## 🧩 Componentes básicos de un juego

Todo modelo de teoría de juegos define con precisión:

1. **Jugadores**
   Los agentes que toman decisiones.

2. **Estrategias**
   El conjunto de acciones posibles para cada jugador.

3. **Pagos (utilidades)**
   El beneficio o coste que recibe cada jugador según la combinación de estrategias.

Estos tres elementos convierten una situación real en un **modelo formal analizable**.

---

## 🗂️ Tipos principales de juegos

La teoría de juegos clasifica los problemas según varias dimensiones:

| Dimensión       | Tipos                          | Qué significa                                          |
| --------------- | ------------------------------ | ------------------------------------------------------ |
| **Relación**    | Cooperativos / No cooperativos | ¿Se permiten acuerdos vinculantes o no?                |
| **Momento**     | Simultáneos / Secuenciales     | ¿Se decide a la vez o por turnos?                      |
| **Información** | Completa / Incompleta          | ¿Conoces las reglas y tipos de los demás?              |
| **Resultado**   | Suma cero / Suma no-cero       | ¿Lo que uno gana lo pierde otro, o pueden ganar ambos? |

---

## 🧠 Idea clave

La teoría de juegos no estudia “qué es lo mejor”, sino **qué es racional cuando otros también razonan**.

Es un lenguaje para entender:

- conflictos,
- cooperación,
- competencia,
- negociación,
- evolución social.

---

## 🧩 El Dilema del Prisionero

Dos sospechosos son detenidos por un delito.
La policía los interroga **por separado** y les ofrece el mismo trato:

- **Confesar (traicionar)**
- **Callar (cooperar)**

No pueden comunicarse.

---

## 📊 Matriz de pagos

|                | Prisionero B calla    | Prisionero B confiesa |
| -------------- | --------------------- | --------------------- |
| **A calla**    | A: 2 años · B: 2 años | A: 10 años · B: 0     |
| **A confiesa** | A: 0 · B: 10 años     | A: 5 años · B: 5 años |

(Recuerda: **menos años = mejor pago**)

---

## 🧠 Análisis racional

Miremos desde A:

- Si B **calla** → A mejora confesando (0 < 2)
- Si B **confiesa** → A mejora confesando (5 < 10)

**Confesar domina siempre.**

Lo mismo ocurre para B.

---

## 🎯 Equilibrio de Nash

Ambos confiesan → **(5, 5)**
Nadie puede mejorar cambiando solo su decisión.

Pero…

---

## 💥 La paradoja

Si ambos callaran → **(2, 2)**
Los dos estarían mejor, pero la lógica individual lo impide.

---

## 🔑 Idea central

> La racionalidad individual puede producir resultados colectivamente peores.

Esto explica por qué aparecen:

- guerras de precios,
- sobreexplotación de recursos,
- desconfianza estructural,
- sabotaje mutuo.

---

## 🔁 Cómo emerge la cooperación (Dilema del Prisionero Repetido)

Cuando el dilema no ocurre una sola vez, sino **muchas veces con los mismos jugadores**, todo cambia.

Ya no maximizas _este turno_.
Maximizas **la relación futura**.

---

## 🧠 Nueva lógica estratégica

En un juego repetido, cada decisión:

- castiga o recompensa al otro,
- construye reputación,
- crea expectativas,
- altera su conducta futura.

Ahora traicionar tiene un **coste acumulado**.

---

## 🎯 Estrategia clave: _Tit for Tat_

Regla simple:

1. Empieza cooperando
2. Luego copia la última jugada del otro

Propiedades:

- **Amable**: nunca traiciona primero
- **Vengativa**: castiga de inmediato
- **Perdonadora**: vuelve a cooperar si el otro coopera
- **Transparente**: el otro entiende tu lógica

Resultado: domina en torneos iterados.

---

## 📈 Condición matemática

La cooperación es racional si:

[
\delta > \frac{T - R}{T - P}
]

Donde:

- ( \delta ) = cuánto valoras el futuro
- ( T ) = tentación de traicionar
- ( R ) = recompensa mutua
- ( P ) = castigo mutuo

Traducción:

> si el futuro importa lo suficiente, cooperar es la mejor estrategia.

---

# 🧠 Juegos con Información Incompleta y Reputación

## 1) Información incompleta

Un juego tiene **información incompleta** cuando al menos un jugador **desconoce el tipo, incentivos o costes reales del otro**.

Formalmente:

- Existe un conjunto de **tipos** ( \theta_i ) para cada jugador.
- Cada jugador conoce su tipo, pero no el de los demás.
- Las creencias se representan con una distribución ( \mu(\theta) ).

Esto convierte el juego en un **juego bayesiano**.

---

## 2) El problema central

El jugador no responde a una acción, sino a una **creencia** sobre quién es el otro.

> La estrategia óptima maximiza utilidad esperada, no pagos directos.

[
\max*{s_i} ; \mathbb{E}*{\theta*{-i}}[u_i(s_i, s*{-i}, \theta)]
]

---

## 3) Reputación como estado dinámico

En juegos repetidos con información incompleta:

- El tipo de un jugador (cooperador, oportunista, disciplinador) no se observa directamente.
- Sus acciones generan **señales**.
- Los demás actualizan creencias mediante **Bayes**.

[
\mu_{t+1}(\theta_i) = \frac{\mu_t(\theta_i), P(a_i^t \mid \theta_i)}{\sum_{\theta'} \mu_t(\theta'), P(a_i^t \mid \theta')}
]

La reputación es, por tanto, un **estado público endógeno**.

---

## 4) Efecto disciplinador

Aunque un tipo oportunista prefiera traicionar hoy, puede **imitar a un tipo cooperador** para preservar su reputación.

Esto genera:

> **Cooperación por imitación estratégica.**

No porque sea “bueno”, sino porque el futuro lo penaliza.

---

## 5) Equilibrio reputacional

En un **equilibrio bayesiano secuencial**:

- Las acciones son óptimas dado un sistema de creencias.
- Las creencias se actualizan racionalmente.
- La reputación disciplina comportamientos desviados.

Resultado:

> la posibilidad de ser observado en el futuro puede sostener cooperación incluso entre oportunistas.

---

## 6) Implicación estructural

Para inducir cooperación en entornos reales:

- Hacer **observables** las acciones.
- Crear **memoria institucional**.
- Establecer **trayectorias de reputación**.
- Penalizar rupturas creíbles.

Diseña el flujo de información → transformas el equilibrio.
