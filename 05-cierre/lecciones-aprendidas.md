# Lecciones Aprendidas

Reunión de cierre celebrada el **26 de marzo de 2026** con los patrocinadores, la directora del proyecto y la festejada.

## Lo que funcionó bien

| # | Lección | Evidencia | Recomendación a futuro |
|---|---------|-----------|------------------------|
| 1 | Cotizar al menos 3 proveedores por servicio | Se ahorraron $29,000 al elegir Las Palmas sobre Villa Real | Mantener la regla de las 3 cotizaciones |
| 2 | Reservar una contingencia desde el inicio | La reserva absorbió el aumento del banquete sin pedir dinero extra | Reservar entre el 5% y el 8% del presupuesto |
| 3 | Calendario fijo de ensayos los sábados | 12 ensayos completados sin conflictos escolares | Definir el calendario antes de reclutar chambelanes |
| 4 | Confirmar el headcount 10 días antes | Se evitó pagar platillos de más | Dejarlo por escrito en el contrato |
| 5 | Documentar todo en un repositorio versionado | Se puede rastrear qué cambió, cuándo y por qué | Usar Git también en proyectos no técnicos |

## Lo que se debe mejorar

| # | Problema detectado | Causa raíz | Acción correctiva a futuro |
|---|--------------------|------------|----------------------------|
| 1 | El costo del banquete subió $8,250 | El contrato no tenía cláusula de precio blindado contra inflación | Exigir cláusula de precio fijo con vigencia hasta el día del evento |
| 2 | Un padrino aportó $2,000 menos | La confirmación fue verbal, no escrita | Formato de compromiso firmado por cada padrino |
| 3 | La decoración se montó apenas a las 14:30 h | Se acordó un horario de montaje demasiado justo | Pactar el montaje con 6 horas de margen |
| 4 | El fotógrafo llegó 10 min tarde a la misa | No se le compartió el itinerario detallado por escrito | Enviar itinerario impreso a todos los proveedores 1 semana antes |
| 5 | La misa inició 12 min tarde | Retraso en el traslado de la festejada | Considerar 20 min de holgura en el traslado |

## Lecciones sobre el uso de Git en este proyecto

| # | Lección | Explicación |
|---|---------|-------------|
| 1 | Un commit por fase da trazabilidad | El historial cuenta la historia del proyecto: inicio, planificación, ejecución, seguimiento y cierre |
| 2 | Las ramas sirven para cambios en revisión | El aumento del banquete se trabajó en `cambio-banquete` sin tocar la versión oficial hasta su aprobación |
| 3 | El merge documenta la aprobación | Integrar la rama a `main` equivale a "el patrocinador autorizó el cambio" |
| 4 | Los mensajes de commit deben ser claros | "Actualiza costo del banquete" explica el porqué; "cambios" no explicaría nada |
| 5 | `git log` sustituye al reporte manual | El historial es en sí mismo la bitácora del proyecto |

## Conclusión general

El proyecto cumplió el **100% de sus entregables** dentro del presupuesto y en la fecha comprometida. El único desvío relevante (el costo del banquete) estaba **previsto como riesgo R1** y fue absorbido por la reserva de contingencia, lo que confirma el valor de planificar los riesgos antes de que ocurran.

**Recomendación final:** conservar este repositorio como plantilla para futuros eventos familiares.
