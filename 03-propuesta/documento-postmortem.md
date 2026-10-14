# Documento post-mortem

Para esta actividad el equipo asume que la solución propuesta presentó un incidente significativo durante su implementación. El incidente es simulado y está construido a partir de los hallazgos de las entrevistas.

## 4. Causa raíz

### 4.1 Análisis de los 5 porqués

| Nivel | Pregunta | Respuesta |
|---|---|---|
| 1 | ¿Por qué se agotó el producto a media mañana? | Porque se compró y preparó para un día de poca actividad. |
| 2 | ¿Por qué se preparó para poca actividad? | Porque la sugerencia diaria indicó actividad baja. |
| 3 | ¿Por qué la sugerencia indicó actividad baja? | Porque el calendario no tenía las fechas de exámenes y el historial venía de días con la universidad cerrada o virtual. |
| 4 | ¿Por qué el calendario no tenía esas fechas? | Porque la carga era manual y no había un responsable ni una fecha de revisión definida. |
| 5 | ¿Por qué no había responsable ni revisión? | Porque al priorizar la fecha de entrega, los criterios de aceptación no incluyeron verificar los datos del calendario ni probar con una semana de exámenes real. |

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

