(1) | Campo                      | Valor                                                                                                                                                                                                                                                                                    |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tipo de incidente          | Phishing                                                                                                                                                                                                                                                                                 |
| Severidad                  | Alta                                                                                                                                                                                                                                                                                     |
| Activo afectado            | Laptop corporativa con Windows 11; credenciales del dominio empresarial comprometidas potencialmente; acceso a carpeta compartida de finanzas en riesgo.                                                                                                                                 |
| Primera acción recomendada | Reportar inmediatamente al SOC o equipo de seguridad. Solicitar el bloqueo o restablecimiento seguro de las credenciales comprometidas, revocar sesiones activas y verificar posibles accesos no autorizados. Evaluar el aislamiento de la laptop según el procedimiento interno.        |
| Información faltante       | Confirmar si hubo inicios de sesión sospechosos posteriores al envío de las credenciales, si la cuenta tiene MFA habilitado, la URL y el remitente del correo, si otros usuarios ingresaron sus credenciales, y si existen accesos o modificaciones inusuales en la carpeta de finanzas. |





(2) | Campo                      | Valor                                                                                                                                                                                                                                           |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tipo de incidente          | acceso no autorizado                                                                                                                                                                                                                            |
| Severidad                  | media                                                                                                                                                                                                                                           |
| Activo afectado            | Cuenta de correo electrónico                                                                                                                                                                                                                    |
| Primera acción recomendada | Reportar inmediatamente al equipo de seguridad para investigar el inicio de sesión sospechoso, revisar los registros de acceso, cerrar sesiones activas desconocidas y verificar que la autenticación multifactor esté habilitada.              |
| Información faltante       | Fecha y hora del inicio de sesión sospechoso, dirección IP y ubicación de origen, dispositivo utilizado, registros de acceso, existencia de actividad no reconocida posterior al cambio de contraseña y estado de la autenticación multifactor. |




(3) | Campo                      | Valor                                                                                                                                                                                                                                                                      |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tipo de incidente          | Acceso no autorizado                                                                                                                                                                                                                                                       |
| Severidad                  | Media                                                                                                                                                                                                                                                                      |
| Activo afectado            | Cuenta de correo personal utilizada para trabajo; posible exposición de la cuenta desde una ubicación no reconocida.                                                                                                                                                       |
| Primera acción recomendada | Verificar los registros de inicio de sesión y las sesiones activas; cerrar las sesiones desconocidas, cambiar la contraseña si no se ha hecho y activar la autenticación multifactor. Escalar al equipo de seguridad para investigar el acceso sospechoso.                 |
| Información faltante       | Fecha y hora del acceso sospechoso, ubicación y dispositivo de origen, confirmación de si el hermano utilizó la tablet, evidencia de acceso no autorizado, estado de la autenticación multifactor y confirmación de si el celular fue sustraído o estuvo fuera de control. |


