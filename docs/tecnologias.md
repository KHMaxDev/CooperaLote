# Tecnologías y herramientas propuestas

Diseño de referencia, no compra ni implementación. Se conserva la orientación del documento maestro y se posponen integraciones complejas.

| Componente | Propuesta | Justificación y costo a presupuestar |
|---|---|---|
| Aplicación | Laravel, Vue y Tailwind CSS | Continuidad con maestro; validar competencias del equipo y horas reales |
| Datos | PostgreSQL | Relaciones entre entregas, lotes y pagos; respaldo y operación requieren responsable |
| Autenticación | Sanctum para aplicación propia | Sesión/cookies con protección CSRF; las autorizaciones de negocio se implementan aparte |
| Captura local | PWA, Service Worker e IndexedDB | Cola provisional; no garantiza disponibilidad en todos los equipos |
| Documentos | Almacenamiento privado con respaldo | Comprobantes y resultados de calidad separados de consulta pública |
| Reportes | Exportación CSV y PDF | Portabilidad, archivo y conciliación; evitar dependencia del proveedor |
| Identificación | QR con identificador público opaco | Consulta de lote; el QR no certifica autenticidad |
| Operación | Hosting administrado o VPS mantenido, TLS y monitoreo | Decidir con cotización de soporte, respaldo y recuperación, no sólo renta |
| Control físico | Báscula, refractómetro y material alimentario adecuado | Selección por procedimiento de calidad; calibración/verificación y laboratorio presupuestados |
| Seguimiento | Tablero de tareas y registro de decisiones en Markdown | Trazabilidad de cambios y responsables |

## Fuentes técnicas primarias consultadas

- [Laravel Sanctum](https://laravel.com/framework/docs/13.x/sanctum): autenticación para SPA/API. Usar versión soportada y compatible al implementar; esta consulta no fija una versión contractual.
- [PostgreSQL, políticas de seguridad por fila](https://www.postgresql.org/docs/current/ddl-rowsecurity.html): controles de fila y excepciones de propietarios/roles privilegiados.
- [MDN, IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API): persistencia local estructurada; probar cuotas y comportamiento del navegador elegido.

## Política de selección y mantenimiento

Antes del desarrollo, registrar versiones, soporte de seguridad, licencia, costo anual, disponibilidad local y pruebas de restauración. Revisión mensual de dependencias y cambios críticos. No se promete que $8,000 cubran un SaaS completo: se debe estimar desarrollo, pruebas, capacitación y mantenimiento de forma separada.

Una hoja de cálculo controlada puede sostener el diagnóstico y la primera conciliación. Se migrará al MVP con validación de saldos, registro de importación y conservación de originales. No se recomienda IA para liberar lotes, emitir dictámenes sanitarios o autorizar pagos. Las proyecciones de este plan se reproducen con fórmulas explícitas.
