# Proceso BPMN — Registro y gestión de facturas

## Pool
**Empresa usuaria**

## Lanes
- **Usuario administrativo:** carga la factura, revisa los datos reconocidos y corrige los campos observados.
- **Sistema de reconocimiento:** verifica el archivo, extrae los datos, ejecuta validaciones, guarda y confirma.
- **Administración / Control:** consulta los registros para controles y reportes.

## Flujo principal
1. Evento de inicio: necesidad de registrar una factura.
2. El usuario carga una imagen o un PDF.
3. El sistema verifica el formato y la legibilidad.
4. Compuerta exclusiva: **¿el archivo es válido?**
   - **No:** informar el error, solicitar otro archivo y finalizar el intento.
   - **Sí:** continuar con el reconocimiento.
5. El sistema extrae fecha, CUIT, razón social, número de factura, importes, impuestos y total, cuando estén disponibles.
6. El sistema muestra los datos reconocidos.
7. El usuario revisa y corrige los campos.
8. Compuerta exclusiva: **¿los datos están completos y son correctos?**
   - **No:** volver a la revisión y corrección.
   - **Sí:** continuar.
9. El sistema valida campos obligatorios y controla posibles duplicados.
10. Compuerta exclusiva: **¿la validación fue aprobada?**
    - **No:** informar observaciones y devolver al usuario para corregir.
    - **Sí:** guardar la factura y sus detalles.
11. El sistema confirma el registro.
12. Administración consulta el registro para controles y reportes.
13. Evento de fin: factura registrada y disponible.

## Excepciones contempladas
- Archivo dañado, formato no admitido o imagen ilegible: no se crea un registro definitivo.
- Datos incompletos o reconocidos incorrectamente: se permite la corrección antes de guardar.
- Posible factura duplicada: se emite una advertencia para revisión.
- Error durante el guardado: el sistema informa que la operación no se confirmó.

## Criterios BPMN
Las compuertas son exclusivas porque en cada validación se selecciona un único camino. Los flujos de secuencia conectan elementos dentro del Pool de la empresa. Si en otra versión se contrata un servicio externo de OCR, su interacción deberá modelarse en otro Pool mediante flujos de mensaje.

El archivo `proceso_facturas.bpmn` contiene el modelo BPMN 2.0 para abrirlo en una herramienta compatible.
