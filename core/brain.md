# 🧠 Engine de Observabilidad (Monitoring Brain)

## Matriz de Diagnóstico de Incidentes

1. **Si aumenta la Latencia sin aumento de Tráfico**:
   - Diagnóstico: Bloqueo de hilos (event loop / main thread) o lentitud en DB/APIs de terceros.
   - Acción: Revisar span de OpenTelemetry en llamadas I/O externas.

2. **Si aumentan los Errores 5xx drásticamente**:
   - Diagnóstico: Excepción no capturada en controlador o fallo de conexión a dependencia crítica.
   - Acción: Agrupar por `trace_id` en Sentry y revisar log de stacktrace.

3. **Si hay fugas de Memoria (Memory Leaks)**:
   - Diagnóstico: Listeners no cancelados, cachés sin expiración o colecciones estáticas acumulativas.
   - Acción: Activar métricas de Garbage Collection y Heap usage.
