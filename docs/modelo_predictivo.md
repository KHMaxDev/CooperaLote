# Escenarios de adopción e impacto del software

Versión 2.0 · 4 de noviembre de 2026 · Alcance tecnológico aprobado por el equipo. Metas, adquisiciones y servicios todavía sujetos a validación.

## Naturaleza del modelo

Modelo condicional, no pronóstico estadístico ni causal. No existen usuarios ni pruebas reales con los que calibrarlo. Sustituye las proyecciones de miel procesada por CooperaLote: el proyecto no procesa miel.

```text
N_t = organizaciones activas del periodo
R_t = N_t × r_t                          registros válidos, si r_t es promedio por organización
H_t = R_t × (b_t − d_t) / 60             horas de tarea potencialmente ahorradas
T_t = V_t × c_t                         toneladas únicas con expediente completo
DeltaT_t = V_t × (c_t − c0_t)            mejora documental respecto a cobertura previa
Cobertura_ref_t = 100 × T_t / 2727.78    escala relativa a miel estatal 2023
```

`b` y `d` son minutos por tarea antes/después. `V` es volumen físico único registrado por participantes, sin sumar repetidamente entregas, lotes padres e hijos. `c` es proporción cubierta y `c0` la cobertura anterior. Ni T ni DeltaT representan nueva producción. La referencia 2023 (F02) no es denominador medido del año futuro.

## Sensibilidad anual ilustrativa

Hipótesis comunes: 600 registros por organización al año, 5 minutos antes y 3 después, 10 t únicas por organización, cobertura posterior 90% y previa 50%. Todos los parámetros requieren medición. Organizaciones activas no equivalen a pagadoras.

| Escenario | N | Registros | Horas potenciales ahorradas | V, t | T, t | DeltaT, t | T / referencia 2023 |
|---|---:|---:|---:|---:|---:|---:|---:|
| Sin adopción | 0 | 0 | 0 | 0 | 0 | 0 | 0% |
| Validación limitada | 1 | 600 | 20 | 10 | 9 | 4 | 0.3299% |
| Adopción intermedia | 3 | 1,800 | 60 | 30 | 27 | 12 | 0.9898% |
| Expansión condicionada | 5 | 3,000 | 100 | 50 | 45 | 20 | 1.6497% |

Son escenarios anuales de sensibilidad, no compromisos para el piloto de seis meses. La reducción de 5 a 3 minutos equivale a 40%, distinta de la meta operativa de 30%; no se presenta ninguna como efecto observado. Si d≥b, el ahorro es cero o negativo. Si un mismo lote pasa por varias organizaciones, deduplicar V o no publicar cobertura regional.

## Límites de atribución

No se estima aumento de producción estatal, turismo, población, ingresos de productores ni emisiones evitadas. Ahorro de tiempo no significa automáticamente ahorro de nómina ni ingreso para CooperaLote. Las organizaciones deben decidir cómo usan la información; la mejora física eventual se evaluará aparte.

Antes de publicar un resultado, medir tareas equivalentes, volumen único, cobertura previa y posterior, selección de participantes y faltantes. Para atribución causal se necesita diseño de evaluación adicional; estas fórmulas únicamente hacen explícitas las hipótesis.
