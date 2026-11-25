# PRD — farmacia-san-martin

## 1. Problema
Las farmacias pequeñas que gestionan inventario y ventas mediante cuadernos o planillas dispersas sufren descuadres de caja, agotamiento inesperado de medicamentos frecuentes y pérdidas por productos vencidos o próximos a caducar.

## 2. Usuarios
- **Atención en mostrador / Farmacéutico:** Consulta precios, existencias y condición de récipe, y registra ventas.
- **Encargado / Administrador:** Registra compras y lotes con fecha de vencimiento, ajusta precios y revisa el cierre diario.

## 3. Alcance (MVP)
- **Incluye:** Catálogo de productos, control de lotes y fechas de vencimiento, ventas en mostrador con descuento automático de stock, alertas de stock mínimo y vencimiento, y resumen diario de caja.
- **No incluye (en esta etapa):** Facturación fiscal electrónica, múltiples sucursales ni automatización de pedidos con droguerías.

## 4. Requisitos
- **Funcionales:** Crear/editar/buscar productos, registrar lotes y vencimientos, validar disponibilidad antes de vender, consultar alertas y generar cierre diario.
- **No funcionales:** Consultas rápidas en entorno local, trazabilidad de entradas y salidas, comprobaciones de CI en verde y código modular explicable.

## 5. Funcionalidades y carpetas en `src/`
- **Catálogo de medicamentos y misceláneos:** `src/catalogo/`
- **Control de lotes, vencimientos y existencias:** `src/lotes-inventario/`
- **Ventas y despacho en mostrador:** `src/despacho-ventas/`
- **Usuarios y roles:** `src/usuarios/`
- **Alertas y cierre de caja:** `src/cierre-caja/`