# User Stories Iniciales

## Contexto

Sistema de reclutamiento (ATS) con IA que permite gestionar vacantes, candidatos y evaluaciones en un pipeline tipo Kanban.

---

## User Stories

### US-01 - Crear y publicar una vacante
Como recruiter  
Quiero crear y publicar una vacante  
Para comenzar a recibir candidatos  

**Criterios de aceptación:**
- Se pueden completar los campos obligatorios (título, descripción, tipo, ubicación)
- La vacante puede guardarse como borrador o publicarse
- Al publicarse, se genera un link de aplicación

---

### US-02 - Gestionar candidatos en pipeline
Como recruiter o hiring manager  
Quiero ver y mover candidatos en un tablero Kanban  
Para gestionar el proceso de selección de forma visual  

**Criterios de aceptación:**
- El pipeline muestra etapas: Applied, Screening, Interview, Offer, Hired, Rejected
- Se pueden mover candidatos entre etapas
- Se visualiza información básica del candidato y su estado

---

### US-03 - Aplicar a una vacante
Como candidato  
Quiero postularme mediante un formulario  
Para ser considerado en el proceso  

**Criterios de aceptación:**
- El formulario permite cargar datos básicos y CV
- Se crea el candidato y su aplicación en el sistema
- El candidato recibe confirmación

---

### US-04 - Ver perfil del candidato
Como recruiter o hiring manager  
Quiero ver toda la información del candidato en un solo lugar  
Para tomar decisiones  

**Criterios de aceptación:**
- Se visualizan datos personales y CV
- Se muestran notas internas
- Se ve el historial del proceso

---

### US-05 - Evaluación automática con IA
Como recruiter  
Quiero que el sistema evalúe automáticamente los CVs  
Para priorizar candidatos  

**Criterios de aceptación:**
- Se asigna un score (0–100)
- Se muestra una clasificación (alto, medio, bajo)
- El resultado se guarda en el sistema

---

### US-06 - Autenticación y roles
Como usuario  
Quiero acceder al sistema con permisos según mi rol  
Para usar solo las funcionalidades correspondientes  

**Criterios de aceptación:**
- Login con email y contraseña
- Existen roles (admin, recruiter, hiring manager, interviewer)
- Cada rol tiene permisos diferenciados

---

## Backlog Priorizado

| ID | User Story | Prioridad |
|----|-----------|----------|
| US-06 | Autenticación y roles | Must |
| US-01 | Crear vacante | Must |
| US-03 | Aplicar a vacante | Must |
| US-02 | Pipeline Kanban | Must |
| US-04 | Ver candidato | Must |
| US-05 | Evaluación con IA | Should |

---

## Desglose técnico (US-02)

**Frontend**
- Componente de tablero Kanban
- Drag & drop de candidatos
- Visualización de estado

**Backend**
- Endpoint para obtener pipeline
- Endpoint para actualizar etapa
- Registro de cambios

**Base de datos**
- Tabla de aplicaciones con estado
- Tabla de historial de cambios

---

## Estimación

| Tarea | Story Points |
|------|-------------|
| Frontend | 8 |
| Backend | 5 |
| Base de datos | 3 |

---

## Conclusiones

- La autenticación es la base del sistema  
- El pipeline Kanban es la funcionalidad central  
- La evaluación con IA agrega valor pero depende de datos previos  