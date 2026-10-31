# Indicadores de control

| Indicador | Fórmula / criterio | Estándar propuesto | Frecuencia |
|---|---|---|---|
| Precisión de reconocimiento | Campos principales correctos / campos evaluados × 100 | ≥ 90 % en facturas legibles | Cada ciclo de pruebas |
| Validación previa al guardado | Facturas revisadas y validadas / facturas almacenadas × 100 | 100 % | Cada versión |
| Integridad de registros | Registros sin pérdida ni inconsistencias / registros probados × 100 | 100 % en aceptación | Antes de implementar |
| Errores críticos abiertos | Conteo de defectos críticos pendientes | 0 antes de implementar | Semanal y al liberar |
| Volumen de procesamiento | Cantidad de facturas procesadas correctamente | ≥ 500 en validación final prevista | Cierre de validación |
| Cumplimiento del cronograma | Actividades en fecha / actividades planificadas × 100 | Seguimiento del plan de 10 semanas | Semanal |
| Trazabilidad | Commits descriptivos y cambios revisados por PR | Ramas secundarias y al menos 1 PR revisado | Cada integración |

Las cifras son metas de planificación provenientes de la Entrega 2 o estándares propuestos; no son resultados ya medidos.

## Acciones ante desvíos
- Precisión inferior al 90 %: revisar calidad de imágenes, campos problemáticos y casos de prueba.
- Registros incompletos o duplicados: revisar validaciones y bloquear la confirmación hasta resolver.
- Errores críticos abiertos: postergar la implementación y priorizar su corrección.
- Retrasos: revisar dependencias, estimaciones y prioridades del backlog.
