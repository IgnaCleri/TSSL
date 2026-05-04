# Clase: Convolucion en Tiempo Continuo

## Objetivo

Entender la convolucion en tiempo continuo con foco en ejercicios de parcial:

- definicion
- interpretacion grafica
- propiedades
- atajos utiles
- errores tipicos
- criterios practicos para resolver ejercicios

---

## 1. Idea central

Si un sistema LIT tiene entrada \(x(t)\) y respuesta al impulso \(h(t)\), la salida es

\[
y(t)=x(t)*h(t)=\int_{-\infty}^{\infty}x(\tau)\,h(t-\tau)\,d\tau
\]

Interpretacion:

- \(x(\tau)\): entrada
- \(h(t-\tau)\): respuesta al impulso invertida y desplazada
- la integral suma el producto donde ambas señales se superponen

La convolucion responde:

\[
\text{"si conozco la entrada y conozco } h(t) \text{, cual es la salida?"}
\]

---

## 2. Interpretacion grafica

La receta grafica es siempre:

1. tomar \(h(\tau)\)
2. invertirla: \(h(-\tau)\)
3. desplazarla: \(h(t-\tau)\)
4. mirar donde se superpone con \(x(\tau)\)
5. integrar el producto en la zona comun

La clave del ejercicio suele estar en detectar bien la zona de superposicion.

---

## 3. Definicion formal

\[
(x*h)(t)=\int_{-\infty}^{\infty}x(\tau)h(t-\tau)\,d\tau
\]

Tambien puede escribirse como

\[
(x*h)(t)=\int_{-\infty}^{\infty}x(t-\tau)h(\tau)\,d\tau
\]

Esto anticipa la propiedad conmutativa:

\[
x(t)*h(t)=h(t)*x(t)
\]

---

## 4. Zona de superposicion

Si

\[
x(\tau)\neq 0 \text{ en } [a,b]
\qquad\text{y}\qquad
h(t-\tau)\neq 0 \text{ en } [c(t),d(t)]
\]

entonces la integral real vive en

\[
[\max(a,c(t)),\min(b,d(t))]
\]

Si ese intervalo queda vacio:

\[
y(t)=0
\]

Esta idea resuelve gran parte de los ejercicios.

---

## 5. Propiedades importantes

### Conmutatividad

\[
x*h=h*x
\]

Sirve para elegir el orden mas comodo.

### Asociatividad

\[
x*(h_1*h_2)=(x*h_1)*h_2
\]

Sirve en sistemas en cascada.

### Distributividad

\[
x*(h_1+h_2)=x*h_1+x*h_2
\]

Sirve en sistemas paralelos.

### Elemento neutro

\[
x(t)*\delta(t)=x(t)
\]

Mas general:

\[
x(t)*\delta(t-t_0)=x(t-t_0)
\]

### Escalado

\[
x*(a\,h)=a(x*h)
\]

### Derivacion

\[
\frac{d}{dt}(x*h)=\left(\frac{dx}{dt}\right)*h=x*\left(\frac{dh}{dt}\right)
\]

---

## 6. Casos fundamentales

### 6.1 Convolucion con delta

\[
x(t)*\delta(t-t_0)=x(t-t_0)
\]

Si

\[
h(t)=\delta(t+2)+2\delta(t-1)
\]

entonces

\[
y(t)=x(t+2)+2x(t-1)
\]

No conviene integrar: se usa propiedad.

### 6.2 Rectangulo con rectangulo

Cuando dos pulsos rectangulares se convolucionan, el resultado suele ser triangular o trapezoidal:

- primero crece la superposicion
- luego puede mantenerse
- finalmente decrece

### 6.3 Señal con escalon

Como el escalon "acumula":

\[
x(t)*u(t)=\int_{-\infty}^{t}x(\tau)\,d\tau
\]

porque \(u(t-\tau)=1\) cuando \(\tau\le t\).

---

## 7. Procedimiento practico

### Metodo general

1. escribir la integral

\[
y(t)=\int_{-\infty}^{\infty}x(\tau)h(t-\tau)\,d\tau
\]

2. determinar donde vale algo \(x(\tau)\)
3. determinar donde vale algo \(h(t-\tau)\)
4. intersectar ambos intervalos
5. separar por casos de \(t\)
6. integrar en cada caso
7. verificar que el resultado tenga sentido grafico

---

## 8. Como sacar intervalos sin confundirse

Si

\[
x(\tau)=1 \quad \text{para } 0\le \tau \le 1
\]

y

\[
h(t-\tau)=1 \quad \text{para } 1\le t-\tau \le 2
\]

despejamos:

\[
1\le t-\tau \le 2
\]

\[
1-t\le -\tau \le 2-t
\]

\[
t-1\ge \tau \ge t-2
\]

ordenando:

\[
t-2\le \tau \le t-1
\]

Entonces:

- \(x(\tau)\) vive en \([0,1]\)
- \(h(t-\tau)\) vive en \([t-2,t-1]\)

La superposicion es

\[
[\max(0,t-2),\min(1,t-1)]
\]

---

## 9. Mini ejemplo clasico

Sea

\[
x(t)=
\begin{cases}
1, & 0\le t\le 1 \\
0, & \text{otro caso}
\end{cases}
\qquad
h(t)=
\begin{cases}
1, & 1\le t\le 2 \\
0, & \text{otro caso}
\end{cases}
\]

Entonces

\[
y(t)=x*h
\]

Por casos:

- si \(t<1\), no hay superposicion
- si \(1\le t\le 2\), la superposicion crece
- si \(2\le t\le 3\), la superposicion decrece
- si \(t>3\), no hay superposicion

Resultado:

\[
y(t)=
\begin{cases}
0, & t<1 \\
t-1, & 1\le t\le 2 \\
-t+3, & 2\le t\le 3 \\
0, & t>3
\end{cases}
\]

---

## 10. Ayudas practicas para parcial

### Ayuda 1

Si aparece \(\delta\), casi seguro conviene usar propiedades.

### Ayuda 2

Si ambas señales son rectangulares o triangulares, pensá primero la forma final:

- crece
- puede mantenerse
- decrece

### Ayuda 3

Antes de integrar, buscá para qué valores de \(t\) la salida puede ser distinta de cero.

Si

\[
x(t)\neq 0 \text{ en } [a,b]
\qquad\text{y}\qquad
h(t)\neq 0 \text{ en } [c,d]
\]

entonces tipicamente

\[
y(t)\neq 0 \text{ en } [a+c,b+d]
\]

### Ayuda 4

Si el sistema es paralelo:

\[
h(t)=h_1(t)+h_2(t)
\]

Si es cascada:

\[
h(t)=h_1(t)*h_2(t)
\]

### Ayuda 5

Si el resultado da raro, revisar:

- signo al invertir
- limites de integracion
- intervalo real de superposicion

---

## 11. Errores tipicos

### Error 1

No invertir la señal antes de desplazar.

\[
h(\tau)\to h(-\tau)\to h(t-\tau)
\]

### Error 2

Mover \(h(\tau-t)\) en lugar de \(h(t-\tau)\).

### Error 3

No separar por casos de \(t\).

### Error 4

Integrar donde no hay superposicion.

### Error 5

No usar propiedades con deltas.

---

## 12. Checklist minimo de parcial

Deberias poder:

- escribir la definicion correctamente
- explicar la interpretacion grafica
- resolver convoluciones simples por tramos
- usar deltas desplazadas
- analizar sistemas LIT con respuesta al impulso
- combinar sistemas paralelos y en cascada
- detectar soporte de la salida
- verificar si el resultado tiene forma razonable

---

## 13. Resumen express

\[
y(t)=x(t)*h(t)=\int_{-\infty}^{\infty}x(\tau)h(t-\tau)\,d\tau
\]

Ideas clave:

- invertir y desplazar
- buscar superposicion
- integrar solo donde se pisan
- separar por casos
- usar propiedades cuando haya deltas

Atajos:

\[
x*\delta=x
\]

\[
x*\delta(t-t_0)=x(t-t_0)
\]

\[
x*h=h*x
\]

\[
\text{soporte}(y)=\text{soporte}(x)+\text{soporte}(h)
\]

---

## 14. Cierre

Convolucionar es mezclar la entrada con la respuesta al impulso del sistema.

En ejercicios de parcial esto casi siempre termina en una de dos:

- calcular una superposicion que cambia con \(t\)
- usar propiedades para evitar la integral
