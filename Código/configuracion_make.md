# Configuración del escenario en Make: `Huella_Ecologica_Equipo#`

Flujo: **Página web → Webhook de Make → Make AI Agent → Webhook Response → Página web**

## Módulos

| # | Módulo | Configuración |
|---|--------|---------------|
| 1 | Webhooks → Custom webhook | Crear uno nuevo, copiar la URL y pegarla en `WEBHOOK_URL` de `index.html`. Con *Run once* contestar el cuestionario y presionar **Calcular mi huella**: deben aparecer los 10 campos (`carne`, `local`, `transporte`, `km`, `vuelos`, `aire`, `personas`, `ropa`, `celular`, `separa`). |
| 2 | Make AI Agent | Connection: Make's AI Provider (créditos del plan Pro, sin API key). Input e Instructions: ver abajo. |
| 3 | Webhooks → Webhook Response | Status `200`. Body: respuesta del AI Agent. Headers: `Content-Type` = `text/plain; charset=utf-8` y `Access-Control-Allow-Origin` = `*`. |

Guardar y activar el escenario con **Immediately as data arrives**.

## Input del AI Agent

Mapear cada campo desde el panel (no escribir los números de módulo a mano):

```
Carne: {{1.carne}}
Comida local: {{1.local}}
Transporte: {{1.transporte}}
Km al dia: {{1.km}}
Vuelos al año: {{1.vuelos}}
Aire acondicionado: {{1.aire}} h/dia
Personas en casa: {{1.personas}}
Prendas nuevas al mes: {{1.ropa}}
Cambia de celular cada: {{1.celular}} años
Separa basura: {{1.separa}}
```

## Instructions del AI Agent

```
Eres un analista de huella ecologica para alumnos de Desarrollo Sustentable del TecNM en Mazatlan, Sinaloa (clima calido, uso alto de aire acondicionado).
Recibiras las respuestas de un cuestionario de estilo de vida. Estima la huella ecologica de la persona.
Aclara que es una estimacion aproximada y no un calculo oficial.
Responde en texto plano (sin asteriscos, sin markdown), en espanol, con este formato:

TU HUELLA ESTIMADA
Hectareas globales por año: [valor aproximado]
Planetas necesarios si todos vivieran asi: [valor]

POR AREA (de mayor a menor impacto)
Alimentacion: [alto / medio / bajo y por que, en 1 linea]
Transporte: [...]
Energia: [...]
Consumo: [...]
Residuos: [...]

3 ACCIONES PARA REDUCIRLA
1. [la de mayor efecto]
2. [...]
3. [...]

OPORTUNIDAD ECONOMICA
[2 lineas: un negocio o servicio sustentable de la region que ayudaria a reducir esta huella]
```

## Calculadora oficial

https://www.footprintcalculator.org (elegir idioma español). Guardar el resultado de "planetas" para compararlo con el de la página.
