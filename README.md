# Naturema CR · La Matería de Escazú — demo del sistema de pedidos

Demo navegable (una sola página, sin backend) del **sistema de pedidos** para
**Naturema CR / La Matería de Escazú**, distribuidores de yerba mate, mates y
bombillas en Costa Rica desde 2017 (tienda física en Escazú, San José).

La web actual no tiene forma de pedir, así que los pedidos se pierden entre el
chat de WhatsApp y la tienda. Este sistema los centraliza y les hace seguimiento.

## Qué muestra

- **Entrada**: botón «Entrar al sistema» y «Ver el recorrido guiado».
- **Panel del día**: pedidos nuevos sin confirmar, en preparación, listos para
  enviar, entregados hoy, cobros por verificar (SINPE/transferencia) y mensajes
  por responder.
- **Bandeja de pedidos**: pedidos que entraron **desde la web, desde WhatsApp y
  en tienda física**, con estado (nuevo · confirmado · en preparación · enviado ·
  entregado / cancelado), canal de origen, cliente, artículos con cantidad y
  total en colones, y acciones para avanzar de estado. Al abrir un pedido:
  detalle completo, historial de estados y el botón **«enviar comprobante/guía
  por WhatsApp»** con la maqueta del mensaje al número real.
- **Catálogo e inventario**: productos por categoría (mates, bombillas, yerbas,
  termos, accesorios), precio en colones, stock y aviso automático de **stock
  bajo**; el stock se edita desde la pantalla.
- **Clientes**: ficha con historial de compras, zona, teléfono de ejemplo y notas.
- **Envíos**: pedidos por entregar por zona (San José, Escazú, Heredia, Cartago
  y fuera del GAM), tipo (retiro en tienda / mensajería) y estado de la guía.
- **Caja del día**: ventas cobradas, por SINPE Móvil, por transferencia y en
  efectivo contra entrega, más el total del día. Sin números de cuenta reales.
- **Informes**: gráficos propios (SVG/CSS) de ventas por día de la última semana,
  productos más vendidos, ventas por canal (web vs WhatsApp vs tienda) y ticket
  promedio.
- **Recorrido guiado**: tour de **8 pasos** sobre la interfaz, con Atrás /
  Siguiente / Salir, contador «Paso N de 8», teclado (← → Esc) y modo automático.

## Datos

Todos los datos son **de ejemplo** (clientes, zonas y montos en colones). Los
productos y precios de referencia son los del negocio. No se envía ni se guarda
nada: la app es estática y el envío por WhatsApp es solo una maqueta.

## Ejecutar

```bash
docker build -t sistema-naturemacr .
docker run -p 8080:80 sistema-naturemacr
```

---

Demo de referencia hecho por **Nocodeveloper**. Los datos son de ejemplo.
