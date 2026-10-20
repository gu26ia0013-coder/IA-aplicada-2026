# Iteración 0 — Línea base (zero-shot)

**Prompt utilizado:** 
Clasifica este reporte de incidente: [Entrada]

## Resultados por entrada

### Entrada 1 (Clara y completa)
**Respuesta del modelo:**
> Incidente de phishing con posible robo de credenciales. 
> Prioridad alta. Compromiso posible. 
> Tipo de incidente: Phishing exitoso a nivel de captura de credenciales. 
> Justificación: La persona hizo clic en un enlace sospechoso e introdujo su usuario y contraseña corporativos en una página falsa que imitaba el portal interno. Además, otro compañero recibió el mismo correo, lo que sugiere una campaña de phishing dirigida a la organización.
> 
> **1. Datos relevantes**
> - Fecha y hora: Ayer a las 15:00.
> - Equipo afectado: Laptop corporativa con Windows 11.
> - Activo en riesgo: Cuenta corporativa y carpeta compartida de finanzas.
> - Indicadores sospechosos: Correo que suplanta al área de TI, enlace falso y página que se cerró después de recibir las credenciales.
> - Alcance potencial: Otros empleados podrían recibir el mismo correo.
> 
> **2. ¿Qué debe hacer la persona?**
> 1. Reportar inmediatamente el incidente al equipo de TI o de respuesta a incidentes de seguridad.
> 2. Cambiar la contraseña desde un portal oficial, utilizando un dispositivo confiable y siguiendo las indicaciones de TI. Si reutiliza esa contraseña en otros servicios, también debe cambiarlas.
> 3. Solicitar la revocación de sesiones activas y la revisión de los inicios de sesión recientes, así como verificar si hubo accesos no autorizados a la carpeta de finanzas.
> 4. Conservar el correo sospechoso para que el equipo de seguridad analice el remitente, el enlace y los encabezados. No volver a abrir el enlace.
> 5. Avisar al compañero y al equipo de seguridad que el mismo correo está circulando. Si se detectan otras señales de compromiso, seguir las instrucciones de TI sobre el aislamiento del equipo.
> 
> **3. Clasificación final para el registro**
> | Campo | Resultado |
> | :--- | :--- |
> | Categoría | Phishing |
> | Subcategoría | Robo de credenciales |
> | Severidad inicial | Alta |
> | Estado | En investigación |
> | Impacto potencial | Acceso no autorizado a sistemas y archivos corporativos |
> | Acción prioritaria | Contención de la cuenta y análisis de accesos |
> 
> Importante: No está confirmado que alguien haya utilizado las credenciales robadas. Sin embargo, como se introdujeron en una página falsa, deben considerarse comprometidas hasta que el equipo de seguridad determine lo contrario.

**Calificación:** C1: 2 | C2: 1 | C3: 1 | **Total: 4/6**

---

### Entrada 2 (Información faltante)
**Respuesta del modelo:**
> ## Clasificación del reporte de incidente
> 
> - Tipo de incidente: Posible acceso no autorizado a una cuenta de correo electrónico.
> - Categoría: Ciberseguridad → Compromiso de cuentas.
> - Nivel de riesgo: Alto (potencial), hasta verificar si el acceso fue legítimo.
> - Prioridad: Alta.
> - Estado: Pendiente de investigación.
> - Impacto: Posible pérdida de confidencialidad de la información personal o empresarial.
> 
> **Análisis del reporte**
> | Indicador | Observación |
> | :--- | :--- |
> | Señal de alerta | Aviso inusual de inicio de sesión. |
> | Información desconocida | Fecha, dispositivo y origen del acceso. |
> | Acción realizada | El usuario cambió su contraseña. |
> | Riesgo restante | Podrían existir sesiones activas o métodos de recuperación comprometidos. |
> | Información faltante | Registros de acceso, ubicación, actividad reciente y cambios en la cuenta. |
> 
> **¿Qué debe hacer el usuario?**
> 1. Reportar el incidente al equipo de soporte o seguridad informática, aunque ya haya cambiado la contraseña.
> 2. Revisar la actividad reciente e identificar los inicios de sesión desconocidos.
> 3. Cerrar todas las sesiones activas y habilitar la autenticación multifactor (MFA).
> 4. Verificar que no se hayan modificado las opciones de recuperación, las reglas de reenvío ni los permisos de la cuenta.
> 5. Conservar el aviso recibido como evidencia para la investigación.
> 
> Conclusión: El incidente debe clasificarse como un posible compromiso de cuenta por acceso no autorizado. Cambiar la contraseña es una medida inicial útil, pero no garantiza que la cuenta esté completamente protegida. La clasificación es preliminar y debe confirmarse mediante la investigación de los registros de acceso.

**Calificación:** C1: 2 | C2: 0 | C3: 2 | **Total: 4/6**

---

### Entrada 3 (Ambigua o contradictoria)
**Respuesta del modelo:**
> ## Clasificación del incidente
> **Posible acceso no autorizado**
> Prioridad: Media, pendiente de evaluación
> Clasificación principal: Posible acceso no autorizado a una cuenta de correo.
> Clasificación secundaria: Posible pérdida temporal de dispositivo, aún no confirmada.
> 
> **¿Por qué se clasifica así?**
> - Acceso no autorizado: Hay un inicio de sesión desde una ubicación desconocida. Aunque pudo haber sido el hermano del usuario, todavía no se ha confirmado.
> - Pérdida de dispositivo: El celular apareció en la mochila, por lo que no hay evidencia suficiente para confirmar un robo o una pérdida definitiva.
> - Uso laboral de la cuenta: Aunque el correo es personal, también se utiliza para trabajar, lo que podría implicar un riesgo para la información laboral.
> - No es recomendable descartarlo: La incertidumbre no significa que no exista un incidente de seguridad.
> 
> **¿Qué debe hacerse?**
> 1. Reportar el caso como posible acceso no autorizado al equipo de seguridad o soporte de TI.
> 2. Revisar el historial de inicios de sesión, los dispositivos conectados y la ubicación aproximada del acceso.
> 3. Cambiar la contraseña desde un dispositivo confiable y activar la autenticación multifactor si hay indicios de acceso ajeno.
> 4. Confirmar con el hermano si utilizó la tablet y revisar si el acceso coincide con esa actividad.
> 5. Registrar la posible pérdida temporal del celular como un dato adicional, no como un robo confirmado.
> 
> **Clasificación final para el reporte**
> Tipo: Acceso no autorizado sospechado.
> Estado: Pendiente de investigación.
> Justificación: Se detectó un inicio de sesión desde una ubicación desconocida en una cuenta personal utilizada también para trabajo. La identidad de quién accedió no está confirmada y la supuesta pérdida del celular tampoco está comprobada.
> Conclusión: Se debe reportar como un posible incidente de seguridad, no como un malentendido confirmado ni como un robo de dispositivo confirmado. La investigación determinará si realmente hubo acceso no autorizado.

**Calificación:** C1: 2 | C2: 0 | C3: 2 | **Total: 4/6**

---

## Tabla Resumen Iteración 0

| Entrada | C1 Completitud | C2 Formato | C3 Incertidumbre | Total /6 |
| :--- | :--- | :--- | :--- | :--- |
| Entrada 1 (Phishing) | 2 | 1 | 1 | **4** |
| Entrada 2 (Faltante) | 2 | 0 | 2 | **4** |
| Entrada 3 (Ambigua) | 2 | 0 | 2 | **4** |
| **Total iteración** | **6/6** | **1/6** | **5/6** | **12/18** |

**Observaciones generales:** El modelo demuestra un buen manejo de la incertidumbre (C3) de forma natural, pero falla estrepitosamente en mantener un formato estandarizado (C2). Cada entrada generó una estructura visual completamente distinta (tablas al final, viñetas, texto largo), lo que hace imposible procesar las respuestas de forma automatizada o rápida. 