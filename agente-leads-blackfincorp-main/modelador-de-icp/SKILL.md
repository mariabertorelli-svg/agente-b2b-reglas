---
name: modelador-de-icp
description: |
  Úsala para convertir una descripción en lenguaje natural de tu cliente ideal en una consulta concreta y guardada, contra la que el resto del sistema puntúa. Se activa cuando toca definir o revisar el cliente ideal de esta vigilancia: "modela mi cliente ideal".
---
# Modelador de cliente ideal

## Lógica
1. Traduce tu descripción en lenguaje natural a filtros ejecutables: sector (Seguros), tamaño de empresa, y cargos que deciden de verdad frente a cargos que no cuentan aunque comenten.
2. Comprueba el corte con la primera corrida real: si la lista sale enorme, a la consulta le falta señal; si sale vacía, el suelo duro aprieta de más.
3. Guarda la consulta en Notion, nunca dentro de un conector.
4. Escribe el suelo duro como negación, no como aspiración: qué queda fuera sin discusión, según reference/suelo-duro.md.

## Inputs / Outputs
- Input: tu descripción del cliente ideal.
- Output: la consulta guardada en Notion (filtros + suelo duro), que leen cazador-de-creadores-b2b-linkedin y scoring.

## Guardrails
- No enriquece ni escribe en ningún CRM: solo modela y guarda la consulta.
- La consulta vive en Notion. Nunca dentro de un conector.
