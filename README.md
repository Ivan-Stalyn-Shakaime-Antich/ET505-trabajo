# Planificador Kit Rural - Ivan Stalyn - ET505 S7

## Autor y propósito

Ivan Stalyn- Sistema Planificador Kit Rural. Actividad educativa: organizar pedido de útiles para taller rural en Trujillo con presupuesto de S/200.00. Simula cálculo de total y saldo sin compras reales.

## Ejecutar

Descargue y conserve juntos index.html, styles.css y app.js. Abra index.html en Chrome o Edge. Edite app.js, guarde Ctrl+S y recargue Ctrl+R. No necesita Node ni internet.

## Responsabilidades

- index.html: estructura, entradas y presupuesto visible S/200.00.
- styles.css: apariencia y distinción error rojo #991b1b / éxito verde.
- app.js: limites.presupuestoCentimos:20000, calcularTotal sin acceso a pantalla, validarPedido con reglas, reutilización en comprobar.

## Pendientes obligatorios

TODO 1: return pedido.cantidad * Math.round(pedido.precio * 100); convierte precio a céntimos enteros y multiplica por cantidad. Ej: S/5*100=500 céntimos *10 = 5000 = S/50.00.
TODO 2: if (total > limites.presupuestoCentimos) return "El total supera el presupuesto."; return ""; devuelve vacío si cumple.
TODO 3: const error = validarPedido(pedido); reutiliza validación en ambos botones, conserva ficha anterior.

## Mi personalización

Nombre: Planificador Kit Rural -Ivan Stalyn. Actividad: taller rural. Material ejemplo: Cuadernos A4 para zona rural. Presupuesto: S/200.00 distinto a S/150, entre 50 y 300, múltiplo de 10. Justificación: 20 alumnos * kit S/10. Elegí S/200 para cubrir 20 kits básicos. Cambié limites.presupuestoCentimos de 15000 a 20000 y texto visible S/ 200.00. Mantengo maxCantidad 30 y maxPrecio 50.

## Pruebas

1. Válido: Cuadernos A4, 10, 5.00 -> total S/50.00 saldo S/150.00. Mensaje verde Pedido válido / Simulación confirmada.
2. Inválido: material vacío o cantidad 2.5 -> error rojo: "Escriba un material de al menos 3 caracteres." / "Cantidad: entero entre 1 y 30." probado en Comprobar y Confirmar.
3. Límite: 10 unidades a S/20.00 (presupuesto/10) -> total S/200.00 saldo S/0.00 aceptado.
4. Exceso: 10 unidades a S/20.01 -> total S/200.10 exceso S/0.10 error rojo "El total supera el presupuesto." Detalle muestra Total intentado, Presupuesto y Exceso.
5. Conservación: Confirmo válido 10x5, luego intento inválido vacío -> ficha conserva S/50.00 y mensaje indica "La ficha de abajo es el último pedido válido. Se conserva sin cambios." Luego Limpiar borra ficha y muestra "Todavía no ha confirmado un pedido."

## Mi aporte y ayuda recibida

Corregí 3 TODO siguiendo guía 15/10/2026. Detecté que mensaje error debe conservar ficha. Ayuda: guía docente ET505, consulta IA para redondeo Math.round. Código propio, pruebas reales en Chrome local y GitHub Pages.

## Repositorio individual y GitHub Pages

Repositorio: https://github.com/TUUSUARIO/et505-planificador
Sitio: https://TUUSUARIO.github.io/et505-planificador/
Pasos: New repository public et505-planificador, Upload 4 archivos en raíz, Commit, Settings > Pages > Deploy from branch > main /(root) > Save. Esperar Actions.

## Entrega y evaluación

PDF único con capturas de código, pruebas 5 casos, organización, personalización y aporte. Plazo 17/10/2026 20:00 Perú.

## Mensajes visibles

Error rojo: "ERROR: Pedido no válido." al comprobar y "ERROR: No se pudo confirmar el pedido." al confirmar + motivo en rojo + estado de ficha. Éxito verde. Ya no aparece PENDIENTE TODO.
