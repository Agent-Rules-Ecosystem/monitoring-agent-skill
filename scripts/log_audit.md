# 🔍 Script de Auditoría de Logs JSON

> **Verificación**: Validación de formato de logs estructurados en Python.

```python
#!/usr/bin/env python3
import sys
import json

def check_json_log(line):
    try:
        data = json.loads(line)
        required_keys = ["timestamp", "level", "message"]
        missing = [k for k in required_keys if k not in data]
        if missing:
            return False, f"Faltan claves obligatorias: {missing}"
        return True, "Válido"
    except Exception as e:
        return False, f"No es un JSON válido: {e}"

if __name__ == "__main__":
    print("🔍 Auditoría de Logs Estructurados JSON")
    sample_log = '{"timestamp": "2026-08-21T06:00:00Z", "level": "INFO", "message": "Health check ok"}'
    valid, msg = check_json_log(sample_log)
    print(f"Sample log status: {valid} ({msg})")
```
