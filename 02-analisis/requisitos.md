# Requisitos identificados

Los requisitos se obtuvieron a partir de las entrevistas a los negocios Los Chatios (K y D) y Los Chatos (B y E). 
Cada requisito tiene un identificador único y una descripción en lenguaje sencillo.

- **Prioridad:** Alta, Media o Baja según la urgencia para el negocio.
- **Fase1:** es lo que se construye primero
- **Fase2:** es lo que se evalúa después (ver `03-propuesta/acuerdos-tradeoffs.md`).

| ID | Nombre | Descripción | Origen | Prioridad | Fase | Evidencia en la entrevista |
|---|---|---|---|---|---|---|
| RQ-01 | Registro diario de ventas | El negocio debe poder anotar cada día cuántos productos vendió (por ejemplo Shucos), cuáles se pidieron más y cuánto se vendió en total. | K y D | Alta | 1 | Las ventas se llevan solo de memoria. |
| RQ-02 | Resumen de ventas por día y semana | El sistema debe mostrar de forma sencilla en qué días se vende más o menos y qué productos son los más pedidos. | K y D | Alta | 1 | Quieren poder comparar semanas; hoy no hay datos para decidir. |
| RQ-03 | Calendario de actividad universitaria | El sistema debe mostrar fechas de exámenes, semanas de clases y vacaciones, para saber cuándo llegarán más o menos estudiantes. | K y D | Alta | 1 | Preguntan a licenciados cuándo habrá exámenes; existe una plataforma de la facultad con esas fechas. |
| RQ-04 | Sugerencia diaria de cuánto preparar | El sistema debe dar una recomendación sencilla de cuánto producto preparar según el historial de ventas y el calendario, como referencia y no como cifra exacta. | K y D | Alta | 1 | Antes sabían la cantidad de producto por la cantidad de estudiantes; hoy preparan solo lo que consideran. |
| RQ-05 | Registro de avisos de cierre o acceso restringido | El negocio debe poder anotar avisos de cierre o cambios de acceso a la universidad para tenerlos en cuenta al preparar. | K y D | Media | 1 | Les han impedido el ingreso sin aviso previo. |
| RQ-06 | Control básico de inventario | El negocio debe poder registrar al inicio del día cuánto producto tiene y actualizar solo los productos principales (panes, aguacate, bebidas). | K y D / B y E | Media | 2 | El control es de memoria; cuando algo se acaba hay que conseguir más rápido. |
| RQ-07 | Alerta de cantidad mínima | El sistema debe avisar cuando un producto llegue a una cantidad mínima definida por el negocio. | K y D / B y E | Media | 2 | Se quedan sin producto a media jornada. |
| RQ-08 | Pedidos anticipados con hora de recogida | Los estudiantes deben poder escoger su pedido antes de llegar (por ejemplo con un código QR) y elegir una hora aproximada de recogida. | K y D | Media | 2 | Los estudiantes se desesperan en la fila; el negocio busca atender más rápido para tener más clientes. |
| RQ-09 | Pago anticipado opcional | Quien lo prefiera debe poder pagar por adelantado con una opción digital; el pago en el puesto debe seguir disponible. | K y D | Baja | 2 | Propuesta del equipo para agilizar la atención (no fue mencionado directamente en la entrevista). |
| RQ-10 | Comando digital en mostrador | Quien atiende debe poder registrar el pedido con muy pocos toques (tipo de pan y si es para llevar o para comer ahí) y enviarlo a preparación. | B y E | Media | 2 | En horas pico a veces olvidan lo que pidió el cliente y deben volver a preguntar. |
| RQ-11 | Alerta de insumos a otros locales | Debe existir un botón para avisar a los otros locales cuando un ingrediente está por terminarse, sin hacer llamadas. | B y E | Media | 2 | Cuando se acaba un producto se llaman entre locales para apoyarse. |
| RQ-12 | Control de frescura de verduras | El sistema debe indicar con colores (verde, amarillo, rojo) si una verdura está fresca, debe usarse pronto o ya no se debe servir. | B y E | Alta | 1 | Tomate y cebolla se pasan rápido y se revisan uno por uno. |
| RQ-13 | Lista de preparación del día siguiente | El sistema debe enviar una lista de qué preparar, cuánto y en qué orden, basada en lo más vendido. | B y E | Media | 1 | La preparación antes de abrir (picar, lavar, cocer, ordenar, limpiar) consume mucho tiempo. |
| RQ-14 | Uso muy simple (pocos toques) | Registrar una venta o una preparación debe tomar uno o dos toques, sin escribir texto largo. | K y D / B y E | Alta | 1 | La atención es rápida; un sistema lento les quitaría tiempo. |
| RQ-15 | Uso en celular o tablet | La solución debe funcionar en un teléfono o tablet que ya tengan o sea económica, sin equipos grandes en el mostrador. | K y D / B y E | Alta | 1 | B y E prefiere no tener computadora ni sistema complicado. |
| RQ-16 | Aprendizaje rápido | El personal sin conocimientos técnicos debe poder aprender a usarla en pocos minutos. | K y D / B y E | Alta | 1 | No están contratando personal nuevo y el equipo no es técnico. |
| RQ-17 | Atención tradicional se mantiene | Los clientes que prefieran pedir en el puesto deben poder seguir haciéndolo como siempre. | K y D | Media | 1 | Se desea agilizar sin cambiar la forma de trabajo actual. |

## Restricciones del negocio detectadas

- Las ventas bajaron cerca de 70% por el cierre de la universidad, y el alquiler del local se paga por todo el año.
- No se está contratando personal por ahora.
- El personal no desea sistemas que quiten tiempo de atención.
- La compra de verduras se hace todos los días muy temprano en la terminal.

## Trazabilidad con las propuestas individuales

| Integrante | Propuesta | Requisitos relacionados |
|---|---|---|
| Karla | Planificación y alertas por calendario | RQ-03, RQ-04, RQ-05 |
| Heidi | Pedidos anticipados por QR | RQ-08, RQ-09, RQ-17 |
| Ilse | Control de inventario con alerta mínima | RQ-06, RQ-07 |
| Elner | Comanda digital y alerta entre locales | RQ-10, RQ-11 |
| Darlin | Registro digital de ventas diarias | RQ-01, RQ-02 |
| Brandon | Semáforo de frescura y lista de preparación | RQ-12, RQ-13 |
| Apen | [[PENDIENTE: propuesta de Apen]] | [[PENDIENTE]] |
