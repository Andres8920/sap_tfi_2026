# Anrriquez Andrés – Trabajo Final SAP-TFI-2026

- **Alumno:** Anrriquez, Aldo Andrés
- **Comisión:** Noche
- **Proyecto:** LOREBEL – Sistema de gestión para talleres de reparación
- **Documento principal:** [documento/LOREBEL.pdf](documento/LOREBEL.pdf)
- **Anexo complementario (versión 2):** [documento/ANEXO_complementario_v2.pdf](documento/ANEXO_complementario_v2.pdf) (fuente: [ANEXO_complementario_v2.md](documento/ANEXO_complementario_v2.md))
- **Código fuente del sistema:** <https://github.com/Andres8920/Lorebel-Sistema-De-Reparaciones>

## Descripción de la versión 2

La iteración 2 toma como requerimiento CORE el **cobro de órdenes de reparación** (RF-10, CU-10), con seis medios de pago (efectivo, transferencia, Mercado Pago, MODO, tarjeta de débito y tarjeta de crédito en cuotas), señas, control de saldo y bloqueo de la entrega con saldo pendiente. Incluye inicio de sesión con tres roles, auditoría de trazabilidad y de sesiones, y dos reportes con gráficos. El análisis y el diseño siguen ICONIX: casos de uso, modelo de dominio, robustez, secuencia y clases.

Cambios respecto de la versión 1:

- Anexo complementario con requerimientos funcionales numerados (RF-01 a RF-21), requerimientos no funcionales completos (desempeño, portabilidad, disponibilidad, mantenibilidad), glosario, disparador de CU-10, matriz de trazabilidad REQ → CU → robustez → secuencia → clases → TEST, documentación del patrón Strategy según el estándar UNR (Cristiá, 2015) y cálculo de cobertura.
- Diagrama de casos de uso corregido: se agregan CU-22 a CU-27 y el actor Técnico, y se quita el «include» de CU-13 a CU-14.
- Diagrama de robustez corregido: la Pasarela se comunica con un boundary (endpoint de notificación) y se agregan los alternativos A2 y A4.
- Nuevo diagrama de secuencia del curso básico de CU-10 (efectivo) con alternativos y excepciones.
- Nuevo diagrama de despliegue.
- Carpeta reorganizada en `documento/`, `diagramas/` y `capturas/`; se eliminó un archivo de prueba.

## Contenido de la carpeta

| Carpeta | Contenido |
|---|---|
| `documento/` | Documento principal (PDF) y anexo complementario de la versión 2 (PDF y Markdown). |
| `diagramas/` | Fuentes PlantUML (`.puml`) y diagramas renderizados (`.png`). `estilo.iuml` es el estilo común que incluyen todos los diagramas. |
| `capturas/` | Capturas de pantalla de la versión ejecutable (guion de la interfaz). |

| Diagrama | Archivo |
|---|---|
| Transición de estados del Pago | `diagramas/01_estados_pago` |
| Casos de uso (corregido) | `diagramas/02_casos_uso` |
| Dominio conceptual | `diagramas/03_dominio_conceptual` |
| Robustez CU-10 (corregido) | `diagramas/04_robustez` |
| Dominio actualizado | `diagramas/05_dominio_actualizado` |
| Secuencia CU-10 – Mercado Pago (A3) | `diagramas/06_secuencia_cobro` |
| Secuencia CU-10 – curso básico (nuevo) | `diagramas/06a_secuencia_cobro_basico` |
| Clases del módulo de cobros | `diagramas/07_clases` |
| DER implementado | `diagramas/08_der` |
| Arquitectura en capas | `diagramas/09_arquitectura` |
| Secuencia de auditoría | `diagramas/10_secuencia_auditoria` |
| Grafo de flujo de `validarPago()` | `diagramas/11_grafo_flujo` |
| Despliegue (nuevo) | `diagramas/12_despliegue` |

Para volver a generar los diagramas: `cd diagramas && plantuml -tpng *.puml` (y `dot -Tpng 11_grafo_flujo.dot -o 11_grafo_flujo.png`).
