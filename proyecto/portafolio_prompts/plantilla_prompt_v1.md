# Plantilla: Clasificación de Incidentes de Ciberseguridad v1

## Variables
- `{ROL_LECTOR}`: A quién va dirigida la información (ej. "técnico que atenderá el incidente", "mesa de ayuda N1").
- `{CATEGORIAS}`: Lista de tipos de incidente permitidos (ej. "acceso no autorizado, phishing, malware, pérdida de dispositivo, otro").
- `{SEVERIDADES}`: Niveles de severidad permitidos (ej. "baja, media, alta").
- `{ENTRADA}`: El texto libre del reporte de incidente escrito por el usuario.

---

## Prompt

Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es {ROL_LECTOR} y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: {CATEGORIAS}. Las severidades posibles son: {SEVERIDADES}.

Ejemplo de entrada:
"Recibí un correo del banco pidiendo que confirme mi tarjeta en un enlace. Di clic y puse mis datos. Fue hoy a las 10 am desde la laptop de la oficina."

Ejemplo de salida:
| Campo | Valor |
|---|---|
| Tipo de incidente | phishing |
| Severidad | alta |
| Activo afectado | credenciales bancarias del usuario; laptop de oficina |
| Primera acción recomendada | contactar al banco para bloquear la tarjeta y reportar al área de seguridad |
| Información faltante | ninguna |

Clasifica este reporte de incidente:

{ENTRADA}

Responde únicamente con esta tabla en Markdown, sin texto adicional:

| Campo | Valor |
|---|---|
| Tipo de incidente | |
| Severidad | |
| Activo afectado | |
| Primera acción recomendada | |
| Información faltante | |

Si un campo no puede determinarse a partir del texto, escribe "NO ESPECIFICADO" en Valor y explica qué falta en la fila "Información faltante".

---

## Instrucciones de uso
- **Modelo probado:** ChatGPT (GPT-4o, versión web).
- **Puntaje obtenido:** 18/18 en las iteraciones 3, 4 y 5; 6/6 en la prueba de robustez (Entrada 4 - Malware).
- **Limitaciones conocidas:** 
  1. El modelo depende de que el usuario describa bien el "activo afectado"; si el usuario es muy vago, el modelo podría poner "NO ESPECIFICADO" en campos que sí se podían inferir.
  2. Para la categoría "otro", el modelo a veces intenta forzar la entrada a "acceso no autorizado" si no está seguro.
  3. La plantilla está optimizada para incidentes reportados por usuarios finales, no para alertas automáticas de sistemas (SIEM/EDR).