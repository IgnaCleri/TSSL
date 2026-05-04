# Ejercicios: Serie de Fourier en Tiempo Continuo

## Como usar esta guia

Orden sugerido:

1. ejercicios directos de coeficientes
2. ejercicios de periodo fundamental
3. ejercicios con sistemas LIT
4. ejercicios tipo parcial

Objetivo:

- hallar \(T_0\) y \(\omega_0\)
- calcular coeficientes \(a_k\)
- usar forma exponencial
- aprovechar simetrias
- resolver salida periodica de sistemas LIT

---

## 1. Guia de catedra: coeficientes directos

### Ejercicio 1

Determinar la frecuencia fundamental \(\omega_0\) y los coeficientes \(a_k\) de la Serie de Fourier para

\[
x(t)=\sin(3\pi t)
\]

**Fuente:** [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 2

Determinar \(\omega_0\) y los coeficientes \(a_k\) para

\[
x(t)=2+\cos\left(\frac{2\pi}{3}t\right)+4\sin\left(\frac{5\pi}{3}t\right)
\]

**Fuente:** [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 3

Determinar \(\omega_0\) y los coeficientes \(a_k\) para la señal periodica

\[
x(t)=
\begin{cases}
1.5, & 0\le t<1 \\
-1.5, & 1\le t<2
\end{cases}
\]

extendida periodicamente.

**Fuente:** [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 4

Determinar \(\omega_0\) y los coeficientes \(a_k\) para

\[
x(t)=\cos(4t)+\cos(7t)
\]

**Fuente:** [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 5

Determinar \(\omega_0\) y los coeficientes \(a_k\) para

\[
x(t)=1+\frac{1}{2}\cos(2\pi t)+\frac{2}{3}\cos(4\pi t)+\frac{1}{4}\cos(6\pi t)
\]

**Fuente:** [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

---

## 2. Guia de catedra: señales periodicas por forma

### Ejercicio 6

Encontrar el periodo fundamental y la Serie de Fourier asociada para la señal grafica 1 de la guia, considerando que es periodica.

**Fuente:** sección `(2)` de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 7

Encontrar el periodo fundamental y la Serie de Fourier asociada para la señal grafica 2 de la guia, considerando que es periodica.

**Fuente:** sección `(2)` de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 8

Encontrar el periodo fundamental y la Serie de Fourier asociada para la señal grafica 3 de la guia, considerando que es periodica.

**Fuente:** sección `(2)` de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 9

Encontrar el periodo fundamental y la Serie de Fourier asociada para la señal grafica 4 de la guia, considerando que es periodica.

**Fuente:** sección `(2)` de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

---

## 3. Sistemas LIT y Serie de Fourier

### Ejercicio 10

Encontrar los coeficientes \(a_k\) y \(b_k\) de la Serie de Fourier que representa la salida de un sistema LIT cuya respuesta al impulso es

\[
h(t)=e^{-4|t|}
\]

y verificar Parseval.

**Fuente:** Tema 2 de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 11

Encontrar los coeficientes \(a_k\) y \(b_k\) de la salida para el sistema LIT con

\[
h(t)=u(t)e^{-2t}
\]

y verificar Parseval.

**Fuente:** Tema 2 de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 12

Encontrar los coeficientes \(a_k\) y \(b_k\) de la salida para el sistema LIT con

\[
h(t)=\delta(t-3)+\delta(t+3)
\]

**Fuente:** Tema 2 de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

### Ejercicio 13

Encontrar los coeficientes \(a_k\) y \(b_k\) de la salida para el sistema LIT con

\[
h(t)=u(t)-u(t-1)
\]

**Fuente:** Tema 2 de [practico-03-guia-serie-fourier-resuelto-borgnino.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/01-cursada-actual/03-practicos/guias-catedra/practico-03-guia-serie-fourier-resuelto-borgnino.pdf)

---

## 4. Parciales y simulacros

### Ejercicio 14

Sea la señal periodica

\[
\tilde{x}(t)=2\cos\left(\frac{\pi}{3}t+\frac{\pi}{4}\right)+\sum_{k=-\infty}^{\infty}\delta(t+3k)
\]

que alimenta la entrada de dos sistemas LIT conectados en cascada, con

\[
h_1(t)=e^{-2(t-1)}u(t-2),
\qquad
h_2(t)=e^{-t}u(t+2)
\]

Se pide:

1. determinar el periodo \(T_0\) y la Serie de Fourier de \(\tilde{x}(t)\)
2. determinar \(H(j\omega)\)
3. hallar los coeficientes de la Serie de Fourier de la salida \(\tilde{y}(t)\)

**Fuente:** [parcial-01-2023-recuperatorio-comision-2.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2023-recuperatorio-comision-2.pdf)

### Ejercicio 15

Sea un sistema LIT con respuesta al impulso \(h(t)\) dada graficamente. Si la salida es

\[
\tilde{y}(t)=\cos\left(\frac{1}{2}t-\pi\right)+2\cos\left(\frac{1}{4}t\right)
\]

hallar los coeficientes de la Serie de Fourier de la entrada \(\tilde{x}(t)\).

**Fuente:** ejercicio 2(b) de [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 16

Misma idea que el anterior, pero con la variante B:

\[
\tilde{y}(t)=\cos\left(\frac{1}{3}t+\pi\right)+2\cos\left(\frac{1}{2}t\right)
\]

hallar los coeficientes de la Serie de Fourier de \(\tilde{x}(t)\).

**Fuente:** ejercicio 2(b) variante B en [parcial-01-2024-cursado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-cursado.pdf)

### Ejercicio 17

Sea la señal periodica \(\tilde{x}(t)\) dada en el enunciado del intensivo. Se pide:

1. calcular la Serie de Fourier de \(\tilde{x}(t)\)
2. calcular la serie de Fourier de salida del sistema LIT con

\[
h(t)=e^{-t}u(t-2)
\]

**Fuente:** [parcial-01-2024-intensivo-2024-02-09.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2024-intensivo-2024-02-09.pdf)

### Ejercicio 18

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

e identificar los coeficientes de la Serie de Fourier de salida.

Luego repetir para

\[
x_1(t)=e^{j\frac{3\pi}{2}t}+\frac{1}{2}e^{-j\frac{\pi}{2}t}
\]

**Fuente:** [parcial-01-2025-redictado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/01-primer-parcial/parcial-01-2025-redictado.pdf)

### Ejercicio 19

Sea

\[
x(t)=2+\cos\left(\frac{1}{2}t\right)+\cos(2t)+\cos\left(\frac{3}{4}t\right)
\]

y

\[
h(t)=\frac{2\sin(t)}{t}
\]

Se pide:

1. obtener la Serie de Fourier de la entrada \(x(t)\)
2. obtener la Serie de Fourier de la salida \(y(t)=x(t)*h(t)\)

**Fuente:** [simulacro-parcial-01-enunciado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/03-simulacros/simulacro-parcial-01-enunciado.pdf)

### Ejercicio 20

Para el mismo sistema del simulacro, calcular la salida si

\[
x(t)=\cos(6t)
\]

y explicar qué efecto produce el sistema sobre la señal de entrada.

**Fuente:** [simulacro-parcial-01-enunciado.pdf](/home/ignacio/Documents/Ignacio/Facultad/tercer-ano/primer-cuatrimestre/TSSL/02-parciales/03-simulacros/simulacro-parcial-01-enunciado.pdf)

---

## 5. Orden sugerido de practica

### Nivel 1

- Ejercicio 1
- Ejercicio 2
- Ejercicio 4
- Ejercicio 5

### Nivel 2

- Ejercicio 3
- Ejercicio 6
- Ejercicio 7
- Ejercicio 10
- Ejercicio 11

### Nivel 3

- Ejercicio 12
- Ejercicio 13
- Ejercicio 14
- Ejercicio 15
- Ejercicio 17
- Ejercicio 19
- Ejercicio 20

### Nivel 4

- Ejercicio 16
- Ejercicio 18

---

## 6. Sugerencia de resolucion

En cada ejercicio intentar siempre:

1. verificar periodicidad
2. hallar \(T_0\) y \(\omega_0\)
3. escribir la señal en forma exponencial si conviene
4. usar simetrias antes de integrar
5. si hay sistema LIT, aplicar

\[
b_k=a_k H(jk\omega_0)
\]

6. revisar siempre el coeficiente \(a_0\)

Si querés practicar en serio para parcial, conviene mezclar:

- un ejercicio puro de coeficientes
- uno de periodo
- uno de salida de sistema

en cada tanda.
