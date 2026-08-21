# 🪵 Guía de Logging Estructurado JSON

## Reglas de Campo OBLIGATORIOS
- `timestamp`: Formato ISO-8601 UTC string (`2026-08-21T06:00:00.000Z`).
- `level`: Enum string (`DEBUG`, `INFO`, `WARN`, `ERROR`, `FATAL`).
- `service`: Identificador único del microservicio o cliente.
- `message`: Descripción en texto legible del evento.
- `trace_id`: ID de correlación único que viaja a través de todas las capas de llamadas HTTP/gRPC.
