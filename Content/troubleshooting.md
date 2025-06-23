# Troubleshooting Guide

## Error: 401 Unauthorized
- 🔑 **Token de Autenticación**: Verificar que el token sea válido y tenga permisos suficientes.
- ⚙️ **Headers correctos**: Asegurarse de incluir `Authorization` y `X-GitHub-Api-Version` en cada request.
- 🕓 **Token expirado**: Si estás usando un token temporal, puede haber caducado.

## Error: 403 Rate Limit Exceeded
- 🧭 **Manejo de límites de tasa (Rate Limits)**:
  - Consultar el endpoint `/rate_limit`.
  - Implementar lógica de espera (`time.sleep`) al detectar headers como `X-RateLimit-Remaining: 0`.

## Problemas comunes
- ❌ Respuesta vacía o incompleta → revisar paginación (`per_page`, `page`) y usar bucles para traer todos los datos.
- 🔄 Reintentos → En caso de fallos intermitentes, usar `try-except` con reintentos (`requests.exceptions.RequestException`).

---
