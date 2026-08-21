---
name: monitoring-agent-skill
description: Transversal Observability, Telemetry, Structured Logging, and Alerting Skill for AI Agents.
---

# 📊 Monitoring Agent Skill Directive

## Bootstrap de la Habilidad

Al detectar `$monitoring` o tareas relacionadas con logs, métricas, Sentry, OpenTelemetry, Grafana, Prometheus o alertas, cargar:

1. `.agents/skills/monitoring/SKILL.md` ← **Directiva principal**
2. `.agents/skills/monitoring/core/commands.md`
3. `.agents/skills/monitoring/core/brain.md`
4. `.agents/skills/monitoring/core/path_map.md`

## Reglas Canónicas de Observabilidad Agnóstica

- **Logs Estructurados**: Prohibido `print()` o `console.log()` planos en producción. Todo log debe ser objeto JSON válido.
- **Correlation ID (Trace ID)**: Toda petición cliente -> backend debe incluir el header `X-Correlation-ID` o `traceparent`.
- **Privacidad PII**: Nunca incluir passwords, tokens JWT o datos personales sensibles en mensajes de log o breadcrumbs de Sentry.
- **Silencio de Alerta**: Las alertas deben medir SLO (Service Level Objectives) reales, no picos momentáneos de CPU irrelevantes.
