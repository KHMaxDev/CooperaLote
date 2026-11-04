# Modelo predictivo condicional de impacto

Versión 1.0 · Escenarios 2027–2029. Es un modelo contable de mecanismos y sensibilidad, no una regresión estimada ni pronóstico oficial. Los pocos datos históricos y sus diferencias de metodología no permiten calibrar un efecto causal regional.

## Mecanismo y unidades

El proyecto recibe miel ya producida. Su intervención directa propuesta es reducir pérdidas de acondicionamiento, documentar lotes y mejorar ventas. Por tanto, se espera actuar sobre volumen comercializable y trazabilidad; no se suma el volumen recibido a producción primaria estatal.

Definir:

- `Q_t`: toneladas recibidas y procesadas en el año t, sin duplicar movimientos internos.
- `m0`: merma contrafactual sin mejora, supuesto 5%.
- `m1`: merma con proyecto, supuesto base 2%.
- `B`: referencia de producción estatal 2023 = 2,727.78 t (F02), fija sólo para dimensionar.
- `tau0`: fracción del volumen participante ya trazable antes, supuesto 0 para escenario máximo; medir en campo.
- `a`: fracción atribuible a la intervención, entre 0 y 1; no estimada.

Ecuaciones:

```text
V_sin,t = Q_t × (1 − m0)
V_con,t = Q_t × (1 − m1)
DeltaV_t = Q_t × (m0 − m1)
Efecto atribuible_t = a × DeltaV_t
Cobertura de referencia_t = 100 × Q_t / B
Cobertura incremental trazable_t = 100 × (1 − tau0) × Q_t / B
Equivalente regional_t = 100 × DeltaV_t / B
```

`V` se mide en t comercializables. La cobertura es relativa a un año histórico, no porcentaje medido de la producción de 2027–2029. No son puntos porcentuales de PIB ni crecimiento de la producción agrícola oficial.

## Escenario base de capacidad, pendiente de financiación

| Año | Q, t/año | Sin mejora, t | Con mejora, t | Recuperación, kg | Cobertura sobre B | Recuperación/B |
|---|---:|---:|---:|---:|---:|---:|
| 2027 | 1.25 | 1.1875 | 1.2250 | 37.5 | 0.0458% | 0.00137% |
| 2028 | 3.00 | 2.8500 | 2.9400 | 90.0 | 0.1100% | 0.00330% |
| 2029 | 6.00 | 5.7000 | 5.8800 | 180.0 | 0.2200% | 0.00660% |

Las cantidades son supuestos de escala, no contratos. En 2027, 1.25 t recibidas permiten 1.225 t comercializables con 2% de merma. La meta financiera de 1.000 t vendidas deja hasta 0.225 t para inventario/muestras/salidas documentadas, según fecha de corte. El modelo anual 2027 no equivale exactamente al flujo diciembre 2026–noviembre 2027; conciliar calendarios al levantar pedidos.

## Sensibilidad en 2029

| Escenario | Q, t | m0 | m1 | DeltaV, kg | DeltaV/B |
|---|---:|---:|---:|---:|---:|
| Sin mejora | 6 | 5% | 5% | 0 | 0% |
| Conservador | 3 | 5% | 4% | 30 | 0.00110% |
| Base | 6 | 5% | 2% | 180 | 0.00660% |
| Expansión condicionada | 12 | 5% | 1% | 480 | 0.01760% |

Si `a=0.5`, el efecto atribuible del caso base sería 90 kg; no se afirma que a valga 0.5. Si m1>m0, el resultado es negativo. Un choque de suministro de −20% reduce Q y DeltaV en 20% manteniendo mermas constantes. Si el denominador regional fuese 20% menor/mayor, el equivalente base sería aproximadamente 0.00825%/0.00550%. No se asignan probabilidades ni intervalos de confianza a estos escenarios.

## Vinculación a estadísticas regionales

El efecto directo sobre población y afluencia turística se fija en cero dentro del modelo: no existe mecanismo ni evidencia para predecir cambios medibles por un piloto de este tamaño. La producción primaria regional también permanece sin incremento atribuido, al no intervenir colmenas. El efecto potencial es disponibilidad comercial recuperada y cobertura documental, indicadores que deben reportarse aparte de la serie SIAP.

Para estimar `Y_con,t = Y_sin,t + a×DeltaV_t` se necesita una línea base regional de volumen comercializable `Y_sin,t`, actualmente no disponible. Por eso se informa DeltaV y su escala sobre B, sin fabricar niveles regionales futuros. En trazabilidad, tau0 debe medirse para no atribuir al proyecto registros que ya existían.

## Calibración y validación

Medir m0 en operaciones comparables antes de la intervención, con balanzas verificadas y separación de muestras/inventarios. Actualizar Q por contratos y capacidad; medir m1 por lotes. Al alcanzar 12 meses, evaluar estacionalidad y grupo de comparación según [KPIs](kpis_evaluacion.md). Reportar incertidumbre de pesaje y faltantes. Sólo tras esta etapa se podría estimar un modelo estadístico y validarlo fuera de muestra.
