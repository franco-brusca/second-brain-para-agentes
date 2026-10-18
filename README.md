# Second brain para agentes

Plantilla para armar un **second brain mantenido por agentes de IA**: una wiki de archivos markdown, versionada y con fuentes, que tu asistente mantiene y que vos leés con [Obsidian](https://obsidian.md).

No reemplaza la memoria nativa de tu asistente: la complementa. La memoria le da contexto a cada agente en cada conversación; el second brain es la **fuente única** que leen todos tus agentes y vos, legible, auditable y portable a otra herramienta.

Sigue el patrón **LLM Wiki** que describió Andrej Karpathy: en lugar de buscar cada vez en documentos sueltos, el agente mantiene páginas cortas y enlazadas que actualiza a medida que entra información.

Es agnóstico de agente: sirve con cualquier asistente que pueda leer y escribir archivos, usar git y correr tareas programadas.

## Cómo funciona, en breve

**Tres capas, cada una con su regla:**

| Capa | Dónde | Regla |
|---|---|---|
| Fuentes crudas | `10 Fuentes/` | No se editan. Si algo cambia, se agrega una fuente nueva. |
| Wiki | `20 Wiki/`, `30 MOCs/`, `40 Diario/`, `60 Pendientes/`, `index.md`, `log.md` | La mantiene el agente. |
| Reglas | `AGENTS.md`, `99 Plantillas/` | Cambian solo con tu aprobación. |

**El Inbox no es una capa, es la puerta de entrada.** Los agentes dejan todo lo nuevo en `00 Inbox/` y no tocan la wiki directamente (salvo el agente principal y vos).

**Destilado nocturno.** Una tarea diaria integra cada nota del Inbox en su página, fusiona duplicados, actualiza índice, mapas y pendientes, escribe el diario y guarda una versión. Entre hechos con fecha clara gana el más reciente; las decisiones en conflicto no se descartan: te llegan para que decidas.

**Revisión semanal.** Busca páginas huérfanas, duplicados, enlaces rotos, pendientes estancados y contradicciones abiertas. No aplica nada: te deja una propuesta para aprobar.

Todo se apoya en reglas simples, escritas en un solo archivo (`AGENTS.md`): toda afirmación con fuente, una decisión vive en una sola página, reemplazar en lugar de sumar, un registro que solo crece y nada de secretos ni datos personales de terceros.

## Cómo usarlo

Pegale esto a tu agente:

> Leé la guía https://github.com/franco-brusca/second-brain-para-agentes/blob/main/GUIA-AGENTE.md y seguila para armar mi second brain. Haceme las preguntas que necesites de a una, mostrame el plan completo y no crees nada hasta que lo apruebe.

Si tu agente no navega la web, cloná el repo en su espacio de trabajo y pedile que lea `GUIA-AGENTE.md`.

Tu second brain va a contener datos personales: respaldalo siempre en un **repositorio privado**, nunca en un fork público de este repo.

## Qué trae

```
00 Inbox/          entrada: notas sin procesar
10 Fuentes/        fuentes crudas (Llamadas, Charlas, Adjuntos)
20 Wiki/           páginas por tipo (Conceptos, Entidades, Decisiones, Procesos, Proyectos, Comparaciones)
30 MOCs/           mapas de contenido: Inicio y uno por área
40 Diario/         una nota por día
50 Revisiones/     observaciones del destilado, revisiones semanales y Propuestas/
60 Pendientes/     una página por área
90 Archivo/        lo inactivo
99 Plantillas/     13 plantillas con frontmatter común
AGENTS.md          archivo único de reglas
index.md           una línea por página
log.md             registro de cambios, solo se agrega
GUIA-AGENTE.md     instrucciones paso a paso para el agente
```

## Licencia

[MIT](LICENSE) © 2026 Franco Emmanuel Brusca
