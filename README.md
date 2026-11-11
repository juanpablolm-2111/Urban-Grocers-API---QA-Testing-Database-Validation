# Urban Grocers API - QA Testing & Database Validation

Este repositorio contiene la documentación completa, casos de prueba, consultas SQL de verificación y reportes de incidencias (bugs) desarrollados como parte del ciclo de pruebas de la API de paquetes de comestibles (**Urban Grocers**).

## 🚀 Acerca del Proyecto
El objetivo principal fue validar el comportamiento del servicio de gestión de paquetes (`/api/v1/grocery-bundles`), asegurando el correcto manejo de códigos de respuesta HTTP, restricciones de negocio (como el límite máximo de productos), la integridad de las relaciones en la base de datos y la correcta persistencia de los datos.

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Postman:** Pruebas de endpoints REST, manejo de autenticación por Bearer Token y ejecución de colecciones.
* **SQL / SQLite:** Consultas de verificación de estado (antes y después), funciones de agregación (`COUNT`, `SUM`, `COUNT(DISTINCT)`) y cruces relacionales (`JOIN`).
* **Documentación y QA:** Diseño de casos de prueba formales, precondiciones detalladas, análisis de impacto y reporte formal de bugs (con severidad y pasos de reproducción).

## 📁 Estructura del Repositorio
* `Casos-de-Prueba/`: Documentación de pruebas funcionales, de límites y de errores (TC01 al TC08).
* `Consultas-SQL/`: Scripts utilizados para validar los estados en la base de datos de SQLite.
* `Reportes-de-Bugs/`: Documentación formal de los hallazgos críticos detectados durante el ciclo de pruebas (BUG-01, BUG-02 y BUG-03).
* `Evidencias/`: Capturas de pantalla de solicitudes en Postman y resultados de base de datos.

## 🔍 Aspectos Clave Validados
1. **Autenticación:** Uso de tokens Bearer dinámicos generados mediante el endpoint de usuarios.
2. **Pruebas de Límites:** Verificación del comportamiento del sistema al alcanzar el límite máximo (30 productos) e inferior (29 productos).
3. **Manejo de Errores y Transaccionalidad:** Comprobación de que la base de datos mantenga su integridad y rechace cambios ante datos inválidos o IDs inexistentes, previniendo alteraciones parciales.
