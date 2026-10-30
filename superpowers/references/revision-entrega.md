# Revisión y entrega

Reúne `requesting-code-review`, `receiving-code-review`, `verification-before-completion` y `finishing-a-development-branch`.

## Revisar el resultado

Revisa el cambio completo contra los requisitos, las interfaces afectadas y los escenarios de uso. Si usas Git, identifica el intervalo real desde el inicio del trabajo; `HEAD~1` no representa necesariamente una tarea de varios commits. Considera también cambios sin confirmar y archivos nuevos.

Comprueba primero el cumplimiento funcional; después la calidad, el mantenimiento y los riesgos concretos introducidos. Un hallazgo útil identifica una ubicación precisa, la condición que lo dispara y su efecto para la persona o el sistema. Prioriza por impacto, no por preferencia de estilo. No inventes observaciones para completar una cuota.

Cuando una revisión independiente esté autorizada y disponible, facilita al revisor el resultado esperado, las rutas necesarias, el alcance del cambio y las verificaciones ya realizadas. Examina sus hallazgos y el código real. En otro caso, realiza una pasada separada de autorrevisión y descríbela como tal. Una revisión no equivale a la ejecución de pruebas.

## Responder a observaciones

Reproduce o contrasta el hallazgo antes de cambiar código. Si es correcto, corrígelo y realiza la comprobación pertinente. Si depende de un supuesto equivocado, explica el comportamiento observado y la evidencia. Si la sugerencia amplía el alcance, separa la corrección necesaria de la mejora opcional.

Resuelve los defectos que impiden cumplir la tarea antes de declarar finalización. Las observaciones menores pueden documentarse como pendientes si no son requisitos. Las nuevas correcciones justifican volver a ejecutar las comprobaciones afectadas; una nueva revisión amplia se reserva para incertidumbres que esas pruebas no resuelvan.

No publiques respuestas en una plataforma ni contactes a otras personas por el solo hecho de recibir comentarios: utiliza la autorización existente para esa comunicación concreta.

## Integración y cierre

Entrega primero un resultado concreto y revisable: archivos, cambio comprobado, evidencia y limitaciones materiales. Diferencia implementación local, integración de rama, publicación y validación en el destino. Si se pidió solo revisión, entrega hallazgos; no modifiques archivos automáticamente.

Si se pidió integrar o publicar, usa la rama y el destino verificados y continúa dentro de la autorización. Si la decisión de integración sigue abierta, conserva el trabajo e indica qué falta decidir; no fuerces un menú idéntico para todas las tareas. Antes de pedir una aprobación necesaria para una acción final, completa todo el trabajo preparatorio autorizado.

Antes de limpiar un espacio de trabajo, identifica su propietario real y los archivos que contiene. Una carpeta llamada `.worktrees` no demuestra que esta sesión la creó. Conserva espacios externos y trabajo sin integrar; no borres ramas, registros o archivos por una convención de cierre.

Informa con precisión qué cambió, cómo se comprobó y qué queda pendiente. Una ejecución sin errores no basta si no cubre el comportamiento que se solicitó.
