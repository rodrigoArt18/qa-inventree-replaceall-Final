# Aseguramiento de la Calidad de Software — Proyecto ReplaceAll (InvenTree)

Repositorio de gestión de pruebas, trazabilidad y control de incidentes del sistema de inventario **InvenTree** (`localhost:8003`) para **ReplaceAll**, estructurado bajo las normas **ISO/IEC/IEEE 29119-3**, **ISO/IEC/IEEE 25010** y **TMMi Nivel 2**.

---

## 4.6 Asignación de Roles

Para garantizar una correcta separación de funciones, la independencia en las revisiones cruzadas y el cumplimiento del cronograma de 11 semanas, el equipo del proyecto ReplaceAll organiza sus responsabilidades articulando los roles de prueba con los procesos y artefactos documentales de la norma ISO/IEC/IEEE 29119-3:

### Integrante: Rodrigo Arturo Paredes Santa Cruz
**Gerente de Pruebas / Test Manager (Líder del Proyecto).** Responsable de la planificación, monitoreo y control del proceso de pruebas, definición de objetivos, alcance, criterios de entrada y salida, gestión de riesgos y supervisión del cronograma de 11 semanas. Asimismo, realiza el triaje y cierre formal de incidencias en GitHub Issues y consolida los entregables normativos (*Test Plan* y *Test Summary Report*).

### Integrante: Luis Diego Perrigo Cruz
**Analista de Pruebas / Test Analyst.** Encargado de analizar los requisitos funcionales y no funcionales de InvenTree, diseñar las especificaciones de casos de prueba (`CS-01` al `CS-10`) aplicando técnicas de caja negra (partición de equivalencia y análisis de valores límite), auditar reglas de negocio durante la verificación de incidencias y mantener la matriz de trazabilidad bidireccional.

### Integrante: Juan Anderson Gutierrez Andia
**Ejecutor de Pruebas / QA Tester.** Responsable de desplegar y preparar el entorno local contenerizado (`localhost:8003`) junto con los datos iniciales de prueba, ejecutar paso a paso los procedimientos de prueba diseñados, recolectar las evidencias visuales de ejecución y registrar formalmente los reportes de incidentes (*Test Incident Reports*) en GitHub Issues.
