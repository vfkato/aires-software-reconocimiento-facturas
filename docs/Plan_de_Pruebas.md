# Plan de pruebas funcionales — Registro de facturas

## Objetivo
Verificar que el sistema reciba facturas, reconozca sus datos, permita la revisión, valide la información y conserve correctamente los registros confirmados.

## Casos de prueba

| ID | Escenario | Resultado esperado |
|---|---|---|
| CP-01 | Cargar un PDF legible y válido | El sistema acepta el archivo y comienza el reconocimiento. |
| CP-02 | Cargar una imagen ilegible o un archivo dañado | El sistema informa el error y no crea una factura definitiva. |
| CP-03 | Reconocer una factura con campos principales legibles | Se muestran los campos extraídos para revisión del usuario. |
| CP-04 | El reconocimiento devuelve un dato incorrecto | El usuario puede corregirlo antes de confirmar. |
| CP-05 | Falta un campo obligatorio | La validación informa la observación y bloquea el guardado definitivo. |
| CP-06 | Se intenta cargar una factura posiblemente duplicada | El sistema advierte la coincidencia para que el usuario la revise. |
| CP-07 | Todos los datos están completos y validados | El sistema guarda la factura y sus detalles y confirma la operación. |
| CP-08 | Se produce un error durante el almacenamiento | El sistema informa que el registro no fue confirmado. |

## Criterios de aceptación
- Ningún archivo inválido debe quedar registrado como factura confirmada.
- La persona usuaria debe poder revisar y corregir los datos reconocidos.
- El 100 % de las facturas guardadas debe haber pasado por validación.
- La prueba de reconocimiento debe alcanzar como meta al menos un 90 % de campos principales correctos en documentos legibles.
- No deben quedar errores críticos abiertos antes de la implementación.

**Nota:** estos son casos diseñados para la etapa de verificación. Los resultados deben registrarse al ejecutar las pruebas; no se declaran como pruebas ya realizadas.
