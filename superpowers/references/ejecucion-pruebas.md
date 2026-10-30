# Ejecución y pruebas

Reúne `executing-plans`, `test-driven-development` y la comprobación de `verification-before-completion`. La ejecución con agentes se describe en [colaboración](colaboracion.md), solo cuando esté autorizada.

## Ejecutar y conservar continuidad

Lee el plan, sus requisitos de origen y el estado real de los archivos. Comprueba las interfaces entre tareas antes de depender de ellas. Un plan no puede anular una restricción del usuario.

Para tareas prolongadas, mantén un registro pequeño junto al plan o en el espacio de trabajo establecido. Identifica el plan por su ruta y anota por tarea: estado, archivos afectados, decisiones relevantes y comando o comprobación con su resultado. Incluye referencias a commits solo si se crearon realmente; no hagas commits como un ritual de este flujo.

Al retomar una sesión, contrasta el registro con los archivos y, cuando exista, el historial de Git. Una marca de completado es una pista que verificar, no una razón para repetir todo ni una prueba suficiente de éxito. Reanuda en el primer resultado pendiente y conserva el trabajo ajeno.

Si un paso falla, distingue entre un defecto del código y un defecto del plan. Investiga los fallos con [depuración](depuracion.md). Ajusta detalles rutinarios del plan para cumplir los requisitos y registra las desviaciones materiales. Una decisión que cambia el alcance o depende del usuario se consulta; las partes independientes pueden continuar.

## Ciclo de pruebas de comportamiento

Para nueva lógica, regresiones y cambios de comportamiento que ameriten pruebas automatizadas, usa rojo, verde y refactorización:

1. Define una entrada y un resultado observable exigidos por el requisito. Escribe la prueba mínima que distinga el comportamiento correcto del defectuoso.
2. Ejecútala antes de la corrección y confirma que falla por el comportamiento relevante. Un fallo de instalación, sintaxis o configuración no demuestra una regresión reproducida.
3. Implementa el cambio mínimo que satisfaga el requisito y vuelve a ejecutar la prueba.
4. Comprueba los comportamientos vecinos afectados. Refactoriza solo si ayuda a la solución y conserva las pruebas correctas.

Si ya hay una prueba que reproduce el fallo, úsala. Si la implementación ya existe, verifica que la prueba pueda detectar el defecto con una reproducción segura y aislada; no borres ni reviertas trabajo del usuario para fingir un ciclo de pruebas.

Los cambios reversibles de bajo impacto, como una corrección de texto o estilo, pueden comprobarse directamente. No añadas pruebas que solo busquen una cadena del código, repliquen el algoritmo o validen el comportamiento de un simulacro. Para interfaces visuales, comprueba el resultado visible cuando la presentación sea parte del requisito.

## Pruebas que aporten evidencia

- Prefiere comportamiento público y resultados reales. Simula límites externos cuando haga falta aislamiento; no pruebes que un simulacro devuelve su propia respuesta.
- Incluye entradas límite o errores que se desprendan del requisito y del riesgo del cambio. No inventes una batería exhaustiva por defecto.
- Una prueba que pasa antes del cambio necesita investigación: puede estar probando otra cosa o la funcionalidad ya puede existir.
- Registra fallos preexistentes por separado. No debilites expectativas para ocultar un defecto ni afirmes que toda la suite pasó si hubo fallos o partes omitidas.

Cuando las comprobaciones apropiadas pasan y no hay cambios posteriores, continúa hacia la entrega. Repetirlas requiere una razón nueva.
