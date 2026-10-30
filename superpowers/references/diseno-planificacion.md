# Diseño y planificación

Reúne los flujos `brainstorming` y `writing-plans`.

## Aclarar la intención

En un proyecto existente, lee primero los requisitos aportados, las convenciones locales y el código que conecta con el cambio. Determina qué funciona hoy, qué cambiará y cómo se reconocerá un resultado correcto.

Si la solicitud ya fija esos puntos, procede. Si una decisión no trivial cambia el producto, plantea la pregunta que más reduzca esa incertidumbre. No conviertas una preferencia técnica rutinaria en un bloqueo. Distingue lo dicho por el usuario de las suposiciones que tú propongas.

Cuando haya alternativas reales, compara las viables por su efecto sobre los objetivos, las restricciones y el mantenimiento. Recomienda una con una razón concreta. Usa una maqueta o diagrama si permite decidir algo que el texto no aclara; el servidor visual del paquete original no es necesario.

Si el usuario pidió explorar o aprobar un diseño antes de construir, respeta ese límite. Si pidió implementar y el alcance está claro, no añadas una aprobación de diseño por defecto. Un prototipo solicitado puede resolver incertidumbres sin exigir el proceso de una entrega de producción; indica qué permite comprobar y qué queda pendiente.

## Convertir requisitos en un plan ejecutable

Para trabajo con varias dependencias, describe el resultado y divide el trabajo en entregables comprobables. Usa un plan breve en la conversación cuando baste. Guarda un archivo cuando el usuario lo pida o cuando la duración y el traspaso de contexto lo justifiquen; sigue primero la ubicación del proyecto. Como alternativa, pueden usarse `docs/superpowers/specs/` y `docs/superpowers/plans/`.

Un plan útil conserva:

- Objetivo, límites y restricciones globales con sus valores exactos: versiones, formatos, permisos o textos fijados por el usuario.
- Archivos que se crearán o modificarán y responsabilidades de cada parte.
- Dependencias entre tareas y contratos compartidos: nombres, entradas, salidas y condiciones de error que otros componentes consumirán.
- Resultado observable de cada tarea y comprobación que lo demostraría.
- Casos de fallo relevantes que todavía no estén cubiertos por esas comprobaciones.

Una tarea debe tener suficiente independencia para verificarla; no necesita una duración artificial ni un número fijo de pasos. Incluye código completo solo si es necesario para fijar un algoritmo, contrato o texto exacto. No transcribas la implementación en el plan.

Antes de ejecutarlo, contrasta el plan con los requisitos: busca requisitos sin tarea, nombres incompatibles entre componentes y verificaciones que no demuestren el resultado. Corrige esos problemas. Mantén el método de ejecución que el usuario ya eligió; si no hay delegación autorizada, ejecuta en la sesión actual.
