# Práctica 4.5 – Calculadora de huella ecológica

**Instituto Tecnológico de Mazatlán** · Ingeniería en Sistemas Computacionales
**Asignatura:** Desarrollo Sustentable (ACD-0908) · **Unidad 4:** Escenario económico
**Tema:** 4.5 Estrategias de sustentabilidad para el escenario económico (análisis de ciclo de vida y huella ecológica)
**Alumno:** Christian Paul Lizárraga Oronia
**Profesor:** Miguel Ángel Barrón Hernández

---

## 🎥 Video

[▶ Ver el video de la práctica en YouTube](https://www.youtube.com/watch?v=PEGA_AQUI_EL_ID_DEL_VIDEO)

## 🌐 Página publicada

[Abrir la calculadora en GitHub Pages](https://christiac507.github.io/P4.5-Calculadora_huella_ecologica/C%C3%B3digo/)

---

## Objetivo

Calcular y comparar la huella ecológica personal, identificar qué hábitos la elevan y proponer estrategias económicas y personales para reducirla, evaluando la precisión de una estimación hecha con IA.

## ¿Cómo funciona?

```
Página web (index.html) — cuestionario de 10 preguntas
   │  POST con URLSearchParams
   ▼
Webhook de Make → Make AI Agent → Webhook Response
   │
   ▼
La página muestra: hectáreas globales, planetas necesarios,
impacto por área, 3 acciones y una oportunidad económica
```

Después, el resultado se compara con la calculadora oficial de Global Footprint Network ([footprintcalculator.org](https://www.footprintcalculator.org)).

## Secciones del cuestionario

| Sección | Campos |
|---------|--------|
| Alimentación | `carne`, `local` |
| Transporte | `transporte`, `km`, `vuelos` |
| Energía | `aire`, `personas` |
| Consumo | `ropa`, `celular` |
| Residuos | `separa` |

## Tecnologías

- HTML, CSS y JavaScript (un solo archivo, sin librerías externas)
- Make: Webhooks, Make AI Agent, Webhook Response
- GitHub Pages
- Calculadora oficial de Global Footprint Network

## Estructura del repositorio

| Carpeta | Contenido |
|---------|-----------|
| `Código/` | `index.html` (la calculadora) y `configuracion_make.md` (módulos e instrucciones de la IA) |
| `Imágenes/` | Capturas del escenario, de la página y de la calculadora oficial |
| `Video/` | Video de la práctica (enlace arriba) |
| `Resultados/` | Informe en PDF con investigación, comparación y preguntas |

## Resultados

La comparación entre la estimación de la IA y la calculadora oficial, junto con la huella promedio de México y del mundo, está en [`Resultados/`](Resultados/).
