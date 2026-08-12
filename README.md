# Prueba Práctica — Unidad IV — Ingeniería de Requisitos (ISR-401)

Solución de las actividades P1–P8 del caso "Sistema de Gestión de Pedidos", desarrollada en LaTeX.

## Estructura del repositorio

```text
.
├── main.tex                          # Documento principal con la solución (carátula + P1–P8 + evidencia SGA)
├── figures/
│   ├── p1_clases.png                 # Diagrama de clases UML (P1)
│   ├── p2_actividades.png            # Diagrama de actividades UML (P2)
│   ├── p3_estados.png                # Máquina de estados UML (P3)
│   ├── evaluacion_formativa.png      # Evidencia de la evaluación en el SGA
│   └── revision_intento.png          # Evidencia de revisión/intento de la prueba
├── PruebaPractica_UnidadIV.pdf       # PDF compilado (entregable final)
└── README.md                         # Este archivo
```

## Contenido del documento

* **Carátula:** datos de identificación del estudiante y URL del repositorio en una sola línea.
* **P1:** Modelo de datos — Diagrama de clases UML.
* **P2:** Modelo funcional — Diagrama de actividades UML.
* **P3:** Modelo de comportamiento — Máquina de estados UML.
* **P4:** Consistencia entre las tres perspectivas.
* **P5:** Especificación de requisitos con esquema de atributos.
* **P6:** Priorización MoSCoW.
* **P7:** Validación por inspección (ISO/IEC/IEEE 29148).
* **P8:** Pruebas de aceptación trazadas.
* **Evidencia final:** captura del resultado de la evaluación formativa en el SGA.

## Requisitos previos

* Distribución LaTeX con `pdflatex` (TeX Live 2022+ o MiKTeX equivalente).
* Paquetes utilizados (todos incluidos en una instalación estándar / `texlive-latex-extra`):

  * `inputenc`, `fontenc`
  * `geometry`
  * `graphicx`
  * `booktabs`, `longtable`, `array`
  * `xcolor`
  * `hyperref`
  * `enumitem`
  * `titlesec`
  * `fancyhdr`
  * `parskip`
  * `ragged2e`
  * `float`
  * `caption`

No requiere `babel` para la compilación actual.

## Compilación

El archivo principal es **`main.tex`**. Se compila con **pdflatex**, ejecutando el comando dos veces para asegurar que los índices y referencias internas (tabla de contenidos, hyperref) queden resueltos:

```bash
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```

Esto genera `main.pdf` en la raíz del repositorio (el entregable subido al LMS corresponde a este mismo archivo, renombrado como `PruebaPractica_UnidadIV.pdf`).

### Alternativa con latexmk

```bash
latexmk -pdf main.tex
```

Para limpiar los archivos auxiliares generados por LaTeX:

```bash
latexmk -c
```
