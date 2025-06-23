# Repositorios - Resultados de la API de GitHub

Este archivo `repositorios.json` contiene el resultado de una consulta a la API REST de GitHub, realizada como parte del ejercicio técnico para el puesto de Data Source API Analyst.

## 🔍 Descripción

Se utilizó el endpoint:
GET https://api.github.com/search/repositories

### Parámetros utilizados en la consulta:
- `q=language:Python stars:>10000`
- `sort=stars`
- `order=desc`
- `per_page=5`

Este conjunto de parámetros busca los repositorios públicos escritos en Python con más de 10.000 estrellas, ordenados por popularidad de forma descendente, y limita la respuesta a los primeros 5 resultados.

---

## 📁 Estructura del archivo

Cada elemento en la lista `items` representa un repositorio e incluye, entre otros, los siguientes campos clave:

- `name`: nombre del repositorio
- `full_name`: nombre completo con el usuario u organización
- `html_url`: URL del repositorio en GitHub
- `description`: descripción del proyecto
- `stargazers_count`: cantidad de estrellas
- `language`: lenguaje principal
- `forks_count`: cantidad de forks
- `license`: tipo de licencia (si la tiene)

---

## 🧪 Uso

Este archivo puede ser usado para:
- Validar la estructura de la respuesta de la API de GitHub.
- Analizar tendencias en proyectos populares escritos en Python.
- Probar la integración de APIs con notebooks de análisis o herramientas tipo Postman.

---

## ✅ Validación

Este resultado fue obtenido exitosamente utilizando autenticación personal con token y configuración adecuada de headers:
- `Authorization: Bearer <token>`
- `X-GitHub-Api-Version: 2022-11-28`

---

