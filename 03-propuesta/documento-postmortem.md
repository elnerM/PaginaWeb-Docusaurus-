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
