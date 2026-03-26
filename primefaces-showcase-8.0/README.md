# Documentación de la API: Gestión de Usuarios

<!-- TOC -->
* [Documentación de la API: Gestión de Usuarios](#documentación-de-la-api-gestión-de-usuarios)
  * [Introducción](#introducción)
  * [Endpoints](#endpoints)
    * [1. Obtener Lista de Usuarios](#1-obtener-lista-de-usuarios)
<!-- TOC -->

## Introducción
- **Versión de la API**: v1.0
- **Base URL**: `https://api.tu-dominio.com/v1`
- **Autenticación**: JWT Bearer Token (excepto en `/auth/login`)
- **Formato de Respuestas**: JSON
- **Códigos de Estado Comunes**:
    - 200 OK
    - 201 Created
    - 400 Bad Request
    - 401 Unauthorized
    - 403 Forbidden
    - 404 Not Found
    - 500 Internal Server Error

## Endpoints

### 1. Obtener Lista de Usuarios
- **Método HTTP**: GET
- **Path**: `/usuarios`
- **Descripción**: Devuelve una lista paginada de usuarios.
- **Parámetros**:
    - **Query Parameters**:
        - `page` (Integer, opcional, default: 1) — Página actual
        - `size` (Integer, opcional, default: 10) — Elementos por página
        - `filtro` (String, opcional) — Búsqueda por nombre o email sdfd
- **Respuestas**:
    - **200 OK**
      ```json
      {
        "content": [
          {
            "id": 1,
            "nombre": "Juan Pérez",
            "email": "juan@example.com",
            "activo": true
          }
        ],
        "page": 1,
        "size": 10,
        "totalElements": 45
      }
      
modifico de nuevo sdsd wwe