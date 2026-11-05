# Presupuesto tecnológico y sostenibilidad financiera

Versión 2.0 · 4 de noviembre de 2026 · Alcance tecnológico aprobado por el equipo. Metas, adquisiciones y servicios todavía sujetos a validación.

## Alcance y clasificación

Solicitud objetivo: **$95,000 MXN** para cinco integrantes. Todo el apoyo se destinará a equipamiento y servicios del producto. Sin remuneraciones a integrantes, miel, envases, maquinaria alimentaria ni capital para inventario apícola. Los cálculos previos de margen por frasco, ventas de miel y brecha de $17,500 dejan de aplicar al proyecto.

Los valores siguientes son **topes internos ilustrativos para preparar cotizaciones**, no precios investigados, ofertas comerciales ni rubros cuya elegibilidad esté confirmada. Se expresan como desembolsos finales objetivo, incluidos impuestos y envío cuando correspondan; el desglose fiscal lo dará cada proveedor. No son una orden de compra ni presupuesto final para presentar sin evidencia.

## Distribución propuesta de la solicitud

| ID | Concepto | Cantidad / duración | Tope unitario MXN | Subtotal MXN | Resultado y condición |
|---|---|---|---:|---:|---|
| E01 | Estaciones de desarrollo | 2 equipos | 18,000 | 36,000 | Backend y pruebas locales; sólo si inventario demuestra insuficiencia de laptops existentes |
| E02 | Dispositivos móviles de prueba | 2 dispositivos | 4,000 | 8,000 | Validar captura y QR en configuraciones diferentes; evitar duplicar dispositivos ya disponibles |
| E03 | Respaldo eléctrico | 2 unidades | 2,000 | 4,000 | Continuidad de estaciones/red; dimensionar carga y justificar necesidad |
| E04 | Almacenamiento externo de respaldo | 2 unidades | 1,000 | 2,000 | Copias locales cifradas rotativas, distintas del respaldo remoto |
| | **Equipamiento** | | | **50,000** | Inventario, custodia y pruebas de aceptación |
| S01 | Alojamiento de pruebas y piloto | 12 meses | 1,000 | 12,000 | Entornos separados con límites de uso; cotizar configuración |
| S02 | Copias remotas y almacenamiento de evidencias | 12 meses | 300 | 3,600 | Recuperación fuera del alojamiento principal; evitar servicios duplicados en S01 |
| S03 | Dominio y correo del proyecto | 1 paquete anual | 1,400 | 1,400 | Identidad y contacto del servicio; TLS gratuito cuando sea viable |
| S04 | Evaluación externa de seguridad | 1 servicio delimitado | 16,000 | 16,000 | Revisión de acceso entre organizaciones, informe y nueva prueba tras correcciones |
| S05 | Evaluación externa de usabilidad y accesibilidad | 1 servicio delimitado | 12,000 | 12,000 | Protocolo, cinco sesiones objetivo, hallazgos y revisión de mejoras; sujeto a reclutamiento |
| | **Servicios** | | | **45,000** | Entregables y conformidad documentados |
| | **Total solicitado propuesto** | | | **95,000** | Sujeto a cotizaciones y conceptos autorizados |

S04 y S05 no pagan programación a integrantes. El equipo implementa correcciones y conserva la responsabilidad técnica. Si el equipo puede ejecutar una evaluación con independencia y evidencia suficientes, deberá justificarse si contratarla agrega valor. No adquirir servicios sólo para completar el monto.

## Justificación y evidencia por adquisición

Para cada renglón preparar: problema, recurso existente, especificación mínima, alternativa de reutilización, dos o tres cotizaciones comparables como control interno, proveedor, impuestos, entrega, garantía, vigencia, concepto oficial al que corresponde y entregable. El número de cotizaciones aquí es una recomendación, no una exigencia atribuida a la convocatoria.

E01 puede considerar inicialmente 16 GB de RAM y SSD de 512 GB como perfil de referencia, sin GPU dedicada; comprobar necesidad ejecutando el entorno en las laptops disponibles. No existe evidencia para afirmar todavía que se necesitan dos equipos nuevos. Si las laptops bastan, reducir o reasignar únicamente a necesidades permitidas y comprobadas, según autorización. No inflar importes para alcanzar $95,000.

No se conoce el inventario de laptops. Por ello esta distribución sirve para preparar la solicitud, pero **la justificación definitiva del monto sigue incompleta**. El apoyo puede autorizarse por un monto menor y requerir ajuste conforme a la convocatoria.

## Trabajo y recursos aportados

| Recurso | Tratamiento | Pendiente |
|---|---|---|
| Programación, documentación y capacitación por los cinco integrantes | Aportación de trabajo; $0 cargado al apoyo | Horas disponibles por persona y valoración económica referencial |
| Laptops actuales | Aportación de uso, sin compra presunta | Cantidad, especificaciones, propiedad y disponibilidad |
| Internet, electricidad y lugar de trabajo | No incluidos en la solicitud propuesta | Responsable de cubrirlos, costo incremental y disponibilidad |
| Contabilidad, obligaciones fiscales y trámites aplicables | No presupuestados por falta de datos | Determinar necesidad, costo y fuente de recursos |
| Transporte para sesiones presenciales | No incluido | Priorizar remoto, pero estimar desplazamientos indispensables |

Estos costos no son cero por estar fuera del apoyo. No se ha confirmado una aportación monetaria adicional. Registrar gasto directo y costo económico del tiempo por separado. El proyecto no puede declararse financieramente viable hasta cubrir los costos indispensables no financiados.

## Programación de desembolsos del apoyo

Ejemplo sujeto a reglas de comprobación: equipo $50,000 en M1; servicios S01–S03 $17,000 al inicio si se permiten pagos anuales; S05 $12,000 en M4 tras conseguir usuarios; S04 $16,000 en M5 antes del piloto con información sensible. Total: $95,000. Saldo del apoyo recibido completo: M0 $95,000; M1 $28,000; M4 $16,000; M5 $0. Se separará el dinero comprometido del disponible. No se gastará antes de autorización suponiendo reembolso.

El prototipo previo se realiza con laptops disponibles y herramientas gratuitas o locales. Si éstas no bastan, reducir su complejidad y documentar la limitación; no financiarlo ficticiamente con el apoyo futuro. Los 12 meses de servicio son una hipótesis a verificar frente al periodo de ejecución autorizado.

## Ingresos y continuidad después del apoyo

Clientes potenciales: organizaciones existentes. Modelo por validar: suscripción por organización y servicios de implementación con alcance definido. No hay clientes, ingresos ni tarifa aceptada. La versión gratuita del piloto no cuenta como suscripción pagada.

```text
Ingreso mensual = organizaciones pagadoras × tarifa neta + servicios efectivamente cobrados
Contribución mensual = ingreso − costos variables por organización − costos variables de servicios
Resultado económico = contribución − costos fijos − valor del trabajo aportado − depreciación
Equilibrio recurrente = techo(costos fijos / (tarifa neta − costo variable por organización))
```

Ejemplo exclusivamente de sensibilidad: fijos $3,000/mes, tarifa $600 y costo variable $100 ⇒ 6 organizaciones pagadoras para equilibrio de caja simplificado. Con tarifa $400 ⇒ 10; con tarifa $800 ⇒ 5. Estos parámetros no proceden de entrevistas y excluyen remuneración futura, impuestos y depreciación. No prueban rentabilidad integral ni aseguran cubrir a cinco personas.

Escenario sin clientes: ingresos $0; identificar cómo sostener las obligaciones no prepagadas. Antes de agotar servicios financiados, decidir renovación con cobros reales, aportaciones expresas o cierre ordenado con exportación de datos. No se presume otro subsidio.
