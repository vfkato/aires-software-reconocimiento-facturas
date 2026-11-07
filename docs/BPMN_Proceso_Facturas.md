# Proceso BPMN — Registro y gestión de facturas

## Objetivo del proceso
Registrar una factura digital desde su carga hasta su almacenamiento y consulta, contemplando la verificación del archivo, el reconocimiento automático, la revisión humana y las validaciones previas al guardado.

## Pool y carriles
- **Pool: Empresa usuaria.** Representa a la organización que utiliza el sistema.
- **Lane: Usuario administrativo.** Carga la factura, revisa los campos reconocidos y corrige los datos observados.
- **Lane: Sistema de reconocimiento.** Comprueba el archivo, reconoce los datos, ejecuta las validaciones, guarda la información y confirma el registro.
- **Lane: Administración / Control.** Consulta el registro confirmado para controles y reportes.

## Recorrido normal
1. **Inicio:** el usuario necesita registrar una factura.
2. **Cargar factura:** selecciona una imagen o un archivo PDF.
3. **Verificar formato y legibilidad:** el sistema controla que el archivo pueda procesarse.
4. **Compuerta exclusiva - ¿Archivo válido?**
   - **No:** el sistema informa el error y solicita otro archivo. Ese intento finaliza sin crear una factura definitiva.
   - **Sí:** el sistema continúa con el reconocimiento.
5. **Reconocer los datos:** se extraen, cuando están disponibles, fecha, CUIT, razón social, número de comprobante, importes, impuestos y total.
6. **Mostrar los datos reconocidos:** el sistema presenta los campos para que el usuario pueda revisarlos.
7. **Revisar los datos reconocidos:** el usuario comprueba la información.
8. **Compuerta exclusiva - ¿Datos completos y correctos?**
   - **No:** el usuario corrige los datos observados y vuelve a revisarlos.
   - **Sí:** el sistema inicia las validaciones.
9. **Validar campos y posibles duplicados:** se comprueban los campos obligatorios y las coincidencias que podrían indicar una factura repetida.
10. **Compuerta exclusiva - ¿Validación aprobada?**
    - **No:** el sistema informa las observaciones; el usuario corrige los datos y vuelve a revisarlos.
    - **Sí:** el sistema guarda la factura y sus detalles.
11. **Confirmar el registro:** el sistema informa que la operación finalizó correctamente.
12. **Consultar el registro:** Administración / Control utiliza la información para controles y reportes.
13. **Fin:** la factura queda registrada y disponible para consulta.

## Cómo leer el diagrama
- Los círculos representan eventos de inicio y fin.
- Los rectángulos redondeados representan actividades realizadas por el usuario o por el sistema.
- Los rombos con una X representan compuertas exclusivas: se elige una sola salida según la respuesta.
- Las flechas continuas representan flujos de secuencia dentro del mismo Pool.
- Las salidas de decisión están identificadas como **Sí** y **No**.

## Tratamiento de excepciones
- **Archivo ilegible, dañado o no admitido:** no se genera un registro definitivo; se solicita un nuevo archivo.
- **Datos incompletos o incorrectos:** el usuario puede corregirlos antes de guardar.
- **Posible duplicado o validación rechazada:** el sistema informa la observación y devuelve el proceso a la corrección.
- **Error de almacenamiento:** la confirmación solo debe mostrarse si el guardado finalizó correctamente.

## Archivos del modelo
- `BPMN_Registro_Facturas_Clarificado.svg`: diagrama visual completo.
- `proceso_facturas_clarificado.bpmn`: modelo en formato BPMN 2.0, con Pools, Lanes, eventos, tareas, compuertas y flujos.
