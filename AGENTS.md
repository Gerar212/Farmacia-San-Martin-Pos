# AGENTS.md — farmacia-san-martin

## Descripción del producto
`farmacia-san-martin` es una aplicación de punto de venta, inventario y control operativo para una farmacia pequeña. Facilita el registro de ventas en mostrador, el control de lotes y fechas de vencimiento, la validación de existencias disponibles y el cierre diario de caja.

## Arquitectura y convenciones
- **Estructura (`src/`):** Organización modular por dominio (`src/catalogo/`, `src/lotes-inventario/`, `src/despacho-ventas/`, `src/usuarios/`, `src/cierre-caja/`).
- **Entorno y base de datos:** Node.js 24, Docker Compose (`docker-compose.yml`), migraciones con `npm run migrate`, datos de prueba con `npm run seed` y ejecución local con `npm run dev`.
- **Reglas de negocio:**
  - Registrar lote y fecha de vencimiento en cada entrada de mercancía.
  - Impedir ventas cuando la cantidad pedida supere el stock disponible.
  - Diferenciar medicamentos de venta libre y productos que requieren récipe médico.
- **Reglas del curso:**
  - Todo cambio pasa por un Pull Request; nada se sube directo a la rama principal.
  - Declarar el uso de IA en la bitácora de cada PR y escribir estructuras de datos y algoritmos a mano.
  - Todo código debe poder explicarse con claridad.
  