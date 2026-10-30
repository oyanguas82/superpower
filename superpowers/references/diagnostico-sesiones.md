# Diagnóstico de sesiones

Adaptación de `diagnosing-superpowers`. Carga esta referencia cuando el usuario pida investigar el comportamiento de una sesión de trabajo, no como auditoría rutinaria de cada tarea.

## Delimitar y localizar

Identifica la sesión o evento, el resultado esperado y el síntoma observable: trabajo repetido, instrucciones omitidas, tiempo transcurrido o consumo. Usa el alcance que ya haya dado el usuario. Si solo falta una precisión, pregunta por ella y revisa lo que esté claramente delimitado.

Para chats de Codex, prefiere las herramientas de chats disponibles. Usa registros locales cuando sean necesarios y accesibles. Verifica el identificador y las fechas antes de atribuir eventos; la sesión de un subagente no es la del usuario.

Lee primero una región acotada alrededor del evento. En archivos JSONL, una línea puede contener una respuesta enorme: inspecciona campos y tamaños y extrae solo los fragmentos pertinentes. No vuelques todo el historial al contexto. Conserva los registros originales sin modificarlos.

## Construir conclusiones respaldadas

Relaciona cada hallazgo con una ruta y línea del registro, o con un identificador estable de evento o mensaje de la herramienta consultada. Distingue instrucciones humanas de mensajes de herramientas, ganchos y encargos entre agentes.

Sigue las dimensiones relevantes al síntoma: requisitos frente a acciones, repetición, fallos y reintentos, cambios de plan, verificaciones y tiempos. No hace falta activar todas las dimensiones ni delegarlas. Separa hecho observado, explicación posible y dato faltante.

Calcula duración o consumo solo con campos presentes y unidades conocidas. Los tiempos de pared pueden solaparse en ejecución paralela. No deduzcas precio de tokens ni coste monetario sin datos verificables del modelo y la tarifa aplicable.

Entrega la explicación que permita la evidencia, incluyendo límites de cobertura. No conviertas automáticamente un síntoma en un defecto de Superpowers ni cambies la habilidad a partir de una sola conjetura.

## Informe compartible, solo si se solicita

Si el usuario pide un paquete o reporte para terceros, selecciona la evidencia necesaria, conserva las ubicaciones de origen y trabaja sobre copias. Retira credenciales, datos personales y contenido ajeno al caso; comprueba que lo restante todavía sostenga cada hallazgo. Evita llamar anónimo a un paquete que solo fue revisado parcialmente.

Crear un informe o archivo local no implica autorización para enviarlo o publicar una incidencia. Prepara primero el contenido concreto y utiliza la autorización correspondiente para cualquier comunicación externa.
