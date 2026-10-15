# Documento post-mortem

Para esta actividad el equipo asume que la solución propuesta presentó un incidente significativo durante su implementación. El incidente es simulado y está construido a partir de los hallazgos de las entrevistas.

## 1. Resumen del incidente

| Dato | Detalle |
|---|---|
| Fecha | 21 de septiembre, primer lunes de la semana de exámenes presenciales |
| Duración | Aproximadamente 3 horas (de 9:40 AM a 12:30 PM) |
| Sistemas afectados | Módulo de sugerencia diaria y calendario de actividad universitaria |
| Procesos afectados | Compra y preparación de producto, atención en el mostrador |
| Áreas del negocio | Kiosco de Shucos El Chatío y apoyo del local de panes Los Chatos |
| Gravedad | Alta |

**¿Qué ocurrió?** Durante la primera semana de exámenes tras la entrega de la fase 1, la sugerencia diaria indicó una actividad baja y recomendó preparar poco producto. En realidad llegaron muchos más estudiantes de lo esperado, el producto se agotó a media mañana y se formaron filas. La causa inmediata fue que el calendario no tenía cargadas las

## 2. Línea de tiempo (timeline)

| Hora aproximada | Evento |
|---|---|
| 3:00 AM | Heidi compra en la terminal siguiendo la sugerencia: actividad baja. |
| 5:00 AM | Inicia la preparación con las cantidades recomendadas. |
| 7:30 AM | Apertura del puesto con ventas normales. |
| 9:40 AM | Llegan más estudiantes de lo habitual por los exámenes de la facultad. |
| 10:15 AM | Se agota el aguacate y se empiezan a acabar los panes; comienza la fila. |
| 10:30 AM | Heidi llama a otro local para pedir apoyo con producto. |
| 11:00 AM | Heidi reporta el problema a Brandon. Ilse revisa el sistema y detecta que el calendario no tiene los exámenes. |
| 11:45 AM | Ilse carga manualmente las fechas desde la plataforma de la facultad. |
| 12:10 PM | Karla verifica la sugerencia corregida con tres casos de prueba. |
| 12:30 PM | La sugerencia indica actividad alta y se prepara una segunda tanda. |
| 2:00 PM | Reunión de equipo para registrar el incidente y definir mejoras. |

## 3. Impacto

### Quiénes se vieron afectados

- **Dueña y personal del kiosco (Heidi):** debieron improvisar y atender con producto limitado.
- **Estudiantes:** esperaron en fila o se fueron sin comprar.
- **Local de panes (B y E):** tuvo que atender llamadas de apoyo en horas de trabajo.
- **Equipo de desarrollo:** debió detener otras tareas para corregir el sistema.

### Efectos directos

- Producto agotado durante aproximadamente 2 horas en plena hora de mayor demanda (valor simulado).
- Filas de hasta unos 40 estudiantes (valor simulado).
- Interrupción del servicio normal por la preparación de emergencia.

### Efectos indirectos

- Ventas perdidas que no se pueden recuperar.
- Pérdida de confianza de la clienta en la sugerencia diaria.
- Retrasos en las tareas de la fase 2.
- Posible pérdida de clientes que desistieron por la espera.

### Gravedad

| Afectado | Impacto |
|---|---|
| Negocio (ventas del día) | Alto |
| Estudiantes (espera) | Medio |
| Equipo de desarrollo (retrabajo) | Medio |
| Datos del sistema | Bajo, no hubo pérdida de información |

## 4. Causa raíz

### 4.1 Análisis de los 5 porqués

| Nivel | Pregunta | Respuesta |
|---|---|---|
| 1 | ¿Por qué se agotó el producto a media mañana? | Porque se compró y preparó para un día de poca actividad. |
| 2 | ¿Por qué se preparó para poca actividad? | Porque la sugerencia diaria indicó actividad baja. |
| 3 | ¿Por qué la sugerencia indicó actividad baja? | Porque el calendario no tenía las fechas de exámenes y el historial venía de días con la universidad cerrada o virtual. |
| 4 | ¿Por qué el calendario no tenía esas fechas? | Porque la carga era manual y no había un responsable ni una fecha de revisión definida. |
| 5 | ¿Por qué no había responsable ni revisión? | Porque al priorizar la fecha de entrega, los criterios de aceptación no incluyeron verificar los datos del calendario ni probar con una semana de exámenes real. |

### 4.2 Causa raíz y decisiones del proyecto

**Causa raíz.** El sistema dependía de datos cargados a mano (calendario de exámenes) sin un proceso de actualización ni una validación previa, y la sugerencia no avisaba cuando sus datos eran pobres o antiguos.

**Relación con las decisiones del proyecto.** En la junta directiva se acordó una fecha firme de entrega y un piloto de un día. El piloto se hizo en un día normal, no en una semana de exámenes, y los criterios de aceptación revisaban la funcionalidad (dos toques, sugerencia visible) pero no la calidad ni la vigencia de los datos. Fue una consecuencia del trade-off entre tiempo y alcance, no de un error de una sola persona.


## 5. Acciones tomadas para solucionarlo

| Hora | Quién | Acción | Aporte a la solución |
|---|---|---|---|
| 10:30 AM | Heidi | Pidió apoyo al otro local y preparó producto adicional. | Mitigó la falta de producto. |
| 11:00 AM | Brandon | Priorizó el problema y detuvo otras tareas del equipo. | Concentró al equipo en el incidente. |
| 11:00 AM | Ilse | Revisó el sistema y encontró que faltaban los exámenes. | Identificó la causa inmediata. |
| 11:45 AM | Ilse | Cargó manualmente las fechas desde la plataforma de la facultad. | Corrección temporal. |
| 12:10 PM | Karla | Verificó la sugerencia corregida con tres casos de prueba. | Confirmó que la corrección funcionaba. |
| 12:30 PM | Elner | Revisó cómo se calcula la sugerencia y propuso un margen mínimo. | Evita subestimar la demanda. |
| 1:00 PM | Apen | Registró cronológicamente el incidente para el post-mortem. | Base documental del análisis. |
| 2:00 PM | Darlin | Dirigió la reunión de equipo y levantó el acta con los acuerdos. | Ordenó las acciones de mejora. |

## 6. Acciones a futuro

| N.º | Acción | Causa que ataca | Responsable | Plazo | Indicador |
|---|---|---|---|---|---|
| 1 | Asignar un responsable semanal para cargar y revisar el calendario con checklist. | Nivel 4: no había responsable | Brandon | Inmediato | Calendario actualizado cada lunes |
| 2 | Alerta de calendario sin actualizar por más de 7 días. | Nivel 3: datos ausentes o antiguos | Ilse | 1 semana | Alerta visible en pantalla |
| 3 | Mostrar nivel de confianza en la sugerencia y un margen de seguridad. | Causa raíz: sugerencia sin aviso de datos pobres | Elner | 2 semanas | Sugerencia con confianza visible |
| 4 | Mínimo de historial antes de mostrar una sugerencia. | Nivel 3: historial no representativo | Elner | 2 semanas | Sin sugerencia con menos de 14 días de historial |
| 5 | Pruebas en una semana de exámenes antes de cerrar una fase. | Nivel 5: sin prueba con demanda real | Karla | Próxima fase | Prueba documentada |
| 6 | Agregar verificación de datos a los criterios de aceptación. | Nivel 5 | Karla | Inmediato | Criterios actualizados |
| 7 | Capacitar al personal sobre cómo interpretar la sugerencia y plan de contingencia con otros locales. | Efecto: sin plan al agotarse el producto | Heidi y Darlin | 2 semanas | Guía de una página entregada |

