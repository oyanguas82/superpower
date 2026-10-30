# Aislamiento y colaboración

Reúne `using-git-worktrees`, `dispatching-parallel-agents` y `subagent-driven-development`.

## Aislar cuando sea útil

Comprueba el estado de Git y los cambios existentes antes de elegir dónde trabajar. Una tarea local sencilla no necesita un worktree nuevo por defecto.

Si hace falta aislamiento, detecta primero si ya existe un worktree vinculado. Compara las rutas resueltas de `git rev-parse --git-dir` y `git rev-parse --git-common-dir`; comprueba también `git rev-parse --show-superproject-working-tree` para distinguir un submódulo. Conserva la ubicación y las decisiones del entorno que lo creó.

Para crear un espacio aislado, prefiere las herramientas nativas disponibles y respeta la preferencia de ubicación del usuario. Si recurres a Git, verifica la rama de origen, una ruta libre y la exclusión de carpetas internas mediante `git check-ignore`. No confirmes cambios de `.gitignore` ni instales dependencias indiscriminadamente para satisfacer un paso genérico.

Establece una comprobación inicial pertinente al trabajo para distinguir los fallos anteriores de los introducidos. Una comprobación inicial fallida no autoriza reparar problemas ajenos; determina si bloquea la tarea o si puede continuarse con esa limitación registrada.

Si el aislamiento no está permitido o falla, evalúa si trabajar en la ubicación actual sigue siendo seguro y autorizado; no cambies silenciosamente una petición explícita de aislamiento.

## Elegir ejecución directa o delegada

Esta referencia explica cómo coordinar agentes cuando la petición del usuario o las instrucciones aplicables autoricen esa modalidad y existan herramientas para ello. La presencia de esta habilidad no concede por sí sola permiso para delegar. Respeta las restricciones de herramientas, modelos, concurrencia y coste del entorno.

Usa ejecución directa si no hay delegación autorizada o si la tarea depende estrechamente de un mismo contexto. Paraleliza solo trabajos con entradas estables y sin escritura simultánea sobre los mismos archivos, recursos o estado compartido. Varios síntomas de una misma causa suelen investigarse juntos.

## Preparar encargos acotados

Proporciona a cada agente:

- Objetivo y resultado observable de su tarea.
- Rutas concretas y el mínimo contexto necesario de requisitos e interfaces.
- Archivos que puede cambiar y recursos que debe dejar intactos.
- Dependencias que ya deben estar resueltas y comprobaciones pertinentes.
- Informe esperado: cambios, evidencia, decisiones y obstáculos.

No otorgues a un agente permisos que tú no tengas. No le transmitas el historial completo si un encargo autónomo basta, ni sugieras la solución al revisor cuando se busca una evaluación independiente.

## Coordinar y verificar

Para un plan delegado, mantén un registro por plan con tarea, responsable, estado y evidencia. Un implementador puede resolver un entregable y un revisor examinar su cumplimiento y calidad. Adapta la frecuencia de revisión al riesgo; no dupliques contextos para cada operación mecánica.

Antes de avanzar sobre una dependencia, comprueba los cambios devueltos y su evidencia. Al integrar trabajo paralelo, busca conflictos de contratos y archivos y ejecuta las comprobaciones de integración pertinentes. Un informe de agente no demuestra por sí solo que el resultado funciona.

Si un ciclo de revisión repite el mismo fallo sin evidencia nueva, detén el ciclo, concentra el diagnóstico y revisa la división de tareas. No amplíes presupuesto, alcance o permisos para mantener el flujo en marcha.
