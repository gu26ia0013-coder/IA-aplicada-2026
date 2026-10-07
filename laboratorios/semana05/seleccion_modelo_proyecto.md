# Selección de modelo generativo para el proyecto "El lado digital"

## Modelos evaluados
- **Gemini** (versión gratuita web, modelo Flash-Lite): fue el único modelo probado en este laboratorio. Se eligió por su acceso gratuito, disponibilidad inmediata y capacidad de procesar documentos extensos en español.

## Evidencia de tokens
- **Tokens de mi documento de referencia:** ~1,860 tokens (4 páginas, ~1,300 palabras).
- **Caracteres por token en español:** 5.29 (medido en un párrafo de 100 palabras).
- **Caracteres por token en inglés:** 6.40 (mismo párrafo traducido).
- **Implicación para mi proyecto:** el español consume ~40% más tokens que el inglés para decir lo mismo, porque las palabras españolas se fragmentan en más subpalabras. Esto significa que los documentos en español agotan la ventana de contexto más rápido y debo planear ya sea dividir documentos largos o usar un modelo con ventana amplia.

## Evidencia de temperatura
- **Temperatura para tareas de precisión** (explicar normas, redactar avisos, responder consultas técnicas): la más baja posible. Evidencia: en el modo "predecible" de la prueba, las respuestas fueron idénticas entre sí (2 de 3 ejecuciones iguales), lo que demuestra que la instrucción reduce la variabilidad. Para un proyecto de ciberseguridad necesito respuestas estables y consistentes.
- **Temperatura para tareas creativas** (proponer nombres, analogías, explicaciones didácticas): la más alta posible. Evidencia: en el modo "creativo" obtuve 3 respuestas completamente distintas ("portero cuántico", "dragón digital paranoico", "gorila digital con armadura medieval"), lo que demuestra que la variabilidad aumenta con la instrucción creativa.

## Evidencia de contexto
- El modelo **encontró correctamente la aguja** (código AZUL-7342) con 1, 2 y 4 copias del documento (~1,860 a ~7,440 tokens).
- Al intentar con **8 copias (~14,880 tokens)**, la interfaz web de Gemini **rechazó el texto** por exceder su límite de entrada.
- La aguja se encontró **sin importar su posición** (inicio, mitad o final del documento), lo que indica que Gemini Flash-Lite no sufre el fenómeno "lost in the middle".
- **Mis documentos del proyecto** pueden medir entre ~1,860 y ~5,000 tokens cada uno. Por lo tanto: **caben completos si son de hasta 4 páginas, pero debo dividirlos en fragmentos si son más largos**, para no arriesgar que la interfaz rechace la consulta.

## Decisión
- **Modelo elegido:** Gemini (versión gratuita web, Flash-Lite).
- **Configuración:** temperatura baja o instrucción "predecible" para tareas de precisión; temperatura alta o instrucción "creativa" para tareas de generación de ideas.
- **Restricciones de datos según la política de la semana 4:** no usar datos personales reales; los documentos de prueba deben ser ficticios o públicos; anonimizar cualquier información sensible antes de pasarla al modelo; no subir documentos con datos de clientes, contraseñas o información clasificada.