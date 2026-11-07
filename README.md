# Aires Software — Sistema de Reconocimiento y Gestión de Facturas

**Trabajo Práctico Integrador y Progresivo (TPI) — Organización Empresarial**  
**Alumno:** Aires Tobias  
**Carrera:** Tecnicatura Universitaria en Programación a Distancia (TUP AD)  
**Institución:** Universidad Tecnológica Nacional

## Descripción
Proyecto académico de una aplicación que recibe facturas como imágenes o archivos PDF, reconoce sus datos principales, permite la revisión y corrección por parte del usuario, valida la información y la almacena para consultas y controles administrativos.

## Alcance funcional
1. Cargar una factura en imagen o PDF.
2. Verificar que el archivo sea válido y legible.
3. Reconocer fecha, CUIT, razón social, número de factura, importes, impuestos y total, según disponibilidad.
4. Mostrar los datos reconocidos para revisión y corrección humana.
5. Validar campos obligatorios y advertir posibles duplicados.
6. Guardar la factura y sus detalles.
7. Confirmar el registro y permitir su consulta.

## Documentación
- `docs/BPMN_Proceso_Facturas.md`: recorrido normal, carriles y excepciones.
- `docs/BPMN_Registro_Facturas_Clarificado.svg`: diagrama completo revisado.
- `docs/Backlog_Historias_de_Usuario.csv`: historias de usuario y criterios de aceptación.
- `docs/Seguimiento_Historias.md`: criterio de seguimiento de estados del tablero.
- `docs/Indicadores_de_Control.md`: indicadores, fórmulas, metas y frecuencia.
- `docs/Modelo_Datos.md`: entidades y relaciones definidas inicialmente en la Entrega 3.
- `docs/Plan_de_Pruebas.md`: escenarios de prueba funcional.
- `docs/Respuesta_Observaciones_Docentes.md`: correcciones preparadas a partir de la devolución de la Entrega 4.

## Organización del repositorio
- `main`: versión estable.
- `feature/bpmn-facturas`: primera documentación del proceso BPMN.
- `feature/backlog-control`: historias de usuario, indicadores y plan de pruebas.
- `fix/bpmn-claridad-y-seguimiento`: correcciones solicitadas por la devolución docente.

El [Pull Request #1](https://github.com/vfkato/aires-software-reconocimiento-facturas/pull/1) integró la documentación inicial a `main`.  
El [Pull Request #5](https://github.com/vfkato/aires-software-reconocimiento-facturas/pull/5) presenta la corrección del BPMN y del seguimiento para una **revisión de pares pendiente**. No debe considerarse revisado hasta que otra persona deje su revisión registrada en GitHub.

## Tablero ágil
Se registraron las tres historias de usuario como Issues #2, #3 y #4. El tablero público [Aires Software — Gestión de Facturas | TPI UTN](https://github.com/users/vfkato/projects/2) utiliza los estados **Por Hacer**, **En Progreso** y **Listo**.

Los estados describen el avance de análisis y documentación de este TPI. No representan funcionalidades ya implementadas en una aplicación de producción.

## Declaración de uso de IA
Se utilizó ChatGPT como apoyo para ordenar la estructura del informe, proponer una primera secuencia BPMN, redactar historias de usuario y proponer indicadores. Los pedidos se orientaron a organizar los conceptos de la materia y mantener la continuidad del caso Aires Software.

La revisión humana consistió en contrastar cada propuesta con las entregas anteriores y con la devolución docente. Se corrigieron el recorrido del proceso, las compuertas, las excepciones, las conexiones entre carriles y la explicación de los estados del tablero. También se verificaron los enlaces reales de GitHub. La IA se usó como herramienta de apoyo y no como reemplazo de las decisiones ni de la comprensión del estudiante.

## Estado de publicación
La documentación inicial está integrada en `main`. La actualización del BPMN y del seguimiento se presenta en el Pull Request #5 y queda pendiente de revisión real por un par antes de integrarse.
