# Modelo de datos inicial — Sistema de reconocimiento y gestión de facturas

Este modelo continúa el diccionario de datos de la Entrega 3. Se enumeran las entidades principales y sus relaciones funcionales.

## Entidades
- **Proveedor:** identifica al emisor de la factura. Incluye identificador, CUIT, razón social y datos de contacto.
- **Factura:** registra los datos generales del documento, como proveedor, tipo y número, fecha, importes, impuestos y total.
- **DetalleFactura:** almacena los conceptos o renglones que componen una factura y se vincula con una factura.
- **Usuario:** identifica a la persona que utiliza el sistema y revisa los datos reconocidos.
- **Revision:** registra la revisión de una factura, el usuario responsable, la fecha, si requirió corrección y las observaciones.

## Relaciones
- Un proveedor puede emitir muchas facturas; cada factura se asocia a un proveedor mediante `id_proveedor`.
- Una factura puede contener varios detalles; cada detalle se vincula mediante `id_factura`.
- Una factura puede tener una o más revisiones; cada revisión identifica la factura y el usuario responsable.
- Un usuario puede revisar muchas facturas; `id_usuario` identifica quién realizó cada revisión.

## Controles de integridad propuestos
- Validar el formato del CUIT y los campos obligatorios.
- Controlar importes y consistencia entre subtotal, impuestos y total, según las reglas de cada comprobante.
- Advertir posibles comprobantes duplicados.
- Verificar que las referencias apunten a registros existentes.
