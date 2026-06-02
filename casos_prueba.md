# Casos de prueba del simulador electrostático

Este archivo documenta los tres casos de prueba solicitados para comprobar el funcionamiento del simulador en 1D, 2D y evaluación de campo eléctrico.

## Constante utilizada

```text
k = 8.987551 × 10^9 N·m²/C²
```

Las cargas se ingresan en microcoulombs (`µC`) desde la interfaz, pero internamente el programa las convierte a coulombs (`C`).

---

## Caso de prueba 1: Sistema en 1D

### Datos ingresados

- Modo: 1D
- Carga 1: `+2 µC` en `x = -1 m`
- Carga 2: `-3 µC` en `x = 1 m`
- Carga seleccionada: Carga 1

### Resultado esperado

La distancia entre las cargas es:

```text
r = 2 m
```

La magnitud de la fuerza es:

```text
F = k |q1 q2| / r²
F = (8.987551 × 10^9)(2 × 10^-6)(3 × 10^-6) / 2²
F ≈ 1.35 × 10^-2 N
```

Como las cargas son de signos opuestos, la interacción es atractiva. Por lo tanto, la fuerza sobre la carga 1 apunta hacia la derecha.

```text
Fx ≈ +1.35 × 10^-2 N
```

### Evidencia

Ver archivo:

```text
evidencias/caso_1d.png
```

---

## Caso de prueba 2: Sistema en 2D

### Datos ingresados

- Modo: 2D
- Carga 1: `+2 µC` en `(0, 0) m`
- Carga 2: `-2 µC` en `(2, 1) m`
- Carga 3: `+1 µC` en `(-1, 2) m`
- Carga seleccionada: Carga 1

### Resultado esperado

La fuerza neta sobre la carga 1 se obtiene mediante la suma vectorial de las interacciones con la carga 2 y la carga 3.

Resultado aproximado:

```text
ΣFx ≈ 8.04 × 10^-3 N
ΣFy ≈ 0.00 N
|F_neta| ≈ 8.04 × 10^-3 N
```

La fuerza neta queda dirigida principalmente hacia el eje X positivo.

### Evidencia

Ver archivo:

```text
evidencias/caso_2d.png
```

---

## Caso de prueba 3: Campo eléctrico en un punto

### Datos ingresados

- Modo: 2D
- Carga 1: `+3 µC` en `(-1, 0) m`
- Carga 2: `-3 µC` en `(1, 0) m`
- Punto de evaluación: `P(0, 1) m`

### Resultado esperado

El campo eléctrico total en el punto P se calcula sumando vectorialmente el campo producido por cada carga.

Resultado aproximado:

```text
Ex ≈ 1.91 × 10^4 N/C
Ey ≈ 0.00 N/C
|E_total| ≈ 1.91 × 10^4 N/C
```

En este caso, las componentes verticales se cancelan por simetría, mientras que las componentes horizontales se suman.

### Evidencia

Ver archivo:

```text
evidencias/campo_electrico.png
```
