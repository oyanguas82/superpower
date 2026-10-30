# Superpower

**Superpowers para Codex: una habilidad unificada en español para desarrollar software con resultados verificables.**

Esta adaptación reúne los 15 flujos del paquete Superpowers en una sola habilidad, `superpowers`. Su punto de entrada selecciona las referencias necesarias según la tarea: diseño, planificación, implementación, pruebas, depuración, revisión o entrega.

El proceso se ajusta al trabajo: una corrección pequeña puede resolverse directamente; un cambio con varias dependencias puede requerir un plan y comprobaciones adicionales.

## Estado de distribución

Este repositorio contiene la documentación y la licencia. La habilidad se distribuye actualmente mediante el paquete `superpowers-codex.zip`, generado por separado. Los archivos de la habilidad todavía no están versionados en este repositorio; para instalarla se necesita ese paquete o su carpeta `superpowers`.

## Qué incluye

| Flujo | Para qué sirve |
|---|---|
| Diseño y planificación | Aclarar requisitos, comparar alternativas y convertir decisiones en tareas comprobables. |
| Ejecución y pruebas | Implementar un plan, conservar el progreso y comprobar comportamientos relevantes. |
| Depuración sistemática | Reproducir un fallo, investigar su origen y verificar la corrección. |
| Revisión y entrega | Contrastar el cambio con los requisitos, atender observaciones y preparar una entrega verificable. |
| Aislamiento y colaboración | Organizar espacios de trabajo y coordinar agentes cuando esa modalidad esté autorizada. |
| Diagnóstico de sesiones | Investigar repeticiones, desviaciones del plan y consumo de recursos con evidencia. |
| Autoría de habilidades | Crear o mejorar habilidades y evaluar si ayudan a tomar mejores decisiones. |

Las referencias se cargan según la necesidad de la tarea, en lugar de incorporar todos los procedimientos al mismo tiempo.

## Instalación desde el paquete

1. Obtén el archivo `superpowers-codex.zip` generado para esta adaptación y descomprímelo.
2. Localiza la carpeta `superpowers`. En su interior deben estar `SKILL.md`, `agents`, `references` y `LICENSE`.
3. Copia la carpeta completa a tu directorio personal de habilidades de Codex.

Ubicación predeterminada en Windows:

```text
%USERPROFILE%\.codex\skills\superpowers\
```

Ubicación predeterminada en macOS o Linux:

```text
~/.codex/skills/superpowers/
```

Si utilizas una ubicación personalizada mediante `CODEX_HOME`, copia la carpeta en `CODEX_HOME/skills/superpowers/`.

El archivo de entrada debe quedar directamente en `skills/superpowers/SKILL.md`; evita una carpeta adicional como `skills/superpowers/superpowers/SKILL.md`. Si ya existe una versión instalada, conserva una copia antes de sustituirla.

## Cómo usarla

Invoca la habilidad junto con el objetivo concreto de tu solicitud:

```text
$superpowers Revisa este proyecto y prepara un plan para añadir exportación a Excel.
```

```text
$superpowers Investiga por qué falla el inicio de sesión, corrige la causa y comprueba el resultado.
```

```text
$superpowers Ejecuta este plan y conserva un registro de las tareas y comprobaciones realizadas.
```

```text
$superpowers Revisa estos cambios y señala los defectos que impiden cumplir los requisitos.
```

La habilidad también conserva la selección automática predeterminada según su descripción y las capacidades del entorno.

## Criterios de trabajo

- Examinar el contexto antes de preguntar por información que ya está disponible.
- Respetar las decisiones, la plataforma y el alcance indicados por el usuario.
- Aplicar pruebas de comportamiento cuando aporten evidencia y comprobaciones directas para cambios sencillos.
- Mantener un registro útil para continuar trabajos prolongados sin repetir tareas ya resueltas.
- Usar las herramientas disponibles y respetar la autorización concreta para delegar, publicar o modificar recursos.
- Vincular las afirmaciones de éxito con comprobaciones realizadas y comunicar las limitaciones materiales.

## Estructura del paquete

```text
superpowers/
├── SKILL.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── diseno-planificacion.md
    ├── ejecucion-pruebas.md
    ├── depuracion.md
    ├── revision-entrega.md
    ├── colaboracion.md
    ├── diagnostico-sesiones.md
    ├── autoria-habilidades.md
    └── procedencia.md
```

El paquete contiene 11 archivos y un único punto de entrada `SKILL.md`. La referencia de procedencia documenta la correspondencia de los 15 flujos originales y las decisiones de adaptación.

## Validación de la adaptación inicial

Se comprobó la estructura con el validador de habilidades, se verificaron los 12 enlaces locales de la documentación del paquete y se comparó el contenido del ZIP con los archivos preparados. La copia instalada también se comparó por sus huellas SHA-256.

Estas comprobaciones validan estructura e integridad; el comportamiento en cada proyecto se verifica durante su uso.

## Origen y licencia

Adaptación basada en el archivo `superpowers-main.zip` proporcionado para este trabajo, cuya versión declarada es `7.0.1`.

Proyecto de origen: [obra/superpowers](https://github.com/obra/superpowers), de Jesse Vincent. Esta distribución es una adaptación independiente para Codex.

La documentación de este repositorio se publica bajo [licencia MIT](LICENSE). El paquete de la habilidad conserva el aviso MIT original de Jesse Vincent en su propio archivo `LICENSE`.
