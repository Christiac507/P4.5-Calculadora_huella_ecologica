# Práctica 4.5 – Calculadora de huella ecológica

**Instituto Tecnológico de Mazatlán** · Ingeniería en Sistemas Computacionales
**Asignatura:** Desarrollo Sustentable (ACD-0908) · **Unidad 4:** Escenario económico
**Tema:** 4.5 Estrategias de sustentabilidad para el escenario económico (análisis de ciclo de vida y huella ecológica)
**Alumno:** Christian Paul Lizárraga Oronia
**Profesor:** Miguel Ángel Barrón Hernández

---

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
| `Código/` | `index.html` (la calculadora), `Huella_Ecologica_Equipo#.blueprint.json` (blueprint exportado de Make) y `configuracion_make.md` (módulos e instrucciones de la IA) |
| `Imágenes/` | Capturas del escenario, de la página y de la calculadora oficial |
| `Video/` | `enlace.txt` con el enlace al video en YouTube |
| `Resultados/` | Informe en PDF con investigación, comparación y preguntas |

## Resultados

Respuestas del cuestionario (12 de noviembre de 2026):

| Pregunta | Respuesta |
|----------|-----------|
| Carne de res o cerdo | 3–5 veces por semana |
| Comida local o de temporada | La mitad |
| Transporte principal | Camión urbano, 12 km al día |
| Vuelos al año | 0 |
| Aire acondicionado | 8 h al día |
| Personas en casa | 4 |
| Prendas nuevas al mes | 1 |
| Cambio de celular | Cada 3 años |
| Separa la basura | A veces |

| Herramienta | Resultado |
|-------------|-----------|
| Página con IA (Make AI Agent) | 3.0 hag por año · **1.9 planetas** |
| Calculadora oficial (Global Footprint Network) | **3.6 planetas** · Día de Sobregiro personal: 12 de abril |
| Promedio de México y del mundo | ≈ 1.7 planetas |

- La IA dio casi la mitad que la calculadora oficial (diferencia de 1.7 planetas).
- Área de mayor impacto: **energía**, por el aire acondicionado; la IA también marcó como altas la alimentación y el transporte.
- Oportunidad económica propuesta por la IA: un servicio local de eficiencia energética para viviendas de clima cálido (aire acondicionado eficiente, aislamiento y paneles solares).

El informe completo está en [`Resultados/`](Resultados/).

## Preguntas de reflexión

**1. ¿Qué área de su estilo de vida genera la mayor huella? ¿Coincide en todo el equipo?**

En mi caso, el área de mayor impacto fue la energía, por las 8 horas diarias de aire acondicionado; la IA también marcó como altas la alimentación (carne 3 a 5 veces por semana) y el transporte. En Mazatlán es muy común que la energía y el transporte sean las áreas más altas: el calor obliga a usar aire acondicionado muchas horas y la ciudad está diseñada para moverse en auto o moto. La alimentación también pesa cuando se come carne de res o cerdo casi a diario, porque su producción requiere mucha tierra, agua y alimento para el ganado. En el grupo no hay equipos, así que la práctica la hice solo y no pude comparar con otros integrantes; sin embargo, el resultado coincide con lo que es típico en la ciudad.

**2. ¿Por qué el aire acondicionado pesa tanto en la huella de una persona en Mazatlán? ¿Qué alternativas hay?**

Porque Mazatlán tiene un clima cálido y húmedo durante gran parte del año, y en verano muchas casas usan el aire acondicionado varias horas al día, incluso toda la noche. Es uno de los aparatos que más electricidad consume en un hogar, y en México esa electricidad se genera en gran parte quemando gas natural y combustóleo, lo que libera CO₂; en la huella ecológica, el carbono es el componente más grande. Como alternativas están usar equipos inverter, que gastan menos, mantener el termostato en 24–25 °C, dar mantenimiento a los filtros, aislar el techo con pintura reflejante, usar ventiladores y cortinas, y aprovechar la ventilación cruzada en las horas frescas. También ayudan los paneles solares en casa.

**3. ¿Qué tan cerca estuvo la estimación de la IA de la calculadora oficial? ¿A qué se debe la diferencia?**

No estuvo muy cerca: la IA estimó 1.9 planetas y la calculadora oficial dio 3.6 planetas, una diferencia de 1.7 planetas, es decir, la IA dio casi la mitad. Además, al repetir el cálculo con los mismos datos la IA cambió un poco su resultado (la primera vez dio 2.8 hag y 2 planetas), lo que muestra que no es un cálculo fijo. La diferencia se debe a que la IA no hace un cálculo con datos oficiales, sino una estimación con base en lo que aprendió, por lo que sus valores son aproximados. La calculadora de Global Footprint Network usa datos nacionales de huella y biocapacidad y hace muchas más preguntas, por ejemplo sobre el tipo de vivienda, el tamaño de la casa y la cantidad de comida procesada. Nuestro cuestionario solo tiene 10 preguntas, así que deja fuera hábitos que influyen en la huella. Por eso la IA sirve para orientar, pero el cálculo oficial es más confiable.

**4. ¿Qué estrategia económica (empresa socialmente responsable, economía circular, servicios ambientales) ayudaría más a reducir la huella de su comunidad?**

Creemos que la economía circular ayudaría más, porque ataca varias áreas a la vez: reduce residuos, ahorra materias primas y genera empleos locales. En Mazatlán podría aplicarse con negocios de reparación de electrónicos y electrodomésticos, venta de ropa de segunda mano, centros de acopio que paguen por plástico y aluminio, y compostaje de residuos orgánicos de mercados y restaurantes. También ayudarían empresas que instalen paneles solares y aislamiento térmico en casas, porque el aire acondicionado es la mayor carga energética de la región. Estas actividades reducen la huella y al mismo tiempo crean oportunidades de negocio.

**5. ¿Qué acción concreta harán durante el próximo mes y cómo medirán si funcionó?**

Durante el próximo mes voy a reducir el uso del aire acondicionado programándolo a 25 °C y apagándolo dos horas antes de levantarme, y usaré ventilador en las horas menos calurosas. También voy a hacer caminando o en bicicleta los trayectos cortos que hoy hago en camión y comer carne de res o cerdo solo dos veces por semana. Para medir si funcionó compararé el consumo en kWh del próximo recibo de la CFE con el anterior, anotaré cada semana cuántos viajes hice sin camión y, al final del mes, volveré a contestar la calculadora oficial para ver si bajó el número de planetas.
