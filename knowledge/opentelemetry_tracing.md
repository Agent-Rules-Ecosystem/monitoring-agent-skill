# 🔍 OpenTelemetry & Distributed Tracing

## Conceptos Clave
- **Trace**: Representa el viaje completo de una solicitud a través del ecosistema distribuido.
- **Span**: Unidad de trabajo individual dentro de un Trace (ej. consulta SQL, llamada HTTP a API externa).
- **Context Propagation**: Mecanismo de inyección y extracción de headers `traceparent` (W3C Trace Context).
