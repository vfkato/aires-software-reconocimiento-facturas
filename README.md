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
- `docs/BPMN_Proceso_Facturas.md`: participantes, carriles, flujo y excepciones del proceso.
- `docs/Backlog_Historias_de_Usuario.csv`: historias de usuario y criterios de aceptación.
- `docs/Indicadores_de_Control.md`: indicadores, fórmulas, metas y frecuencia de revisión.
- `docs/Modelo_Datos.md`: entidades y relaciones definidas inicialmente en la Entrega 3.

## Organización del repositorio
- `main`: versión estable.
- `feature/bpmn-facturas`: documentación del proceso BPMN.
- `feature/backlog-control`: historias de usuario e indicadores.

Los cambios se integraron a `main` mediante el [Pull Request #1](https://github.com/vfkato/aires-software-reconocimiento-facturas/pull/1).

## Tablero ágil
Se registraron las tres historias de usuario como Issues #2, #3 y #4. El tablero de GitHub Projects debe crearse y asociar esas historias con los estados **Por Hacer**, **En Progreso** y **Listo**.

## Declaración de uso de IA
Se utilizó ChatGPT como apoyo para organizar la documentación, proponer el flujo BPMN, redactar historias de usuario y definir indicadores. El contenido fue contrastado con las entregas anteriores y ajustado para mantener la continuidad del caso. Las decisiones finales y la verificación de coherencia corresponden al estudiante.

## Estado de publicación
Este repositorio contiene documentación académica del TPI. Las ramas, el tablero y la revisión por Pull Request se registrarán a medida que se completen efectivamente en GitHub.
