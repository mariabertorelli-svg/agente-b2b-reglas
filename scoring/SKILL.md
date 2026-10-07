---
name: scoring
description: |
  Úsala cuando tienes una lista de gente que comentó los posts de tus creadores vigilados y no sabes a quién escribir primero. Puntúa cada uno por encaje con tu cliente ideal y por intención, y devuelve la lista ordenada con el porqué de cada posición.
---
# Scoring de encaje e intención

## Lógica
1. Saca a los que no son tu cliente ideal antes de puntuar (consulta de modelador-de-icp). No reciben nivel bajo: no reciben nivel.
2. Para cada fila que queda, contesta dos preguntas: ¿cuánta intención hay? (calidad del comentario, autoridad del cargo) y ¿cuánto vale si entra? (tamaño y madurez de su empresa).
3. Cruza las dos en la matriz de reference/jerarquia-de-senales.md: intención fuerte + operación grande = Alto; el resto se reparte entre Medio y Bajo.
4. Ante la duda, sube de nivel.
5. Gasta barato antes de gastar caro: usa solo lo que ya es público (el comentario, el cargo, el perfil).
6. Escribe el motivo, siempre: nivel, las dos o tres señales que lo sostienen, tamaño.
7. Aplica el decaimiento de reference/decaimiento-y-niveles.md: una puntuación de hace meses no es fresca.

## Inputs / Outputs
- Input: la lista de quien comentó (de LeadShark/Apify), la consulta de cliente ideal, y el histórico de contacto (para no repuntuar).
- Output: la lista priorizada en Notion, con nivel y motivo por fila.

## Guardrails
- SIEMPRE el no-cliente-ideal sale antes de puntuar, y sin nivel.
- SIEMPRE cada fila lleva su motivo escrito.
- NUNCA se puntúa sin haber cargado la consulta de cliente ideal y el suelo duro.
