# Control de Cambios

Todo cambio que afecte **alcance, tiempo o costo** debe registrarse aquí y ser aprobado por los patrocinadores antes de aplicarse a los documentos del proyecto.

## Solicitud de cambio SC-01 — Incremento del costo del banquete

| Campo | Detalle |
|-------|---------|
| **Folio** | SC-01 |
| **Fecha de solicitud** | 24 de febrero de 2026 |
| **Solicita** | Banquetes Doña Chuy (proveedor) |
| **Descripción** | El proveedor informa un aumento en el precio de insumos (carne, lácteos y aceite) y solicita ajustar el costo por persona de **$320 a $375 MXN**. |
| **Impacto en costo** | +$8,250.00 MXN (de $48,000 a $56,250 para 150 personas) |
| **Impacto en tiempo** | Ninguno |
| **Impacto en alcance** | Ninguno. Se conserva el menú de 3 tiempos acordado. |
| **Alternativas evaluadas** | 1) Cambiar de proveedor a 18 días del evento (alto riesgo). 2) Reducir el menú a 2 tiempos (afecta la calidad esperada). 3) Aceptar el ajuste usando la reserva de contingencia. |
| **Recomendación** | Alternativa 3: aceptar el ajuste y cubrirlo con la reserva de contingencia. |
| **Decisión** | **APROBADA** el 25 de febrero de 2026 por Ricardo Ríos Mendoza |
| **Origen del recurso** | Reserva de contingencia (queda en $1,250.00) |
| **Riesgo asociado** | R1 de `02-planificacion/riesgos.md` |

### Cómo se aplicó este cambio en el repositorio

Este cambio **no se aplicó directamente sobre la versión oficial del proyecto**. Se trabajó primero en una rama independiente para poder revisarlo antes de integrarlo:

```bash
git branch cambio-banquete      # se crea la línea de trabajo paralela
git checkout cambio-banquete    # se cambia a esa rama
# se edita 02-planificacion/presupuesto.csv
git commit -m "Actualiza costo del banquete"
git checkout main               # main sigue con el presupuesto original
git merge cambio-banquete       # se integra el cambio ya aprobado
```

Así, mientras el cambio estuvo en revisión, la rama `main` conservó el presupuesto original de $320 por persona.

## Solicitudes rechazadas

| Folio | Descripción | Fecha | Decisión | Motivo |
|-------|-------------|-------|----------|--------|
| SC-02 | Contratar hora extra de mariachi (+$3,500) | 06/03/2026 | **Rechazada** | La reserva de contingencia ya estaba comprometida en SC-01 |
| SC-03 | Agregar 2 mesas más de invitados (+16 personas) | 02/03/2026 | **Rechazada** | Excede el mobiliario contratado y el headcount ya confirmado |

## Resumen del control de cambios

| Indicador | Valor |
|-----------|-------|
| Solicitudes recibidas | 3 |
| Aprobadas | 1 |
| Rechazadas | 2 |
| Impacto neto en el presupuesto | +$8,250.00 (absorbido por la reserva) |
