# Comparación de superpowers.zip

Fecha de revisión: 2026-10-29.

## Resultado

El archivo `superpowers.zip` contiene la misma versión declarada `7.0.1` que `superpowers-main.zip`, utilizado para preparar la habilidad unificada. Sus 231 archivos de contenido coinciden al normalizar los finales de línea CRLF a LF. Los 15 archivos `skills/*/SKILL.md` coinciden también byte a byte.

El nuevo ZIP añade 28 archivos internos en `.git/`. Son metadatos de un repositorio local, no recursos adicionales de la habilidad.

## Identificación de las fuentes

| Dato | Fuente inicial | ZIP adicional |
|---|---|---|
| Archivo | `superpowers-main.zip` | `superpowers.zip` |
| Tamaño en bytes | 655323 | 9170947 |
| Versión declarada | 7.0.1 | 7.0.1 |
| Archivos de contenido | 231 | 231 |
| Archivos internos de Git | 0 | 28 |

SHA-256 de `superpowers-main.zip`:

```text
d06a326ee189068b1aa0956452c259d39a66f5ff76ae9f0f7ece31710cbfe995
```

SHA-256 de `superpowers.zip`:

```text
a7da8c8c422e58f9953a54a8b8de3e4828d4a5ad8e372b7c9821b72335d5b495
```

La versión procede de `.codex-plugin/plugin.json` dentro de cada archivo. Esta revisión compara los dos ZIP proporcionados; no determina si existe una versión posterior del proyecto original.

## Método

1. Se enumeraron las entradas de ambos ZIP y se retiró únicamente la carpeta contenedora de sus rutas.
2. Se comprobaron rutas relativas, ausencia de recorridos fuera del destino y ausencia de enlaces simbólicos.
3. Se separaron las entradas de `.git/` del segundo ZIP antes de comparar el contenido del proyecto.
4. Se compararon rutas y bytes: no hay archivos de contenido añadidos ni eliminados.
5. Para las 29 diferencias de bytes, se compararon de nuevo los datos convirtiendo CRLF a LF. Todas las diferencias desaparecieron.
6. Se contrastaron los 11 archivos de la habilidad instalada con los objetos de GitHub: coincidían antes de esta actualización de procedencia.

Las instrucciones incluidas en los ZIP se examinaron como material de origen. No se ejecutaron sus hooks, scripts ni instaladores.

## Archivos con diferencias únicamente de finales de línea

- `.gitattributes`
- `.github/FUNDING.yml`
- `.github/ISSUE_TEMPLATE/config.yml`
- `.gitignore`
- `.hermes-plugin/__init__.py`
- `.hermes-plugin/plugin.yaml`
- `.pre-commit-config.yaml`
- `LICENSE`
- `skills/brainstorming/scripts/frame-template.html`
- `skills/brainstorming/scripts/server.cjs`
- `skills/executing-plans/scripts/task-done`
- `skills/executing-plans/scripts/task-start`
- `skills/subagent-driven-development/scripts/review-package`
- `skills/subagent-driven-development/scripts/sdd-workspace`
- `skills/subagent-driven-development/scripts/task-brief`
- `skills/writing-skills/references/graphviz-conventions.dot`
- `tests/claude-code/analyze-token-usage.py`
- `tests/explicit-skill-requests/prompts/action-oriented.txt`
- `tests/explicit-skill-requests/prompts/after-planning-flow.txt`
- `tests/explicit-skill-requests/prompts/claude-suggested-it.txt`
- `tests/explicit-skill-requests/prompts/i-know-what-sdd-means.txt`
- `tests/explicit-skill-requests/prompts/mid-conversation-execute-plan.txt`
- `tests/explicit-skill-requests/prompts/please-use-brainstorming.txt`
- `tests/explicit-skill-requests/prompts/skip-formalities.txt`
- `tests/explicit-skill-requests/prompts/subagent-driven-development-please.txt`
- `tests/explicit-skill-requests/prompts/use-systematic-debugging.txt`
- `tests/hermes/conftest.py`
- `tests/hermes/test_bootstrap.py`
- `tests/hermes/test_plugin.py`

Las rutas de esta lista pertenecen al proyecto original, no a la carpeta de la adaptación unificada.

## Incorporación al repositorio y a la instalación

Se registra la fuente adicional en [la procedencia de la habilidad](../superpowers/references/procedencia.md) y se enlaza esta comparación desde el README.

El contenido funcional de la habilidad unificada ya cubre los 15 flujos del ZIP. Esta revisión actualiza su documentación de procedencia y conserva su comportamiento. Los metadatos internos `.git/` del archivo adjunto se excluyen de la instalación y de la publicación.

La estructura y los enlaces locales de la habilidad se validan antes de la sincronización. La igualdad entre la copia instalada y la publicada se comprueba mediante las huellas de sus archivos.
