# Ejercicios: Convolucion en Tiempo Continuo

## Como usar esta guia

Orden sugerido:

1. guias de catedra
2. practicos tipo Oppenheim
3. ejercicios de parcial

Objetivo:

- practicar superposicion
- resolver por tramos
- usar propiedades con \(\delta(t)\)
- reconocer sistemas en paralelo y cascada

---

## 1. Guias de catedra

### Ejercicio 1

Resolver

\[
x(t)=
\begin{cases}
1, & 1\le t\le 2 \\
0, & \text{otro caso}
\end{cases}
\qquad
h(t)=
\begin{cases}
1, & 0\le t\le 1 \\
0, & \text{otro caso}
\end{cases}
\]

y hallar

\[
y(t)=x(t)*h(t)
\]

de forma analitica y grafica.

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

### Ejercicio 2

Resolver

\[
x(t)=
\begin{cases}
t+1, & 0\le t\le 1 \\
2-t, & 1<t\le 2 \\
0, & \text{otro caso}
\end{cases}
\qquad
h(t)=\delta(t+2)+2\delta(t+1)
\]

y obtener \(y(t)\) usando propiedades.

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

### Ejercicio 3

Resolver

\[
x(t)=u(t-3)-u(t-5)
\qquad
h(t)=e^{-3t}u(t)
\]

y expresar \(y(t)\) por tramos.

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

### Ejercicio 4

Resolver

\[
x(t)=e^{-t}u(t)
\qquad
h(t)=\delta(t-3)+3\delta(t+3)
\]

y simplificar el resultado todo lo posible.

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

### Ejercicio 5

Resolver

\[
x(t)=t e^{-\alpha t}u(t)
\qquad
h(t)=u(t)
\]

y obtener una expresion cerrada para \(y(t)\).

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

### Ejercicio 6

Resolver

\[
x(t)=2t\,[u(t+2)-u(t-2)]
\qquad
h(t)=u(t)-u(t-4)
\]

y dar \(y(t)\) por intervalos.

**Fuente:** [practico-02-guia-convolucion-continua-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-02-guia-convolucion-continua-resuelto-borgnino.pdf)

---

## 2. Practicos tipo Oppenheim

### Ejercicio 7

Resolver por convolucion:

\[
x(t)=e^{-\alpha t}u(t)
\qquad
h(t)=e^{-\beta t}u(t)
\]

hacer ambos casos:

- \(\alpha\neq\beta\)
- \(\alpha=\beta\)

**Fuente:** problema 2.22(a) en [libro-oppenheim-signals-and-systems-1996.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/03-bibliografia/01-libros-base/libro-oppenheim-signals-and-systems-1996.pdf), retomado en [practico-oppenheim-cap02-convolucion-continua.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/oppenheim/practico-oppenheim-cap02-convolucion-continua.pdf)

### Ejercicio 8

Resolver por convolucion:

\[
x(t)=u(t)-2u(t-2)+u(t-5)
\qquad
h(t)=e^{2t}u(1-t)
\]

y bosquejar la salida.

**Fuente:** problema 2.22(b) en [libro-oppenheim-signals-and-systems-1996.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/03-bibliografia/01-libros-base/libro-oppenheim-signals-and-systems-1996.pdf)

---

## 3. Parciales

### Ejercicio 9

Sea el sistema paralelo con

\[
x(t)=e^{-2t}u(t+3)
\]

\[
h_1(t)=1
\qquad
h_2(t)=-\frac{1}{2}u(t+4)+\frac{1}{2}u(t+2)
\]

Resolver

\[
y(t)=x(t)*h(t)
\]

por metodo de convolucion.

**Fuente:** [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 10

Sea el sistema en cascada con

\[
h_1(t)=\delta(t)-\delta(t-1)
\qquad
h_2(t)=-u(t+4)-u(t+2)+2u(t)
\]

Calcular la salida \(y(t)\) usando propiedades.

**Fuente:** [parcial-01-2024-recuperatorio-intensivo-2024-02-28.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-recuperatorio-intensivo-2024-02-28.pdf)

### Ejercicio 11

Sea el sistema paralelo con

\[
x(t)=u(t+5)
\]

\[
h_1(t)=e^{-2t}u(t-1)
\qquad
h_2(t)=e^t u(-t-5)
\]

Calcular

\[
y(t)=x(t)*h(t)
\]

**Fuente:** variante B en [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 12

Sea

\[
x(t)=2e^{j\frac{\pi}{2}t}
\qquad
h(t)=-u(t+1)+u(t+3)
\]

Calcular

\[
y(t)=x(t)*h(t)
\]

e identificar los coeficientes de la serie de Fourier de salida.

**Fuente:** [parcial-01-2025-redictado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2025-redictado.pdf)

### Ejercicio 13

Resolver la salida \(y(t)\) del sistema paralelo del simulacro y justificar:

- estabilidad
- causalidad
- memoria

Este ejercicio obliga a pensar intervalos de convolucion y trabajar por tramos.

**Fuente:** [simulacro-parcial-01-enunciado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/03-simulacros/simulacro-parcial-01-enunciado.pdf)

---

## 4. Orden sugerido de practica

### Nivel 1

- Ejercicio 1
- Ejercicio 2
- Ejercicio 4

### Nivel 2

- Ejercicio 3
- Ejercicio 5
- Ejercicio 6
- Ejercicio 7

### Nivel 3

- Ejercicio 8
- Ejercicio 9
- Ejercicio 10
- Ejercicio 11
- Ejercicio 12
- Ejercicio 13

---

## 5. Sugerencia de resolucion

En cada ejercicio intentar siempre:

1. escribir la integral o la propiedad a usar
2. detectar soporte de cada señal
3. hallar el soporte posible de la salida
4. separar por casos de \(t\)
5. recien despues integrar

Si aparece \(\delta(t)\), revisar primero si conviene evitar la integral.
