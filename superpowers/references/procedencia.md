# Procedencia y alcance de la adaptación

Fuente: archivo local `superpowers-main.zip` facilitado por el usuario.
Proyecto de origen declarado por el paquete: `obra/superpowers`.
Versión declarada en `.codex-plugin/plugin.json`: `7.0.1`.
No se consultó ni se presupone una versión posterior en Internet.
Autor original: Jesse Vincent. Licencia MIT; el archivo `LICENSE` conserva el aviso original.

SHA-256 del ZIP de origen: `d06a326ee189068b1aa0956452c259d39a66f5ff76ae9f0f7ece31710cbfe995`.

## Correspondencia de las 15 habilidades

| Habilidad de origen | Destino en esta adaptación |
|---|---|
| `using-superpowers` | SKILL.md: selección del flujo y uso de referencias |
| `brainstorming` | references/diseno-planificacion.md |
| `writing-plans` | references/diseno-planificacion.md |
| `executing-plans` | references/ejecucion-pruebas.md |
| `test-driven-development` | references/ejecucion-pruebas.md |
| `systematic-debugging` | references/depuracion.md |
| `verification-before-completion` | SKILL.md y references/revision-entrega.md |
| `requesting-code-review` | references/revision-entrega.md |
| `receiving-code-review` | references/revision-entrega.md |
| `finishing-a-development-branch` | references/revision-entrega.md |
| `using-git-worktrees` | references/colaboracion.md |
| `dispatching-parallel-agents` | references/colaboracion.md |
| `subagent-driven-development` | references/colaboracion.md |
| `diagnosing-superpowers` | references/diagnostico-sesiones.md |
| `writing-skills` | references/autoria-habilidades.md |

## Decisiones de adaptación

- Una sola habilidad `superpowers`, con descripción y metadatos de interfaz en español. La selección automática conserva el valor predeterminado; la descripción limita su uso a trabajo de software pertinente.
- Los procedimientos se reescribieron y condensaron por propósito; no son una reproducción íntegra de las habilidades originales.
- Las reglas universales de activación, las aprobaciones por cada diseño o plan y los ciclos obligatorios de revisión se sustituyeron por criterios proporcionales al alcance y a la autorización existente.
- La delegación queda condicionada a la petición del usuario o las instrucciones aplicables y a las herramientas disponibles. Se conserva la ejecución directa y no se fija un modelo obligatorio.
- Se conserva el enfoque de pruebas de comportamiento, sin exigir pruebas automatizadas para todo cambio de texto ni borrar implementaciones existentes para recrear un ciclo de pruebas.
- Se conserva el aislamiento útil y la trazabilidad de tareas, sin commits, limpieza de espacios, publicaciones ni envíos automáticos.
- No se incorporaron hooks de inicio, servidores visuales, telemetría, extensiones para otras plataformas ni ejecutables Bash del ZIP. Los procedimientos usan las herramientas disponibles en el entorno de destino.
- La atribución y el mapa de origen son documentación de procedencia; solo hace falta leerlos al revisar o mantener esta adaptación.
