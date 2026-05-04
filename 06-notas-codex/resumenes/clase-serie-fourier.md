# Clase: Serie de Fourier en Tiempo Continuo

## Objetivo

Entender la Serie de Fourier en tiempo continuo con foco en ejercicios de parcial:

- que representa
- como se calcula
- como se interpreta
- propiedades utiles
- atajos de ejercicios
- errores tipicos

---

## 1. Idea central

La Serie de Fourier sirve para representar una señal periodica como suma de exponenciales complejas, o equivalentemente, de senos y cosenos.

Si \(x(t)\) es periodica de periodo \(T_0\), entonces

\[
x(t)=\sum_{k=-\infty}^{\infty} a_k e^{jk\omega_0 t}
\]

donde

\[
\omega_0=\frac{2\pi}{T_0}
\]

es la frecuencia angular fundamental.

Idea conceptual:

\[
\text{una señal periodica se descompone en armonicos}
\]

Cada termino \(e^{jk\omega_0 t}\) corresponde al armonico \(k\).

---

## 2. Cuándo se usa

La Serie de Fourier continua se usa cuando la señal es:

- de tiempo continuo
- periodica

Si la señal no es periodica, no corresponde Serie de Fourier continua sino, en general, Transformada de Fourier.

---

## 3. Forma exponencial

La forma principal para el parcial suele ser:

\[
x(t)=\sum_{k=-\infty}^{\infty} a_k e^{jk\omega_0 t}
\]

con coeficientes

\[
a_k=\frac{1}{T_0}\int_{t_0}^{t_0+T_0} x(t)e^{-jk\omega_0 t}\,dt
\]

Importante:

- el intervalo de integracion puede ser cualquier periodo completo
- no hace falta integrar siempre de \(0\) a \(T_0\)

Por ejemplo, tambien puede usarse:

\[
a_k=\frac{1}{T_0}\int_{-T_0/2}^{T_0/2} x(t)e^{-jk\omega_0 t}\,dt
\]

si eso simplifica la cuenta.

---

## 4. Significado de los coeficientes

Los \(a_k\) indican cuanto peso tiene cada armonico en la señal.

- \(a_0\): componente continua o valor medio
- \(a_1\), \(a_{-1}\): primer armonico
- \(a_2\), \(a_{-2}\): segundo armonico
- etc.

El termino \(a_0\) vale:

\[
a_0=\frac{1}{T_0}\int_{t_0}^{t_0+T_0}x(t)\,dt
\]

o sea, el valor promedio de la señal en un periodo.

---

## 5. Interpretacion espectral

La Serie de Fourier genera un espectro discreto: solo hay energia en

\[
\omega=k\omega_0,\qquad k\in\mathbb{Z}
\]

Entonces:

- en tiempo hay una señal periodica
- en frecuencia hay lineas discretas

Esto conecta muy bien con sistemas LIT, porque cada armonico se procesa por separado.

---

## 6. Forma trigonometrica

A veces tambien se usa:

\[
x(t)=A_0+\sum_{k=1}^{\infty}\left[A_k\cos(k\omega_0 t)+B_k\sin(k\omega_0 t)\right]
\]

pero para sistemas y señales suele convenir mas la forma exponencial porque:

- simplifica cuentas
- conecta directo con \(H(j\omega)\)
- hace mas limpio el analisis entrada-salida

---

## 7. Como resolver ejercicios

### Paso 1: verificar periodicidad

Primero preguntar:

\[
\text{¿la señal es periodica?}
\]

Si si, hallar \(T_0\).

### Paso 2: hallar \(T_0\) y \(\omega_0\)

\[
\omega_0=\frac{2\pi}{T_0}
\]

### Paso 3: escribir la formula de \(a_k\)

\[
a_k=\frac{1}{T_0}\int_{t_0}^{t_0+T_0}x(t)e^{-jk\omega_0 t}\,dt
\]

### Paso 4: elegir un periodo comodo

Conviene elegir el periodo donde \(x(t)\) tenga la forma mas simple.

### Paso 5: integrar por tramos si hace falta

Si la señal cambia de expresion dentro del periodo, se separa la integral.

### Paso 6: simplificar usando propiedades

Muchas veces no hace falta recalcular todo desde cero.

---

## 8. Periodicidad

### 8.1 Una sola sinusoide

Si

\[
x(t)=\cos(\omega t+\phi)
\]

entonces

\[
T_0=\frac{2\pi}{\omega}
\]

### 8.2 Suma de sinusoides

Si hay varias, la señal es periodica solo si sus frecuencias son conmensurables.

Por ejemplo:

\[
x(t)=\cos(t)+\cos(2t)
\]

es periodica.

Pero

\[
x(t)=\cos(t)+\cos(\sqrt{2}\,t)
\]

no es periodica.

### 8.3 Exponenciales complejas

Si aparece

\[
e^{j\omega t}
\]

el periodo es

\[
T_0=\frac{2\pi}{\omega}
\]

---

## 9. Ejemplo basico

Sea

\[
x(t)=\cos(\omega_0 t)
\]

Usando Euler:

\[
\cos(\omega_0 t)=\frac{1}{2}e^{j\omega_0 t}+\frac{1}{2}e^{-j\omega_0 t}
\]

Entonces:

\[
a_1=\frac{1}{2},\qquad a_{-1}=\frac{1}{2}
\]

y

\[
a_k=0 \qquad \text{para } k\neq \pm 1
\]

Muchas veces conviene pasar primero a forma exponencial.

---

## 10. Otro ejemplo clasico

Sea

\[
x(t)=2+\cos(t)+3\sin(2t)
\]

Usando Euler:

\[
\cos(t)=\frac{1}{2}e^{jt}+\frac{1}{2}e^{-jt}
\]

\[
\sin(2t)=\frac{e^{j2t}-e^{-j2t}}{2j}
\]

Entonces:

- \(a_0=2\)
- \(a_1=\frac{1}{2}\)
- \(a_{-1}=\frac{1}{2}\)
- \(a_2=\frac{3}{2j}\)
- \(a_{-2}=-\frac{3}{2j}\)

y el resto vale cero.

---

## 11. Propiedades importantes

### Linealidad

Si

\[
x(t)=\alpha x_1(t)+\beta x_2(t)
\]

entonces

\[
a_k=\alpha a_k^{(1)}+\beta a_k^{(2)}
\]

### Desplazamiento temporal

Si

\[
y(t)=x(t-t_0)
\]

entonces

\[
b_k=a_k e^{-jk\omega_0 t_0}
\]

### Modulación

Si

\[
y(t)=x(t)e^{jm\omega_0 t}
\]

entonces

\[
b_k=a_{k-m}
\]

### Derivacion

Si

\[
y(t)=\frac{d}{dt}x(t)
\]

entonces

\[
b_k=jk\omega_0 a_k
\]

### Integracion

Si \(y(t)\) es una integral de \(x(t)\), aparecen factores del tipo

\[
\frac{1}{jk\omega_0}
\qquad \text{para } k\neq 0
\]

### Conjugacion

Si

\[
y(t)=x^*(t)
\]

entonces

\[
b_k=a_{-k}^*
\]

---

## 12. Propiedades por simetria

### Señal real

Si \(x(t)\) es real:

\[
a_{-k}=a_k^*
\]

### Señal real y par

Si \(x(t)\) es real y par:

- \(a_k\) es real
- el espectro es simetrico

### Señal real e impar

Si \(x(t)\) es real e impar:

- \(a_k\) es puramente imaginario
- \(a_0=0\)

Estas propiedades ahorran mucho tiempo en ejercicios teoricos.

---

## 13. Relacion con sistemas LIT

Si la entrada es periodica y el sistema es LIT con respuesta en frecuencia \(H(j\omega)\), entonces cada armonico se procesa por separado.

Si

\[
x(t)=\sum_{k=-\infty}^{\infty} a_k e^{jk\omega_0 t}
\]

entonces la salida es

\[
y(t)=\sum_{k=-\infty}^{\infty} a_k H(jk\omega_0)e^{jk\omega_0 t}
\]

O sea, los coeficientes de salida son

\[
b_k=a_k H(jk\omega_0)
\]

Interpretacion:

- la frecuencia no cambia
- cambia amplitud y fase de cada armonico

---

## 14. Ayudas practicas para parcial

### Ayuda 1

Si la señal ya viene como suma de senos, cosenos o exponenciales, no empieces integrando.

### Ayuda 2

Si te piden solo algunos coeficientes, no hace falta reconstruir toda la serie.

### Ayuda 3

Si la señal es un corrimiento temporal, usar:

\[
b_k=a_k e^{-jk\omega_0 t_0}
\]

### Ayuda 4

Si la salida de un sistema LIT es periodica:

\[
b_k=a_k H(jk\omega_0)
\]

### Ayuda 5

Antes de integrar, mirar si la señal tiene:

- simetria par
- simetria impar
- valor medio evidente
- forma exponencial casi hecha

---

## 15. Errores tipicos

### Error 1

Usar Serie de Fourier en una señal no periodica.

### Error 2

Confundir \(T_0\) con \(\omega_0\).

\[
\omega_0=\frac{2\pi}{T_0}
\]

### Error 3

Olvidar el signo del exponente:

\[
a_k=\frac{1}{T_0}\int x(t)e^{-jk\omega_0 t}dt
\]

### Error 4

Integrar en un intervalo que no cubre un periodo completo.

### Error 5

No usar propiedades de simetria.

### Error 6

En sistemas LIT, olvidar evaluar en

\[
\omega=k\omega_0
\]

---

## 16. Checklist minimo

Deberias poder:

- decidir si una señal admite Serie de Fourier
- hallar \(T_0\) y \(\omega_0\)
- calcular \(a_0\)
- obtener coeficientes de señales simples
- pasar senos y cosenos a exponenciales
- usar corrimiento temporal y simetria
- hallar coeficientes de salida en sistemas LIT

---

## 17. Resumen express

Si \(x(t)\) es periodica:

\[
x(t)=\sum_{k=-\infty}^{\infty} a_k e^{jk\omega_0 t}
\]

\[
a_k=\frac{1}{T_0}\int_{t_0}^{t_0+T_0}x(t)e^{-jk\omega_0 t}\,dt
\]

\[
\omega_0=\frac{2\pi}{T_0}
\]

Si el sistema es LIT:

\[
b_k=a_k H(jk\omega_0)
\]

Si \(x(t)\) es real:

\[
a_{-k}=a_k^*
\]

Si hay corrimiento temporal:

\[
x(t-t_0)\quad \Longrightarrow \quad a_k e^{-jk\omega_0 t_0}
\]

---

## 18. Cierre

La Serie de Fourier dice que una señal periodica puede pensarse como suma de frecuencias elementales.

En parcial, casi todo termina en una de estas dos ideas:

- descomponer bien la señal en armonicos
- usar que un sistema LIT trata cada armonico por separado
