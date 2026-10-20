(1)# Clasificación del incidente de seguridad

# Phishing con posible robo de credenciales

Clasificación inicial del SOC · Nivel 1

Alta prioridad

Severidad provisional

## Alta

Estado

### Incidente en investigación

Justificación: el usuario introdujo sus credenciales corporativas en una página sospechosa que imitaba el portal interno. Además, tiene acceso a una carpeta compartida de finanzas y otro empleado recibió el mismo correo. Existe riesgo de compromiso de la cuenta y de propagación del ataque.

## 1. Datos relevantes del incidente

| Campo                              | Clasificación                                 |
| ---------------------------------- | --------------------------------------------- |
| Tipo de incidente                  | Phishing y posible compromiso de credenciales |
| Vector de ataque                   | Correo electrónico con enlace malicioso       |
| Activo afectado                    | Laptop corporativa con Windows 11             |
| Cuenta potencialmente comprometida | Cuenta del dominio empresarial                |
| Recurso de interés                 | Carpeta compartida de finanzas                |
| Usuarios potencialmente afectados  | Al menos dos empleados                        |
| Momento del incidente              | Ayer, aproximadamente a las 15:00             |
| Confianza en la clasificación      | Alta                                          |
| Compromiso confirmado              | No; requiere investigación                    |

## 2. Indicadores de compromiso (IOC)

- Correo que aparenta provenir del área de TI y solicita restablecer la contraseña.
- Enlace que dirige a una página similar al portal interno.
- Captura de usuario y contraseña seguida del cierre de la página.
- Reporte de un segundo empleado que recibió el mismo mensaje.

Importante: el cierre de la página no demuestra que el ataque haya terminado. Tampoco confirma que se haya instalado malware ni que alguien haya utilizado las credenciales.

## 3. Acciones inmediatas para el técnico de seguridad

1\. Contener el posible compromiso de la cuenta

Contactar al equipo responsable de identidad para restablecer la contraseña desde un canal oficial, revocar sesiones activas y revisar los métodos de autenticación. No utilizar el enlace recibido.

2\. Investigar y contener el correo

Obtener el mensaje original con sus encabezados, URL, remitente y destinatarios. Buscar mensajes similares en el correo corporativo y retirarlos mediante los procedimientos autorizados.

3\. Revisar la laptop corporativa

Consultar las alertas del EDR, el historial de procesos y las conexiones de red. Si hay indicios de ejecución maliciosa o compromiso adicional, aislar el equipo según el procedimiento de respuesta.

4\. Verificar el acceso a finanzas

Revisar los registros de autenticación y acceso a archivos para identificar inicios de sesión inusuales, descargas masivas, modificaciones o accesos fuera del patrón habitual.

5\. Buscar otros usuarios afectados

Contactar al segundo empleado por un canal oficial, comprobar si hizo clic o introdujo credenciales y ampliar la búsqueda a toda la organización.

## 4. Evidencia que debe conservarse

- Correo original y encabezados completos.
- URL sospechosa y dominio de destino, sin volver a abrir el enlace en un equipo de producción.
- Hora aproximada del clic y del envío de credenciales.
- Registros de autenticación, cambios de contraseña y sesiones.
- Alertas del EDR y registros de acceso a la carpeta de finanzas.

No solicitar ni almacenar la contraseña en el ticket del incidente.

## 5. Criterios de escalamiento

Escalar inmediatamente al equipo de respuesta a incidentes (IR) si se detectan sesiones no reconocidas, accesos sospechosos a finanzas, reglas de correo maliciosas, uso de las credenciales por terceros o evidencia de ejecución de malware.

Conclusión para el ticket del SOC: incidente de phishing con exposición confirmada de credenciales por parte del usuario y posible compromiso de una cuenta corporativa. Se recomienda tratarlo como de alta prioridad, contener la cuenta, investigar la actividad posterior y determinar el alcance antes de cerrar el incidente.





(2) ## Clasificación del incidente de seguridad

1\. Tipo de incidente: Posible compromiso de cuenta de correo electrónico (acceso no autorizado).

2\. Prioridad: Alta (P2), provisional. Debe elevarse a crítica si se confirma actividad maliciosa con acceso a información sensible, cuentas privilegiadas o sistemas corporativos.

3\. Severidad: Media, provisional. No se ha confirmado que un tercero haya accedido a la cuenta.

4\. Activo afectado: Cuenta de correo electrónico del usuario.

5\. Indicadores identificados:

- Aviso inusual de inicio de sesión.
- Posible acceso desde un dispositivo o ubicación desconocidos.
- Fecha y origen del evento sin determinar.
- Contraseña cambiada por el usuario, sin confirmar si se revocaron las sesiones activas.

6\. Impacto potencial:

- Acceso no autorizado a correos y archivos adjuntos.
- Robo de información confidencial.
- Uso de la cuenta para enviar phishing.
- Restablecimiento de contraseñas de otros servicios vinculados.

7\. Acciones de respuesta recomendadas:

1. Verificar la legitimidad de la alerta y revisar el historial de inicios de sesión.
2. Revocar las sesiones activas y los tokens de acceso, cuando sea posible.
3. Confirmar el cambio de contraseña y activar la autenticación multifactor (MFA).
4. Revisar reglas de reenvío, filtros, métodos de recuperación y aplicaciones conectadas.
5. Comprobar si hubo envíos de correos sospechosos o modificaciones no autorizadas.
6. Registrar las evidencias disponibles y escalar al equipo de seguridad si se confirma actividad maliciosa.

8\. Información faltante:

- Fecha y hora exactas del inicio de sesión sospechoso.
- Dirección IP, ubicación y dispositivo de origen.
- Tipo de cuenta: personal o corporativa.
- Existencia de sesiones activas desconocidas.
- Estado de la autenticación multifactor.

9\. Estado del incidente: Abierto, pendiente de investigación.

10\. Justificación: El aviso de inicio de sesión inusual puede indicar un intento de acceso o un compromiso real de la cuenta. Cambiar la contraseña es una medida adecuada, pero no garantiza que se hayan cerrado las sesiones existentes ni que se hayan eliminado mecanismos de persistencia.

Recomendación para el técnico: No cerrar el incidente únicamente porque el usuario cambió su contraseña. Verificar los registros de autenticación y contener cualquier acceso no autorizado antes de darlo por resuelto.








(3) ## Clasificación del incidente de seguridad

Clasificación principal: Posible acceso no autorizado a una cuenta de correo electrónico.

Prioridad sugerida: Media, pendiente de investigación. Puede elevarse si se confirma el acceso malicioso o existe exposición de información corporativa.

### 1. Datos del incidente

| Campo                   | Clasificación                                                 |
| ----------------------- | ------------------------------------------------------------- |
| Tipo de incidente       | Posible acceso no autorizado a una cuenta                     |
| Activo afectado         | Cuenta de correo personal utilizada para trabajo              |
| Dispositivo involucrado | Celular y posible tablet compartida                           |
| Estado                  | No confirmado; requiere investigación                         |
| Impacto potencial       | Exposición de correos e información laboral                   |
| Certeza                 | Indicios sospechosos, sin evidencia concluyente de compromiso |

### 2. Justificación

- Acceso no autorizado: existe un inicio de sesión desde una ubicación desconocida. Es el principal indicador que debe investigarse.
- Pérdida o robo de dispositivo: el usuario sospecha que perdió su celular, pero lo encontró en su mochila. No hay evidencia suficiente para clasificarlo como pérdida o robo confirmado.
- Posible actividad legítima: el hermano pudo haber utilizado la tablet, pero esta hipótesis no confirma que el inicio de sesión fuera legítimo.
- Uso laboral de la cuenta: aunque es personal, podría contener información relacionada con el trabajo, por lo que debe evaluarse el riesgo para la organización.

### 3. Acciones recomendadas para el técnico

1. Revisar el historial de inicios de sesión, incluyendo fechas, ubicaciones, dispositivos y direcciones IP disponibles.
2. Verificar si la actividad desconocida coincide con el uso de la tablet o con alguna conexión legítima.
3. Comprobar si hubo cambios de contraseña, reglas de reenvío, sesiones activas desconocidas o modificaciones de recuperación de la cuenta.
4. Recomendar cerrar las sesiones desconocidas, cambiar la contraseña si existe sospecha de compromiso y activar la autenticación multifactor.
5. Determinar si se accedió a información laboral y escalar al equipo de seguridad de la organización si corresponde.

### 4. Decisión final

Registrar como posible acceso no autorizado

No clasificarlo como robo confirmado del dispositivo ni descartarlo como un malentendido. Mantener el incidente abierto hasta verificar la actividad.

Nota para el técnico: La ausencia de certeza por parte del usuario no elimina la necesidad de investigar. Registrar los hechos confirmados por separado de las hipótesis y ajustar la clasificación cuando existan evidencias suficientes.