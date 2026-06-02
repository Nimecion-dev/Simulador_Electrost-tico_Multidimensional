# Simulador Electrostático 1D/2D

## Descripción del proyecto

Este proyecto consiste en una aplicación web interactiva que permite simular un sistema de cargas eléctricas puntuales en una y dos dimensiones. El simulador calcula la fuerza eléctrica entre cargas mediante la Ley de Coulomb, la fuerza neta sobre una carga seleccionada y el campo eléctrico en un punto definido por el usuario.

La aplicación permite visualizar las cargas en un plano, observar vectores de fuerza, activar una malla de campo eléctrico y analizar los resultados numéricos desde la interfaz.

## Objetivo

Desarrollar una herramienta computacional que facilite el análisis y la visualización de sistemas electrostáticos con cargas puntuales, aplicando los conceptos físicos de fuerza eléctrica, campo eléctrico y superposición vectorial.

## Funcionalidades principales

- Simulación de cargas eléctricas puntuales.
- Modo de trabajo en 1D y 2D.
- Agregado manual de cargas positivas y negativas.
- Selección de una carga para calcular la fuerza neta sobre ella.
- Evaluación del campo eléctrico en un punto definido por el usuario.
- Visualización de vectores de fuerza eléctrica.
- Visualización de vectores de campo eléctrico.
- Malla de campo eléctrico.
- Interfaz gráfica interactiva.
- Movimiento de cargas mediante arrastre con el mouse.
- Panel de cálculos con resultados numéricos.

## Modelo físico utilizado

El simulador se basa en la Ley de Coulomb:

```text
F = k · |q1 · q2| / r²
```

Donde:

- `F` es la magnitud de la fuerza eléctrica.
- `k = 8.987551 × 10^9 N·m²/C²` es la constante de Coulomb.
- `q1` y `q2` son las cargas eléctricas en coulombs.
- `r` es la distancia entre las cargas en metros.

Para sistemas con varias cargas, se aplica el principio de superposición, sumando vectorialmente las fuerzas o los campos generados por cada carga.

## Tecnologías utilizadas

El proyecto fue desarrollado con tecnologías web nativas:

- HTML5
- CSS3
- JavaScript
- Canvas API

No se requieren librerías externas.

## Requisitos de instalación

Para ejecutar el simulador solo se necesita un navegador web moderno, por ejemplo:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Opera

No es necesario instalar dependencias adicionales.

## Instrucciones de ejecución

1. Descargar o clonar la carpeta del proyecto.
2. Abrir el archivo `index.html`.
3. Ejecutarlo directamente en el navegador dando doble clic sobre el archivo.

También puede abrirse desde Visual Studio Code usando la extensión Live Server, aunque no es obligatorio.

## Estructura del proyecto

```text
simulador_electrostatico_entrega_100/
│
├── index.html
├── README.md
├── casos_prueba.md
│
├── reporte/
│   ├── Reporte_Tecnico_Simulador_Electrostatico.docx
│   └── Reporte_Tecnico_Simulador_Electrostatico.pdf
│
└── evidencias/
    ├── caso_1d.png
    ├── caso_2d.png
    └── campo_electrico.png
```

## Uso del simulador

### Agregar una carga

1. Seleccionar el modo de simulación: 1D o 2D.
2. Escribir el valor de la carga en microcoulombs.
3. Escribir la posición de la carga.
4. Presionar el botón **Agregar al Sistema**.

Las cargas positivas se muestran en rojo y las cargas negativas se muestran en verde. El programa no permite agregar cargas con valor igual a cero.

### Calcular fuerza neta

1. Agregar dos o más cargas al sistema.
2. Seleccionar una carga haciendo clic sobre ella.
3. El simulador mostrará la fuerza neta sobre la carga seleccionada.
4. El vector de fuerza neta se representa visualmente en el plano.

### Evaluar campo eléctrico

1. Agregar una o más cargas.
2. Presionar el botón **Evaluar Punto P**.
3. Escribir las coordenadas del punto donde se desea evaluar el campo.
4. El programa mostrará el campo eléctrico total en ese punto.

### Activar malla de campo

Presionar el botón **Malla Campo** para mostrar una representación visual del campo eléctrico generado por las cargas.

## Casos de prueba resumidos

### Caso 1: Sistema 1D

- Modo: 1D
- Carga 1: `+2 µC` en `x = -1 m`
- Carga 2: `-3 µC` en `x = 1 m`
- Carga seleccionada: Carga 1
- Resultado esperado aproximado: `Fx = 1.35 × 10^-2 N` hacia la derecha.

### Caso 2: Sistema 2D

- Modo: 2D
- Carga 1: `+2 µC` en `(0, 0) m`
- Carga 2: `-2 µC` en `(2, 1) m`
- Carga 3: `+1 µC` en `(-1, 2) m`
- Carga seleccionada: Carga 1
- Resultado esperado aproximado: `|F_neta| = 8.04 × 10^-3 N`.

### Caso 3: Campo eléctrico

- Modo: 2D
- Carga 1: `+3 µC` en `(-1, 0) m`
- Carga 2: `-3 µC` en `(1, 0) m`
- Punto de evaluación: `(0, 1) m`
- Resultado esperado aproximado: `|E_total| = 1.91 × 10^4 N/C`.

## Interpretación física

El simulador permite observar que las cargas eléctricas interactúan dependiendo de su signo y separación. Las cargas del mismo signo se repelen, mientras que las cargas de signo contrario se atraen.

En un sistema con varias cargas, la fuerza neta sobre una carga no depende únicamente de una interacción aislada, sino de la suma vectorial de todas las fuerzas que actúan sobre ella. De la misma forma, el campo eléctrico en un punto es el resultado de la contribución de todas las cargas presentes en el sistema.

La visualización mediante vectores facilita la comprensión de la dirección y magnitud aproximada de las fuerzas y campos eléctricos.

## Autores

Proyecto desarrollado por:

- Luis Roberto García Sánchez
- Santiago Caleb Barron
- Agudelo Mancera Josue

## Notas

Este simulador fue desarrollado con fines educativos para representar de manera visual e interactiva conceptos básicos de electrostática.
