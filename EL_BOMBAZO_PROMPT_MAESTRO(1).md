# PROMPT MAESTRO — EL BOMBAZO by Yaxiel

Actúa como un equipo senior de producto, arquitectura, UX, seguridad, backend y frontend. Construye una plataforma comercial PWA escalable para EL BOMBAZO by Yaxiel, negocio de zapatos, chancletas, telas y otros artículos que vende exclusivamente a domicilio.

## Reglas no negociables

1. Arquitectura modular, escalable y mantenible.
2. Ningún archivo de código fuente puede superar 300 líneas. Si se acerca al límite, dividir por responsabilidad en módulos pequeños.
3. TypeScript estricto, componentes reutilizables, validación de entradas, estados de carga/error/vacío y accesibilidad móvil.
4. No simular operaciones reales: diferenciar claramente demo y producción.
5. No almacenar secretos en el cliente. Proteger cada recurso con autorización server-side y RLS.
6. Crear pruebas para cálculos de dinero, permisos, estados de pedido, inventario y comisiones.

## Identidad del negocio

Nombre: EL BOMBAZO by Yaxiel. Moneda visible: MN. Venta exclusivamente a domicilio. Dentro de Circunvalación, domicilio de 300 MN. Fuera de la Rotonda, el cliente debe consultar al administrador antes de confirmar. Transferencias con recargo inicial del 15%, configurable. Efectivo y transferencia como métodos admitidos. Comisiones administradas exclusivamente por el propietario: 1.000 MN por par de zapatos; 500 MN por tela, chancletas u otros artículos, sujeto a unidad y regla de liquidación confirmadas por el propietario.

## Producto

Desarrolla storefront móvil-first con catálogo, búsqueda, filtros, variantes, fotos, carrito, dirección, cotización de domicilio, checkout, confirmación, estado del pedido, favoritos, promociones, botón WhatsApp y experiencia instalable PWA. Diseña área privada diferenciada por perfil.

## Panel administrativo completo

Implementa dashboard con métricas y alertas; gestión de pedidos y estados; CRUD de productos, categorías, variantes e imágenes; movimientos de inventario; clientes y direcciones; zonas, cotizaciones, asignación de repartidores y prueba de entrega; pagos y verificación de transferencias; reglas y liquidaciones de comisiones; equipo y permisos; promociones/cupones; informes exportables; configuración comercial; auditoría y registro de actividad.

## Roles

- Owner: acceso total, único que crea/modifica reglas de comisión y roles de máximo privilegio.
- Admin: operación diaria y configuración permitida.
- Seller: ventas atribuidas, catálogo permitido y seguimiento de sus pedidos.
- Courier: entregas asignadas y datos mínimos necesarios.
- Customer: catálogo, perfil y pedidos propios.

## Arquitectura técnica sugerida

Next.js + TypeScript + React; Supabase Auth, PostgreSQL, Storage y RLS; despliegue Cloudflare Pages (Next.js Static HTML Export); PWA con manifest, service worker y estrategia offline segura. Mantener dominio separado de UI. Crear casos de uso server-side y RPC transaccionales para crear pedido, reservar inventario, verificar pago, asignar entrega y liquidar comisión. Dinero en enteros de unidad menor; el servidor recalcula siempre los totales.

## Diseño

Diseño comercial moderno, energético, confiable y muy claro. Adaptado a móvil Android primero, tablet y escritorio. Navegación sencilla, cards limpias, imágenes grandes, tipografía legible, llamadas a acción claras y estados visuales consistentes. Mantener identidad del logo proporcionado; no inventar tarifas o condiciones adicionales.

## Entrega por etapas

A. Auditoría del repositorio, plan y arquitectura. B. Diseño y componentes. C. Catálogo y carrito. D. Backend, auth y RLS. E. Pedidos y pagos. F. Logística. G. Comisiones. H. Panel e informes. I. PWA, pruebas, accesibilidad, rendimiento y despliegue.

En cada etapa: editar archivos reales, ejecutar lint, typecheck, pruebas y build; verificar límite 300 líneas; actualizar documentación y lista de pendientes. No declarar una integración completada sin probarla en el entorno real. No desplegar a producción ni ejecutar cambios destructivos sin autorización expresa.
