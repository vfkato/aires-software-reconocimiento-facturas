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
- `docs/BPMN_Proceso_Facturas.md`: descripción del proceso, carriles, decisiones y excepciones.
- `docs/BPMN_Vista_1_Carga_Reconocimiento.svg`: vista gráfica de carga y reconocimiento.
- `docs/BPMN_Vista_2_Revision_Validacion.svg`: vista gráfica de revisión, validación y almacenamiento.
- `docs/proceso_facturas_clarificado.bpmn`: modelo BPMN 2.0 fuente.
- `docs/Backlog_Historias_de_Usuario.csv`: tres historias de usuario y criterios de aceptación.
- `docs/Indicadores_de_Control.md`: indicadores, fórmulas, metas y frecuencia.
- `docs/Modelo_Datos.md`: entidades y relaciones iniciales.
- `docs/Plan_de_Pruebas.md`: escenarios de prueba funcional propuestos.
- `docs/Seguimiento_Historias.md`: criterio de avance documental en GitHub Projects.
- `docs/Respuesta_Observaciones_Docentes.md`: respuesta a las observaciones de la Entrega 4.

## Control de versiones
- `main`: versión integrada.
- `feature/bpmn-facturas` y `feature/backlog-control`: ramas utilizadas en la primera integración.
- `fix/bpmn-claridad-y-seguimiento`: rama con las correcciones posteriores a la devolución docente.

El [Pull Request #1](https://github.com/vfkato/aires-software-reconocimiento-facturas/pull/1) integró la primera versión documental. El [Pull Request #5](https://github.com/vfkato/aires-software-reconocimiento-facturas/pull/5) presenta las correcciones y permanece abierto para una revisión real de otra persona.

## Tablero ágil
Tablero público de [Aires Software — Gestión de Facturas](https://github.com/users/vfkato/projects/2). Contiene HU-01, HU-02 y HU-03 y utiliza los estados Por Hacer, En Progreso y Listo. Los estados describen el avance de análisis y documentación del TPI, no una implementación de software finalizada.

## Declaración de uso de Inteligencia Artificial
Se utilizó ChatGPT como apoyo para organizar la documentación, proponer el flujo BPMN, redactar historias de usuario y definir indicadores. El contenido fue contrastado con las entregas anteriores y con las observaciones docentes. Se reorganizó el BPMN en dos vistas para facilitar su lectura, se revisó la correspondencia entre historias y proceso y se dejó el Pull Request #5 abierto para una revisión externa real. La responsabilidad de comprender y defender las decisiones en el coloquio corresponde al estudiante.
