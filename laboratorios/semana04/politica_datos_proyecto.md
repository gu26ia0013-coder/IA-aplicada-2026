# Política de datos del proyecto Sistema de Control de Acceso

## 1. Alcance

Esta política cubre los siguientes datos tratados por el sistema de control de acceso:

- D1 — ID interno (No personal)
- D2 — Nombre (Personal)
- D3 — Correo electrónico (Personal)
- D4 — Teléfono (Personal) — dato de mayor riesgo
- D5 — Fecha de acceso (Personal)
- D6 — Hora de entrada (Personal)
- D7 — Área (No personal)
- D8 — Empresa (No personal)
- D9 — Motivo de visita (No personal)

Aplica a todo el personal interno, proveedores de nube y terceros que traten estos datos.

## 2. Ciclo de vida

El ciclo de vida está representado en `ciclo_vida_dato_proyecto.drawio` y `ciclo_vida_dato_proyecto.png`. Las seis etapas son:

- Captura — Responsable: Administrador del sistema de acceso
- Almacenamiento — Responsable: Proveedor de nube / Administrador de base de datos
- Uso — Responsable: Líder del proyecto / Analista de datos
- Compartición — Responsable: Líder del proyecto
- Retención — Responsable: Administrador de base de datos
- Eliminación — Responsable: Administrador de base de datos

El dato de mayor riesgo (D4, teléfono) se sigue en rojo a lo largo de las seis etapas.

## 3. Normativa aplicable

Aplican tres marcos:

- **LFPDPPP México (2025)** — Obligatoria. Rige el tratamiento de datos personales en posesión de particulares. Principios: licitud, consentimiento, información, calidad, finalidad, lealtad, proporcionalidad y responsabilidad. El art. 26, fracción II reconoce el derecho del titular a oponerse a decisiones automatizadas sin intervención humana.
- **Ley de IA de la Unión Europea (Reglamento 2024/1689)** — Aplicable si el sistema se usa en territorio europeo. Establece obligaciones de transparencia y supervisión humana.
- **NIST AI RMF 1.0** — Voluntario. Marco de gestión de riesgos con cuatro funciones: Gobernar, Mapear, Medir y Gestionar.

Detalle completo en `matriz_cumplimiento_proyecto.xlsx`.

## 4. Controles comprometidos

| Control | Responsable |
|---------|-------------|
| Aviso visible de sistema automatizado | Administrador del sistema de acceso |
| Casilla de consentimiento antes de enviar formulario | Administrador del sistema de acceso |
| Publicación del aviso de privacidad con finalidades declaradas | Líder del proyecto |
| Captura mínima de datos (solo nombre, correo, teléfono) | Administrador del sistema de acceso |
| Análisis de riesgos documentado antes del despliegue | Líder del proyecto |
| Supervisión humana sobre alertas de reincidencia | Analista de datos |
| Auditoría trimestral de sesgos | Analista de datos |
| Formulario de oposición a decisiones automatizadas | Líder del proyecto |
| Retención definida en 12 meses con revisión trimestral | Administrador de base de datos |
| Borrado seguro con confirmación documentada | Administrador de base de datos |
| Enmascaramiento del teléfono al compartir (55****1234) | Líder del proyecto |
| Contrato de tratamiento de datos con terceros | Líder del proyecto |

## 5. Manejo de datos con herramientas de IA

Reglas obligatorias para todo el equipo:

- **Datos que NO pueden ingresarse a ChatGPT, Gemini, Deepseek, Dify u otras herramientas de IA:** D2 (nombre), D3 (correo), D4 (teléfono), D5 (fecha de acceso), D6 (hora de entrada) y cualquier combinación que permita identificar a una persona.
- **Datos que sí pueden ingresarse:** D1 (ID), D7 (área), D8 (empresa) y D9 (motivo), siempre que no se combinen con datos personales.
- **Cuando se requiera usar datos reales para pruebas o prompts:** deben anonimizarse previamente (reemplazar nombres por ficticios, teléfonos por 555-0000, correos por ejemplo@test.com) o generarse datos sintéticos.
- **Prohibido:** pegar extractos de la base de datos, capturas con datos visibles, o prompts que incluyan información de visitantes reales.
- **Excepción:** solo con autorización escrita del Líder del proyecto y con contrato de confidencialidad firmado con el proveedor de IA.

## 6. Revisión

Esta política se revisará **cada seis meses** o antes si ocurre:

- Un cambio normativo (nueva ley, reforma o abrogación).
- Un incidente de seguridad relacionado con datos personales.
- Un cambio en los terceros que tratan datos del proyecto.

La aprobación corresponde al **Líder del proyecto**, con visto bueno del **Administrador de base de datos**.

---

**Última actualización:** 4 de octubre de 2026
**Versión:** 1.0