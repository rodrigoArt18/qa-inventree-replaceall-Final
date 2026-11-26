# Aseguramiento de la Calidad de Software — Proyecto ReplaceAll (InvenTree)

Repositorio oficial de gestión de pruebas, trazabilidad y control de incidentes del sistema **InvenTree** (`localhost:8003`) para **ReplaceAll**, estructurado bajo las normas **ISO/IEC/IEEE 29119-3**, **ISO/IEC/IEEE 25010** y **TMMi Nivel 2**.

---

## Reglas de Coordinación y Flujo de Trabajo del Equipo

Para mantener el orden, la trazabilidad y la independencia en las revisiones durante el ciclo de pruebas, el equipo cumple las siguientes reglas operativas:

1. **Control de Entorno (`localhost:8003`):** Antes de ejecutar casos de prueba o pruebas de carga, se verifica que los contenedores Docker de InvenTree estén activos y con los datos base cargados. Ningún integrante modifica configuraciones globales sin avisar al equipo.
2. **Registro Único de Incidentes (1 Incidente = 1 Issue):** Cada defecto detectado (`FAIL`) se registra como un Issue independiente en GitHub con el formato `INC-00X: [Título descriptivo]`, vinculando su caso de prueba de origen (`CS-01` a `CS-10`), severidad, prioridad y pasos de reproducción.
3. **Flujo de Estados y Triaje:**
   * Todo incidente nuevo ingresa en estado **`Open`** tras su ejecución.
   * Los incidentes bloqueantes o pendientes de corrección en código permanecen en **`Open`** como *Known Issues* documentados.
   * Solo el **Test Manager** valida el cierre (`Closed`) previa verificación cruzada con el **Test Analyst**.
4. **Comunicación y Validación Cruzada:**
   * **Canal rápido (WhatsApp):** Coordinación diaria, disponibilidad del entorno y alertas de bloqueo.
   * **Canal formal (GitHub Issues):** Evidencia documental, comentarios de seguimiento y trazabilidad auditables.
5. **Control de Versiones y Evidencias:** Toda captura de pantalla (InvenTree, GitHub Issues y Apache JMeter) debe conservar la nomenclatura estandarizada de los Anexos (`Figura A`, `B`, `C`, `D` y `E`) antes de consolidarse en el informe final.

---

## Asignación de Roles (ISO/IEC/IEEE 29119-3)

* **Rodrigo Arturo Paredes Santa Cruz — Gerente de Pruebas / Test Manager (Líder del Proyecto):** Planificación, monitoreo y control del proceso de pruebas, definición de objetivos, alcance, criterios de entrada/salida, gestión de riesgos, triaje y cierre formal de incidencias en GitHub Issues, y consolidación de entregables (*Test Plan* y *Test Summary Report*).
* **Luis Diego Perrigo Cruz — Analista de Pruebas / Test Analyst:** Análisis de requisitos funcionales y no funcionales de InvenTree, diseño de casos de prueba (`CS-01` al `CS-10`) con técnicas de caja negra, auditoría de reglas de negocio y mantenimiento de la matriz de trazabilidad bidireccional.
* **Juan Anderson Gutierrez Andia — Ejecutor de Pruebas / QA Tester:** Despliegue del entorno local contenerizado (`localhost:8003`), ejecución paso a paso de los procedimientos de prueba, recolección de evidencias visuales y registro formal de incidentes (*Test Incident Reports*) en GitHub Issues.
