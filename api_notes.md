# GitHub REST API - Notas Técnicas

## Documentación principal
- https://docs.github.com/en/rest
- API Version utilizada: `2022-11-28`

## Endpoints utilizados
- `/search/repositories`
- `/repos/{owner}/{repo}/commits`
- `/repos/{owner}/{repo}/contents/{path}`

## Parámetros clave
- `q`: parámetro de búsqueda (ej. `language:Python stars:>10000`)
- `per_page` y `page`: control de paginación
- `Authorization`: header con el token (Bearer token)
- `X-GitHub-Api-Version`: versión de API requerida

## Manejo de errores
- Código de estado HTTP (`401`, `403`, `404`)
- Headers de rate limit: `X-RateLimit-Remaining`, `Retry-After`

---
