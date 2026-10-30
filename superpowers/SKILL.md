---
name: superpowers
description: "Aplica los flujos de Superpowers a proyectos de software: aclarar requisitos, planificar y ejecutar cambios, desarrollar con pruebas, investigar fallos y revisar entregas. Úsala cuando se solicite Superpowers o un proceso estructurado para trabajo de software de varios pasos. Los cambios pequeños y claros se resuelven directamente; no se aplica a conversaciones o tareas ajenas al desarrollo."
license: MIT
---

# Superpowers

Adaptación unificada para Codex del paquete Superpowers proporcionado por el usuario. Su objetivo es convertir una intención de software en cambios verificables, manteniendo continuidad entre diseño, ejecución y revisión.

## Elegir el flujo

Identifica el resultado solicitado y carga solo la referencia pertinente. Anuncia brevemente qué flujo aplicarás y para qué. No cargues todas las referencias por defecto.

| Situación | Referencia |
|---|---|
| Requisitos incompletos, alternativas de diseño o plan de varios pasos | [Diseño y planificación](references/diseno-planificacion.md) |
| Implementar una especificación o continuar un plan; pruebas de comportamiento | [Ejecución y pruebas](references/ejecucion-pruebas.md) |
| Fallo, regresión, error de integración o comportamiento inesperado | [Depuración sistemática](references/depuracion.md) |
| Revisar código, responder a observaciones o preparar la entrega | [Revisión y entrega](references/revision-entrega.md) |
| Aislar cambios con Git o coordinar trabajo delegado autorizado | [Aislamiento y colaboración](references/colaboracion.md) |
| Investigar por qué una sesión repitió trabajo, consumió recursos o ignoró requisitos | [Diagnóstico de sesiones](references/diagnostico-sesiones.md) |
| Crear o mejorar una habilidad como parte de una solicitud explícita | [Autoría de habilidades](references/autoria-habilidades.md) |

Una corrección pequeña y bien definida puede ir directamente a implementación y comprobación. Un fallo empieza por depuración; no necesita pasar primero por una discusión de diseño. Un plan existente conserva su enfoque y sus decisiones autorizadas.

## Criterios de trabajo

- Examina el contexto y los archivos pertinentes antes de preguntar lo que ya pueden responder. Conserva la plataforma, las convenciones y el alcance elegidos por el usuario.
- Ajusta el proceso al trabajo: preguntas para decisiones relevantes aún abiertas, plan para dependencias reales, pruebas para comportamientos que podrían romperse. Evita documentos, aprobaciones o reuniones de proceso sin una necesidad concreta.
- Usa las instrucciones del usuario y los requisitos acordados como referencia para resolver discrepancias con el plan. Registra las decisiones que cambien el resultado o ayuden a continuar después de una interrupción.
- Durante la ejecución autorizada, continúa por las tareas pendientes sin solicitar permiso para cada paso. Si falta una decisión imprescindible, pregunta de forma concreta y continúa con las partes independientes.
- Los flujos son orientación de trabajo; no amplían permisos para publicar, enviar mensajes, borrar datos, modificar configuración global ni usar agentes. Comprueba la autorización de la acción concreta, sin repetir permisos ya concedidos.
- Usa las herramientas que realmente estén disponibles. Si no hay delegación autorizada, realiza el trabajo y la revisión en esta sesión y describe con precisión el tipo de revisión realizado.

## Evidencia antes de declarar éxito

Antes de decir que algo está corregido, probado o terminado, compara el resultado pedido con las verificaciones pertinentes y lee sus resultados. Una modificación de código no demuestra que desapareció el fallo; un análisis estático no demuestra una compilación; una prueba local no demuestra un despliegue.

Tras una comprobación satisfactoria, repítela solo si hubo cambios posteriores o si queda una incertidumbre material. Informa del resultado, la evidencia y las limitaciones reales. No atribuyas una revisión independiente a una autorrevisión.

## Procedencia

Basada en las 15 habilidades de `superpowers-main.zip`, versión declarada `7.0.1`. Es una adaptación, no una instalación del plugin original. La correspondencia y las decisiones de adaptación están en [procedencia](references/procedencia.md); el aviso de licencia está en [LICENSE](LICENSE).
