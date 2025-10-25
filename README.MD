# 🚀 Banco de Bogotá — Portal de Capacitaciones (Backend)

## Resumen ejecutivo
- Repositorio: backend del "Portal de Capacitaciones Interactivo". 🧭  
- Propósito: implementación completa en Spring (Spring Boot + Spring Data JPA) que expone APIs REST para los tres aplicativos definidos en el diagrama de arquitectura.
- Audiencia: personal de selección y primer contacto técnico.

## 📁 Estructura conceptual del repo
- apps/  
  - app-api-gateway/
  - app-user-management/
  - app-course-management/
- diseño/  
  - diagrama_arquitectura.drawio.pdf  
  - diagrama_er.drawio.pdf  
- Cloud _ Reto Middle – Portal de Capacitaciones Interactivo-031025-192751.pdf

> Cada aplicativo será un módulo Spring Boot independiente (posible multi-module Maven a través de Docker).

## 📌 Visión técnica
- Lenguaje: Java (21).  
- Framework: Spring Boot (Web, Data JPA, Security).  
- Persistencia: Spring Data JPA + Hibernate.  
- DB: PostgreSQL.
- Gestión: Maven.  
- Tests: JUnit + Mockito.

## 🗂️ Notas sobre la BD y JPA
- El esquema relacional se generará desde las entidades JPA.  
- Propiedades típicas (application.yml / properties):
  - spring.jpa.hibernate.ddl-auto=update
  - spring.jpa.show-sql=true
- El diagrama ER (diseño/diagrama_er.drawio.pdf) sirve como referencia de las entidades a implementar.

## 📋 Puntos clave para revisión técnica
- Modularidad: separación por responsabilidades (fácil de validar, testear y desplegar).
- Generación automática de esquema: facilita pruebas rápidas pero requiere control en producción.
- Observabilidad básica: logs y SQL mostrados en modo dev.  
- Seguridad: se integrará Spring Security con autentificación JWT stateless.

## 📎 Documentos y diagramas
- Requerimientos: `Cloud _ Reto Middle – Portal de Capacitaciones Interactivo-031025-192751.pdf`  
- Arquitectura: `diseño/diagrama_arquitectura.drawio.pdf`  
- Modelo ER: `diseño/diagrama_er.drawio.pdf`

## 📝 Próximos pasos (documentación)
- Añadir README por cada módulo con:
  - Endpoints (contratos OpenAPI / Swagger)  
  - Configuración de perfiles (dev/test/prod)  
  - Estrategia de migraciones (Flyway / Liquibase si aplica)  
- Indicar CI/CD y despliegue en cloud en documentación separada.

## 📬 Contacto / notas finales
- README inicial orientado a evaluación técnica. Documentación de detalle (contratos, CI/CD, políticas de seguridad) se añadirá en módulos y en la raíz según avance el desarrollo. 🙂
