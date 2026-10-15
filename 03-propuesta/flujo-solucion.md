# Flujo de la solución propuesta

## Qué es la solución

Una aplicación web sencilla, pensada para usarse desde un celular o tablet, que ayuda a los kioscos a decidir cuánto preparar, registrar sus ventas y controlar la frescura de las verduras, sin cambiar la forma en que ya atienden. El nombre del sistema es provisional: Eficiencia mercantil

## Fase 1: funciones incluidas

| Módulo | Qué hace | Requisitos |
|---|---|---|
| Registro de ventas | Anota con pocos toques lo vendido en el día | RQ-01, RQ-14 |
| Resumen de ventas | Muestra días y productos con más y menos venta | RQ-02 |
| Calendario y avisos | Muestra exámenes, clases, vacaciones y avisos de cierre | RQ-03, RQ-05 |
| Sugerencia diaria | Recomienda cuánto preparar según historial y calendario | RQ-04, RQ-13 |
| Semáforo de frescura | Indica con colores qué verdura usar o sacar | RQ-12 |

## Fase 2: funciones pendientes de evaluar

Pedidos anticipados por QR (RQ-08, RQ-09), comanda digital (RQ-10), alerta entre locales (RQ-11), control de inventario con alerta mínima (RQ-06, RQ-07).

## Pasos para dibujar el diagrama de flujo

1. Inicio del día: la persona abre la aplicación.
2. La aplicación muestra la sugerencia diaria (según historial y calendario).
3. Se compra y prepara según la sugerencia.
4. Al preparar cada verdura, se toca el botón correspondiente y el semáforo empieza a contar.
5. Durante el día, el semáforo muestra verde, amarillo o rojo.
6. Decisión: ¿la verdura está en rojo? Si sí, se retira; si no, se usa.
7. Durante el día se anotan las ventas con uno o dos toques.
8. Al cierre se confirma el registro del día.
9. El sistema actualiza el historial y la sugerencia del día siguiente.
10. Decisión: ¿hay aviso de cierre o fecha de examen nueva? Si sí, se registra en el calendario.

> 🖼️ **[ESPACIO PARA DIAGRAMA DE FLUJO]** 

>
> `![Diagrama de flujo de la solución propuesta, desde la sugerencia diaria hasta la actualización del historial.]` <img width="777" height="5070" alt="image" src="https://github.com/user-attachments/assets/dca6f8ce-bcae-44d9-8e9b-056d53502ea9" />

> **Descripción:** Diagrama de flujo de la solución propuesta, desde la sugerencia diaria hasta la actualización del historial.
>
> **Justificación:** Muestra qué hará el sistema y cómo se conecta con las decisiones de la junta (fase 1).
