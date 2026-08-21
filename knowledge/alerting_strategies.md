# 🚨 Estrategias de Alerta e Inhibición de Fatiga

1. **Alertar sobre Síntomas, no Causas**: Alertar cuando la latencia percibida por el usuario sea alta, no porque el CPU esté al 70%.
2. **Ventanas de Evaluación Mínimas**: Evaluar condiciones sobre una ventana móvil de al menos 5 minutos (`for: 5m`) para amortiguar picos esporádicos.
3. **Agrupación y Deduplicación**: Agrupar alertas por servicio o cluster para enviar una sola notificación consolidada.
