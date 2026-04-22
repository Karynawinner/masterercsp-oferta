# Máster ERCSP — Página de Oferta y Matrícula

Página web del **Máster en Economía, Regulación y Competencia en los Servicios Públicos** (Universidad de Barcelona).

Incluye el plan de estudios detallado y formularios interactivos de elección de asignaturas para todos los itinerarios.

---

## Archivos

| Archivo | Descripción |
|---|---|
| `index.html` | Página principal — plan de estudios + formularios de matrícula |

---

## Itinerarios disponibles

**Opción en español:**
- ⚖️ Itinerario Juristas
- 📊 Itinerario Economistas
- 🏛️ Itinerario Ingenieros y Politólogos

**Opción bilingüe (Español / English):**
- 📊 Itinerario Economistas
- 🏛️ Itinerario Ingenieros y Politólogos

---

## Configuración de Airtable (solo administradores)

Los formularios envían los datos a Airtable. La configuración se realiza directamente en la página — **el token nunca aparece en el código fuente**.

**Cómo configurar:**
1. Abre la página en el navegador
2. Pulsa **Ctrl + Shift + A**
3. Introduce el **API Token** y el **Base ID** de Airtable
4. Pulsa **Guardar**

> ⚠️ Esta configuración se guarda solo en el navegador local. Cada administrador debe configurarlo una vez en su propio navegador.

---

## Estructura de datos en Airtable

Base: **MasterERCSP** — dos tablas relacionadas:

**Tabla `Estudiantes`**
| Campo | Tipo |
|---|---|
| Primer apellido | Single line text |
| Segundo apellido | Single line text |
| Nombre | Single line text |
| Teléfono | Phone number |
| Email | Email |
| Itinerario | Single line text |
| Asignaturas | Link to → Asignaturas |
| Fecha | Created time (automático) |

**Tabla `Asignaturas`**
| Campo | Tipo |
|---|---|
| Asignatura | Single line text |
| ECTS | Number (decimal) |
| Tipo | Single line text |
| Estudiante | Link to → Estudiantes (automático) |

---

## Tecnología

- HTML5 / CSS3 / JavaScript puro (sin frameworks ni dependencias)
- Airtable API v0
- Compatible con WordPress para integración futura
