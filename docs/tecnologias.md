# Tecnologías, equipo y servicios

Versión 2.0 · 4 de noviembre de 2026 · Alcance tecnológico aprobado por el equipo. Metas, adquisiciones y servicios todavía sujetos a validación.

## Stack propuesto

| Componente | Propuesta | Justificación y condición |
|---|---|---|
| Backend/API | Laravel | Validación y reglas de negocio; confirmar competencias del equipo |
| Interfaz | Vue y Tailwind CSS | Formularios móviles y componentes reutilizables |
| Datos | PostgreSQL | Transacciones, genealogía e integridad relacional |
| Autenticación | Sanctum para la aplicación propia | Sesión/cookies y protección CSRF; autorización adicional por organización |
| Conectividad limitada | PWA, Service Worker, IndexedDB | Captura provisional; probar compatibilidad y sincronización |
| Exportación | CSV y PDF | Portabilidad y comprobación por usuarios |
| Trazabilidad | QR con identificador opaco | Consulta pública mínima; no certificación |
| Calidad | Pruebas automatizadas, control de versiones y revisión de código | Errores reproducibles, revisión cruzada y liberaciones identificables |
| Infraestructura | Alojamiento, documentos privados y respaldos separados | Costos desglosados S01–S03 en finanzas |

No se fijan versiones antes de verificar soporte, licencia y compatibilidad al implementar. El software libre no elimina costos de configuración, operación o mantenimiento.

## Recursos físicos

Hay laptops reportadas, pero no inventario completo. Las dos estaciones nuevas y dos dispositivos de prueba del presupuesto son hipótesis condicionadas a carencias demostradas. E01–E04 no son dotaciones personales ni premios individuales: el equipo documentará propiedad, custodia y uso del proyecto. Priorizar reutilización y reparación cuando cumplan los requisitos. No se propone GPU dedicada, servidor local de producción ni maquinaria alimentaria.

## Servicios independientes

La programación la realizan los cinco integrantes con trabajo aportado. S04 evalúa seguridad y verifica correcciones; S05 evalúa usabilidad/accesibilidad. Cada contrato debe tener alcance, entregables, calendario, responsable de aceptación y costo final. Evitar duplicidad entre hosting y respaldos.

## Referencias técnicas primarias

- [Laravel Sanctum](https://laravel.com/framework/docs/13.x/sanctum).
- [PostgreSQL, seguridad por fila](https://www.postgresql.org/docs/current/ddl-rowsecurity.html).
- [MDN, IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API).

Referencias consultadas en la investigación inicial; revalidar versiones antes de programar. No se han contratado proveedores ni adquirido licencias. El [presupuesto](finanzas.md) contiene topes de planeación, no precios comerciales verificados.
