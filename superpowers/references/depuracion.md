# Depuración sistemática

Adaptación de `systematic-debugging`.

## Localizar el origen

Lee el error completo, las rutas afectadas y el contexto de la operación. Reproduce el fallo con la entrada y el entorno relevantes. Si es intermitente, registra las condiciones y recoge evidencia antes de atribuirlo a una causa.

Revisa los cambios recientes y compara un caso que funcione con el que falla. Sigue el dato incorrecto hacia su origen: quién lo produjo, qué transformación sufrió y en qué punto deja de cumplir el contrato.

En sistemas con varios componentes, inspecciona los límites pertinentes: solicitud y respuesta, propagación de configuración, persistencia o estado de una tarea. Usa instrumentación temporal acotada y evita registrar secretos o datos personales innecesarios. El objetivo es identificar dónde aparece la discrepancia, no acumular registros.

## Formular y probar una hipótesis

Expresa una causa comprobable y la evidencia que la sugiere. Cambia una variable o realiza una observación que permita distinguir esa hipótesis de otras. Si el resultado la refuta, actualiza la hipótesis; no acumules correcciones especulativas.

Antes de corregir, procura una reproducción o prueba que capture el síntoma. Para una regresión de lógica, aplica el ciclo de [ejecución y pruebas](ejecucion-pruebas.md). Corrige el origen y comprueba el caso original y los comportamientos afectados.

Si varios intentos fallan por la misma razón, cambia de estrategia: vuelve a observar, examina dependencias o cuestiona el diseño. Tres correcciones fallidas son una señal útil para reevaluar, no una autorización para rehacer la arquitectura. Una modificación de alcance se plantea con evidencia y consecuencias concretas.

## Asincronía y dependencias externas

Cuando el fallo dependa del tiempo, espera por una condición observable con un límite de tiempo y una salida de error clara; no aumentes pausas arbitrarias hasta que la prueba parezca estable.

Si la evidencia sitúa el problema fuera del código controlado, informa qué se comprobó y qué no puede verificarse. Aplica un manejo de error, un tiempo de espera o un reintento solo si encaja en el requisito. Los reintentos de escritura externa requieren conocer si la operación ya ocurrió; no dupliques envíos o transacciones.

La entrega debe conectar síntoma, causa respaldada por evidencia, cambio y comprobación. Si la causa sigue sin confirmarse, exprésala como hipótesis y conserva el límite de la conclusión.
