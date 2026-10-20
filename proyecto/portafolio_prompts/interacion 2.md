(1) ## Clasificación del incidente

Tipo de incidente: Phishing Severidad: Alta

### Información para el técnico de seguridad

- Descripción: El usuario recibió un correo aparentemente enviado por el área de TI que solicitaba restablecer la contraseña de Windows mediante un enlace. Hizo clic e introdujo sus credenciales corporativas en una página que imitaba el portal interno.
- Fecha y hora del evento: Ayer, a las 15:00 h.
- Activo afectado: Laptop corporativa con Windows 11 y cuenta de dominio empresarial.
- Indicadores de compromiso: Posible robo de credenciales mediante una página falsa. Otro empleado recibió el mismo correo, lo que sugiere una campaña de phishing dirigida a usuarios de la organización.
- Riesgo asociado: Acceso no autorizado a la cuenta corporativa y posible exposición de la carpeta compartida de Finanzas.
- Estado: Incidente pendiente de investigación. No se ha confirmado que las credenciales hayan sido utilizadas por un tercero.

### Acciones recomendadas

1. Escalar inmediatamente al equipo de seguridad por el riesgo para la cuenta corporativa y los recursos financieros compartidos.
2. Restablecer las credenciales desde un canal oficial y seguro, revocar las sesiones activas y revisar los métodos de autenticación configurados.
3. Revisar los registros de autenticación para identificar inicios de sesión sospechosos, accesos desde ubicaciones desconocidas y posibles cambios en la cuenta.
4. Analizar el correo y el enlace malicioso, incluyendo remitente, URL y posibles destinatarios adicionales.
5. Evaluar los accesos a la carpeta compartida de Finanzas para detectar actividad inusual o extracción de información.
6. Revisar la laptop corporativa en busca de indicios de malware o actividad sospechosa, sin asumir que el equipo está infectado únicamente por haber abierto el enlace.
7. Advertir al compañero y a otros posibles destinatarios que no abran el enlace ni introduzcan sus credenciales.

### Justificación de la severidad

La severidad es alta porque el usuario entregó credenciales corporativas en una página posiblemente fraudulenta, su cuenta tiene acceso a información financiera y existe evidencia de que el mismo correo llegó a otro empleado. Aunque todavía no se ha confirmado un acceso indebido, el riesgo potencial justifica una atención prioritaria.

Nota para el técnico: La clasificación principal es phishing. El acceso no autorizado debe investigarse como una posible consecuencia, no como un hecho confirmado.



(2) ## Clasificación del incidente

- Tipo de incidente: Acceso no autorizado.
- Severidad: Media.

### Justificación

El usuario recibió una alerta de inicio de sesión desconocido en su correo electrónico, lo que sugiere un posible acceso no autorizado. Aunque cambió la contraseña, se desconoce cuándo ocurrió el evento, desde qué dispositivo se realizó y si el acceso no autorizado continúa.

La severidad se clasifica como media porque existe evidencia de actividad sospechosa en una cuenta, pero no se ha confirmado el alcance del incidente ni un impacto adicional.

### Acciones recomendadas para el técnico

1. Revisar los registros de inicio de sesión, las direcciones IP, las ubicaciones y los dispositivos asociados.
2. Verificar si hubo cambios en la configuración de la cuenta, reglas de reenvío o métodos de recuperación.
3. Cerrar las sesiones activas y revocar los tokens de acceso sospechosos.
4. Confirmar que la autenticación multifactor (MFA) esté habilitada y que los métodos de recuperación sean legítimos.
5. Determinar si hubo acceso a información sensible o actividad adicional no autorizada.

Nota para el SOC: La clasificación es preliminar. Se debe elevar a severidad alta si se confirma el acceso a información sensible, el compromiso de otras cuentas o una actividad maliciosa en curso.



(3) Tipo de incidente: Acceso no autorizado

Severidad: Media

Justificación: Se reporta un inicio de sesión en una cuenta de correo desde una ubicación desconocida. Aunque existe la posibilidad de que el acceso haya sido realizado por un familiar desde una tableta personal, no hay evidencia suficiente para confirmar ni descartar un acceso no autorizado. La posible pérdida del celular tampoco está confirmada, ya que el dispositivo apareció posteriormente en la mochila.

Acciones recomendadas:

- Verificar los registros de inicio de sesión, las ubicaciones, los dispositivos y las horas de acceso.
- Confirmar con el usuario si su hermano utilizó la cuenta desde la tableta.
- Revisar si hubo cambios en la configuración, reglas de correo o actividad sospechosa.
- Verificar si la cuenta tiene sesiones activas desconocidas y revocarlas si procede.
- Confirmar si el celular estuvo fuera de su control y si contiene sesiones corporativas.

Prioridad de atención: Investigar el posible acceso no autorizado, ya que la cuenta personal también se utiliza para actividades laborales.

Nota: La clasificación es provisional. La severidad media es una estimación inicial y debe ajustarse según los resultados de la investigación y el impacto potencial en los recursos corporativos.