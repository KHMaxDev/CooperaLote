# CooperaLote · Especificación visual del sistema

Versión 1.0 · 5 de noviembre de 2026 · Propuesta de interfaz y experiencia de uso.

Este documento describe las pantallas, contenidos, componentes, interacciones y recorridos de CooperaLote. Las imágenes son propuestas visuales estáticas: no acreditan que las funciones estén implementadas. Todos los nombres, folios, documentos, cantidades y actividades mostrados son ficticios.

## 1. Criterio documental y alcance

La referencia vigente es la versión 2.0 de [documento maestro](../docs/documento_maestro_cooperalote.md), [decisiones](../docs/decisiones.md), [prototipo](../docs/prototipo.md) y [control documental](../docs/control_documental.md). Se incorporan las necesidades de trazabilidad, evidencia, permisos, conectividad, exportación y evaluación descritas en los demás documentos de `docs`.

El enfoque anterior de `README.md`, `plan_estrategico.md` y la presentación sirve como antecedente. Prevalece el cambio documentado: CooperaLote es un producto digital para organizaciones apícolas existentes. La interfaz representa las operaciones registradas por cada organización; no presenta al equipo desarrollador como productor ni vendedor de miel. El presupuesto del proyecto y su expediente de convocatoria no forman parte del tablero operativo de las organizaciones.

El primer recorrido demostrable comprende organización → productor → entrega → lote → inventario → salida → consulta QR. Se proponen también las pantallas necesarias para completar la experiencia del producto mínimo: acceso, evidencias, exportaciones, historial, pendientes, integrantes y configuración. Los detalles adicionales de diseño, nombres de roles y distribución de componentes aquí definidos son propuestas para validar con usuarios.

Costos, ventas y liquidaciones corresponden a una ampliación posterior sujeta a validación. No aparecen como módulos activos, cifras de rentabilidad o botones utilizables en estas imágenes. Tampoco se incluyen una tienda, pagos bancarios, facturación, certificaciones, predicción de cosechas ni un panel de administración comercial del proveedor.

## 2. Dirección visual compartida

### Personalidad y lenguaje

La interfaz debe sentirse serena, clara y cercana a una organización productiva. Predominan las superficies marfil, los encabezados verdes y el uso moderado del color miel. Se evita convertir la aplicación en una pieza publicitaria: los datos y las acciones tienen prioridad sobre fotografías, ilustraciones o adornos.

Se conserva la paleta base de la presentación local como continuidad visual, sin conservar sus supuestos comerciales anteriores. La marca es el texto **CooperaLote**, acompañado de un pequeño hexágono lineal propuesto como identificador, sin implicar que exista un logotipo aprobado. No se incorporan escudos institucionales, sellos de certificación o logotipos de aliados.

| Elemento | Propuesta visual | Uso |
|---|---|---|
| Verde profundo | `#163C35` | Navegación, títulos, botón principal y cifras importantes |
| Marfil | `#F8F6EF` | Fondo general |
| Blanco | `#FFFFFF` | Formularios, tarjetas, tablas y paneles |
| Miel | `#B47C24` | Acentos, pendientes, iconos y etiquetas de demostración |
| Verde grisáceo | `#52635D` | Texto secundario y metadatos |
| Terracota | `#A34936` | Errores, rechazo y acciones de corrección delicadas |
| Borde suave | `#D9DED8` | Separadores, campos y límites de tarjetas |
| Verde pálido | `#E9F2EB` | Confirmaciones con icono y texto |

Tipografía propuesta: Inter, con alternativas de sistema si no está disponible. Cuerpo de 16 px; textos auxiliares de 14 px; títulos de pantalla de 28–32 px; títulos de sección de 20 px; cifras destacadas de 32–40 px. Los folios usan cifras y caracteres fáciles de distinguir. Los números de tablas se alinean a la derecha y conservan una precisión uniforme.

La retícula usa múltiplos de 8 px, margen exterior de 32 px en escritorio y de 16 px en móvil. Las tarjetas tienen esquinas de 12 px, campos de 8 px y sombras muy leves. Los botones principales son verdes con texto blanco; los secundarios tienen fondo claro y borde. El color miel se reserva para acentos y no para párrafos pequeños sobre blanco.

### Estructura de escritorio

Referencia de diseño: lienzo de 1440 × 1000 px. Navegación lateral de aproximadamente 232 px; barra superior de 72 px; área de trabajo flexible. La barra superior contiene organización activa, indicador de conexión, acceso a pendientes, ayuda y avatar con iniciales. Debajo aparece una franja discreta pero persistente: **“Demostración · Datos ficticios”**.

El menú se agrupa en tres bloques:

- **Operación:** Inicio, Productores, Entregas, Lotes, Inventario.
- **Seguimiento:** Evidencias, Reportes, Historial, Pendientes.
- **Organización:** Equipo y permisos, Configuración.

La consulta y configuración del QR se abren desde el lote. La opción activa utiliza un fondo verde pálido o un contraste claro dentro del lateral; también cambia el peso del texto y presenta un indicador de selección. La navegación no depende sólo del color.

El cuerpo de cada pantalla comienza con una ruta breve cuando hay jerarquía, un título, una explicación de una línea y una acción principal. Los filtros se sitúan antes de las tablas. Las acciones secundarias se ubican en botones con texto o en un menú identificado como “Más acciones”. No se ocultan tareas principales detrás de iconos sin etiqueta.

### Adaptación móvil y tableta

En móvil, a partir de un ancho de referencia de 390 px, la barra lateral desaparece. La cabecera muestra el nombre de la organización abreviado, conexión y menú. La navegación inferior contiene **Inicio, Entregas, Lotes y Más**, con iconos y texto. En un formulario, la navegación inferior se sustituye por una franja de acciones que respeta el teclado y el área segura del dispositivo.

Las tablas pasan a tarjetas: folio y estado arriba; dato principal en grande; fecha y procedencia debajo; acción explícita al final. No se exige desplazarse lateralmente para leer datos esenciales. Los filtros secundarios se abren en un panel “Filtrar”; el número de filtros activos queda visible. Las genealogías disponen de una vista de lista equivalente al diagrama.

En tableta se permite una navegación lateral compacta y formularios de dos columnas sólo si cada campo mantiene suficiente espacio. En todas las dimensiones se conserva el orden de lectura, los nombres de las acciones y la información prioritaria.

### Convenciones comunes

- Cantidades en kilogramos, por ejemplo **100.00 kg**. Se acepta captura con coma o punto decimal y se presenta un formato uniforme. No se suman frascos con kilogramos ni se mezclan unidades sin equivalencia explícita.
- Fechas visibles como **05 nov 2026**; cuando importe el orden, hora y zona de la organización. La referencia de demostración es Quintana Roo, UTC−05:00.
- Un valor desconocido aparece como **“Sin dato”** o **“ND”**, nunca como cero. Un indicador sin denominador muestra **“No calculable”**.
- Los estados llevan icono y palabra: Borrador, Pendiente, Confirmado, Requiere revisión, Rechazado, Archivado. El estado del registro, la condición operativa del lote y su visibilidad pública son conceptos distintos.
- Confirmado significa que el registro fue aceptado en el flujo; no significa calidad certificada. “Disponible” describe una condición registrada por un responsable de la organización.
- Los enlaces de folio conducen al detalle correspondiente y conservan los filtros al volver. Las selecciones y cambios no guardados generan una advertencia antes de abandonar la pantalla.
- Las acciones concluyen con una confirmación breve y verificable: folio creado, cantidad afectada y próximo paso. El aviso no es la única evidencia: el registro aparece en la lista y en su historial.
- Durante una espera se muestran espacios de carga con la forma del contenido. Un error conserva la captura y ofrece “Reintentar”. No se reemplaza una lista que falló por un falso estado vacío.
- Los formularios identifican campos obligatorios mediante texto y asterisco explicado; muestran el error junto al campo y un resumen al comienzo. El foco vuelve al primer error.
- Las confirmaciones relevantes indican objeto, organización y consecuencia. “Cancelar” no borra datos confirmados. Los registros confirmados se corrigen con motivo visible y conservan su historial.
- Las superficies de demostración incluyen el distintivo correspondiente, incluso en archivos exportados y vistas públicas. No se copian datos personales reales a las imágenes.

### Accesibilidad y facilidad de uso

Objetivos de diseño: contraste mínimo de 4.5:1 para texto corriente, foco visible, controles utilizables con teclado, áreas táctiles de al menos 44 × 44 px y lectura sin pérdida de información al ampliar el texto. El contraste deberá comprobarse al implementar; estas imágenes no constituyen una auditoría de accesibilidad.

Los iconos siempre tienen nombre accesible; las gráficas ofrecen cifras y tablas equivalentes; los avisos no desaparecen antes de poder leerlos. No se usa movimiento imprescindible para comprender un resultado. Los paneles y diálogos tienen título, cierre accesible y devuelven el foco al control que los abrió. Las ayudas explican la tarea con lenguaje cotidiano: “Cantidad recibida”, “Ver origen”, “Guardar borrador” y “Revisar diferencias”.

## 3. Personas, permisos y datos de demostración

### Perfiles propuestos

| Perfil | Experiencia visible |
|---|---|
| Administración de la organización | Todas las pantallas de su organización; integrantes, permisos, configuración y revisiones autorizadas |
| Operación | Productores, entregas, lotes y movimientos según autorización; captura y seguimiento de sus pendientes |
| Revisión | Evidencias, trazabilidad, revisión de condiciones y correcciones permitidas; consulta y reportes |
| Consulta | Lectura de información autorizada; exportación únicamente si se concede ese permiso |
| Visitante público | Sólo pantalla pública del lote mediante QR o identificador compartido |

Estos perfiles son una propuesta de experiencia, no los cinco roles del equipo desarrollador. Un productor registrado no recibe automáticamente acceso de usuario. Una persona sólo ve las organizaciones a las que pertenece; cambiar de organización cambia claramente el contexto de trabajo. La interfaz muestra acciones permitidas y, cuando sea útil explicar una restricción, un control deshabilitado con motivo legible.

### Caso de referencia para las imágenes

| Dato | Valor ficticio consistente |
|---|---|
| Organización principal | Organización Demo del Mayab |
| Segunda organización de ejemplo | Organización Demo Costa; sin operaciones en esta maqueta |
| Persona que opera | Usuario Demo · Administración |
| Productor | Productor Demo 01 · PR-001 |
| Procedencia general | Othón P. Blanco, Quintana Roo |
| Entrega | ENT-0001 · 05 nov 2026 · 100.00 kg |
| Lote | LOT-0001 · Miel de abeja · 100.00 kg de entrada |
| Movimiento de entrada | MOV-0001 · +100.00 kg · 09:30 |
| Movimiento de salida | MOV-0002 · −20.00 kg · 10:00 · Salida de ejemplo |
| Pérdidas documentadas | 0.00 kg |
| Existencia resultante | 80.00 kg |
| Evidencia | comprobante-demo.pdf · Documento de ejemplo |
| Situación documental | 1 de 1 lotes con origen y movimientos completos; no equivale a certificación |

Las pantallas de captura muestran el momento anterior a confirmar la acción. Las pantallas de consulta muestran el caso terminado. La pantalla 16 ilustra un escenario alternativo sin conexión; su borrador no se suma al caso confirmado. Esta distinción evita interpretar las imágenes como operaciones adicionales.

## 4. Inventario de pantallas e imágenes

Cada fila corresponde a una pantalla completa y a una imagen independiente. Los paneles, pestañas y diálogos descritos dentro de una pantalla son estados de esa misma pantalla; la imagen representa el estado indicado, no todas sus variantes simultáneamente.

| ID | Pantalla | Estado representado | Imagen |
|---|---|---|---|
| P01 | Acceso | Formulario de entrada y acceso a demostración | [01-acceso.png](imgs/01-acceso.png) |
| P02 | Organizaciones | Selección entre dos organizaciones ficticias | [02-organizaciones.png](imgs/02-organizaciones.png) |
| P03 | Inicio | Resumen posterior a la salida de 20 kg | [03-inicio.png](imgs/03-inicio.png) |
| P04 | Productores | Padrón y panel de ficha del productor | [04-productores.png](imgs/04-productores.png) |
| P05 | Entregas | Listado y resumen de ENT-0001 | [05-entregas.png](imgs/05-entregas.png) |
| P06 | Registrar entrega | Captura móvil de 100 kg antes de confirmar | [06-registrar-entrega.png](imgs/06-registrar-entrega.png) |
| P07 | Lotes | Lista con panel de creación a partir de una entrega | [07-lotes.png](imgs/07-lotes.png) |
| P08 | Detalle del lote | Origen, recorrido y balance de LOT-0001 | [08-detalle-lote.png](imgs/08-detalle-lote.png) |
| P09 | Inventario | Balance y movimientos confirmados | [09-inventario.png](imgs/09-inventario.png) |
| P10 | Registrar movimiento | Salida de 20 kg con saldo proyectado de 80 kg | [10-registrar-movimiento.png](imgs/10-registrar-movimiento.png) |
| P11 | Evidencias | Documento privado vinculado y su panel de revisión | [11-evidencias.png](imgs/11-evidencias.png) |
| P12 | Compartir lote | Selección de información pública y vista previa | [12-compartir-qr.png](imgs/12-compartir-qr.png) |
| P13 | Consulta pública | Información mínima del lote en móvil | [13-consulta-publica.png](imgs/13-consulta-publica.png) |
| P14 | Reportes y exportación | Balance del caso y configuración de descarga | [14-reportes.png](imgs/14-reportes.png) |
| P15 | Historial | Secuencia de registros y detalle de un evento | [15-historial.png](imgs/15-historial.png) |
| P16 | Pendientes de envío | Borrador móvil sin conexión | [16-pendientes.png](imgs/16-pendientes.png) |
| P17 | Equipo y permisos | Integrante de demostración y permisos por rol | [17-equipo-permisos.png](imgs/17-equipo-permisos.png) |
| P18 | Configuración y ayuda | Preferencias de organización y acceso a guías | [18-configuracion.png](imgs/18-configuracion.png) |

## 5. Especificación por pantalla

### P01 · Acceso

**Propósito y entrada.** Dar una entrada clara a la plataforma y distinguir el acceso privado de una demostración. Es la primera pantalla al abrir la aplicación sin una sesión activa. Un enlace público de lote lleva directamente a P13.

**Composición.** Pantalla dividida: aproximadamente 45% para marca y mensaje, 55% para formulario. A la izquierda, fondo verde profundo, marca en marfil, título “Tu organización, lote a lote” y una ilustración lineal discreta de tres nodos conectados que representan entrega, lote e inventario. A la derecha, una tarjeta blanca con título “Entrar a CooperaLote”. No se muestran estadísticas comerciales ni testimonios inventados.

**Elementos y campos.** Correo electrónico, contraseña con control “Mostrar”, botón “Entrar”, enlace “Recuperar acceso” y botón secundario “Explorar demostración”. Las etiquetas permanecen visibles encima del campo. Bajo la demostración: “Recorrido con datos ficticios”. El pie contiene “Privacidad” y “Ayuda”. Los textos jurídicos definitivos deberán validarse antes de un uso real; la maqueta no inventa un aviso aprobado.

**Interacciones.** Entrar lleva a P02 si existen varias organizaciones o a P03 cuando sólo hay una. La demostración entra al contexto ficticio con su distintivo permanente. Recuperar acceso abre un diálogo con correo y acción “Enviar instrucciones”; la respuesta es neutral: “Si el correo está registrado, recibirás instrucciones”. Al enviar, el botón indica progreso y no admite pulsaciones repetidas.

**Estados.** Credenciales no aceptadas: mensaje general encima del formulario sin revelar qué dato falló. Sin conexión: aviso visible con reintento; no se promete abrir una sesión nueva. Sesión expirada: se vuelve a esta pantalla con explicación breve y retorno a la tarea cuando sea posible. Privacidad y ayuda se leen en paneles accesibles.

**Móvil y salida.** Una columna: marca, mensaje corto y formulario. Se elimina el bloque ornamental amplio. El teclado no oculta el botón. La salida habitual es P02 o P03. La imagen muestra la versión de escritorio con campos vacíos.

### P02 · Seleccionar organización

**Propósito y entrada.** Establecer de forma inequívoca en qué organización trabajará la persona. Se abre después del acceso o desde el selector de organización de la barra superior.

**Composición.** Encabezado “Elige tu organización”, texto “Trabaja con los registros de una organización a la vez” y tarjetas de igual tamaño en una retícula. Cada tarjeta contiene iniciales o símbolo, nombre, municipio, rol del usuario y botón “Abrir organización”. La tarjeta Demo del Mayab tiene un borde verde discreto cuando está seleccionada.

**Elementos.** Buscador por nombre, etiquetas “Demostración” y rol, tarjeta Demo del Mayab en Othón P. Blanco y tarjeta Demo Costa sin registros. No hay un resumen que sume las existencias de ambas. En el encabezado se mantiene el menú del usuario para cerrar sesión. La creación de organización aparece sólo en el recorrido habilitado para quien pueda realizarla.

**Alta como estado de esta pantalla.** “Crear organización” abre un panel con nombre, municipio, entidad, nombre público autorizado y preferencias iniciales. El panel distingue campos de uso interno y datos que podrían compartirse; por defecto no publica información. Guardar conduce al inicio vacío de la organización recién creada. Se conserva el nombre completo aunque se abrevie en la barra superior.

**Interacciones y estados.** Al cambiar con una captura abierta se ofrecen “Guardar borrador”, “Descartar cambios” y “Seguir aquí”. Los borradores quedan asociados a la organización de origen. Si no hay acceso a ninguna, se muestra “Todavía no tienes una organización asignada” y la ruta de ayuda; no se presenta un panel vacío como si hubiera acceso concedido. Una organización suspendida para el usuario muestra la restricción sin sus datos internos.

**Móvil y salida.** Tarjetas en una columna, botón ancho y rol siempre visible. Abrir organización lleva a P03, actualiza el contexto de toda la navegación y no conserva filtros de otra organización. La imagen representa las dos tarjetas de demostración.

### P03 · Inicio de la organización

**Propósito y entrada.** Resumir la situación operativa y ofrecer el siguiente paso sin saturar de métricas. Es la página inicial del contexto seleccionado.

**Composición.** Cabecera “Resumen de operación”, nombre de la organización y periodo “05 nov 2026”. A la derecha, botón principal “Registrar entrega”. Debajo hay cuatro tarjetas: “Recibido · 100.00 kg”, “Salidas · 20.00 kg”, “Pérdidas documentadas · 0.00 kg” y “Existencia · 80.00 kg”. Cada tarjeta indica periodo o fecha de corte; no mezcla cantidades acumuladas con existencias sin explicarlo.

**Secciones.** Un bloque ancho “Balance del periodo” presenta 100.00 = 20.00 + 0.00 + 80.00 kg, con segmentos y etiquetas. A su lado, “Por revisar” ofrece expedientes, pendientes y diferencias; si no existen, muestra “Sin pendientes en este ejemplo”. Abajo, “Actividad reciente” enumera ENT-0001, LOT-0001 y MOV-0002; “Accesos rápidos” lleva a Productores, Lotes, Inventario y Reportes.

**Detalles informativos.** “Expedientes completos · 1 de 1” incluye ayuda: origen y movimientos documentados. No usa el texto “miel certificada”. No se incluyen ingresos, ganancias, carbono evitado o crecimiento regional. Cada cifra conduce a la lista correspondiente con periodo y filtros aplicados.

**Interacciones y estados.** El selector de fechas actualiza todo el resumen y muestra el rango elegido. El estado inicial de una organización nueva ofrece tres pasos: registrar productor, capturar entrega y crear lote. Sin datos comparables no hay flechas de crecimiento. Sin conexión, una franja muestra “Vista guardada” y la hora de actualización; las cifras no se presentan como recién comprobadas.

**Móvil y salida.** Tarjetas en dos columnas o una si el texto no cabe; balance en una lista; acción de entrega al alcance del pulgar. Pulsar una actividad abre su detalle. La imagen representa el caso completo después de la salida.

### P04 · Productores

**Propósito y entrada.** Consultar el padrón y relacionar cada productor con sus entregas. Se accede desde el menú o desde la selección de productor en P06.

**Composición.** Título “Productores”, subtítulo con total, botón “Registrar productor”, búsqueda por nombre o identificador y filtro de estado. La tabla contiene Identificador, Productor, Procedencia, Entregas confirmadas, Kilogramos recibidos y Estado. La fila PR-001 muestra Productor Demo 01, Othón P. Blanco, 1 entrega y 100.00 kg.

**Ficha lateral.** Al seleccionar la fila, se abre un panel de aproximadamente 420 px con nombre, identificador, etiqueta Activo y procedencia general. Incluye pestañas “Resumen”, “Entregas” e “Historial”. El resumen muestra la fecha de alta y campos opcionales de contacto sólo para los perfiles autorizados. En la maqueta no se exhiben teléfonos, domicilio exacto, documentos oficiales ni datos bancarios. En entregas aparece ENT-0001 y un enlace al lote asociado.

**Alta y edición.** El mismo panel cambia a formulario: nombre o denominación, identificador visible, municipio, localidad opcional, estado y notas internas. Un contacto opcional se separa visualmente de los datos de procedencia. La ayuda explica que esos datos no se comparten por QR. Los campos mínimos propuestos son nombre y municipio; el identificador se presenta claramente al guardar. Se advierte una posible coincidencia antes de duplicar un productor.

**Interacciones y estados.** Guardar muestra confirmación y actualiza el padrón. “Registrar entrega” dentro de la ficha abre P06 con productor seleccionado. “Archivar productor” requiere confirmar y explica que sus entregas permanecen en el historial. Un productor archivado se ve con etiqueta y no aparece como selección principal para nuevas entregas. Sin coincidencias se ofrece limpiar filtros; sin productores se ofrece crear el primero.

**Móvil y salida.** La ficha ocupa todo el ancho como panel con botón “Volver al padrón”; la lista se representa con tarjetas. La imagen muestra el padrón y la ficha de PR-001 abierta en Resumen.

### P05 · Entregas

**Propósito y entrada.** Revisar recepciones, distinguir borradores de registros confirmados y abrir el siguiente paso hacia un lote. Se accede desde menú, inicio o ficha del productor.

**Composición.** Título “Entregas”, acción “Registrar entrega” y barra de búsqueda. Filtros por periodo, productor, estado y asociación a lote. Debajo, contadores separados: Confirmadas, Borradores y Pendientes. Los kilogramos resumidos corresponden únicamente a entregas confirmadas.

**Tabla y detalle.** Columnas: Folio, Fecha, Productor, Cantidad, Estado y Lote. La fila ENT-0001 contiene 05 nov 2026, Productor Demo 01, 100.00 kg, Confirmada y LOT-0001. Al abrirla aparece un panel con identificación, cantidad recibida, procedencia, notas, documento, responsable y fecha de confirmación. Los enlaces llevan a la ficha del productor, evidencia y detalle del lote.

**Acciones.** Un borrador permite “Continuar captura”; una entrega confirmada aún no asignada ofrece “Crear lote” o “Vincular a lote” con la cantidad disponible; una entrega ya asignada ofrece “Ver lote”. Si una entrega se reparte entre varios lotes, el panel enumera cada aportación y la cantidad restante, sin duplicar la recepción. “Solicitar corrección” pide motivo y muestra el valor anterior y el propuesto.

**Estados y validación visible.** Los borradores y pendientes llevan una nota “No incluido en inventario”. Una corrección no reemplaza silenciosamente el valor original. Falta de evidencia se muestra como pendiente documental, separado del estado de captura. La interfaz no infiere rechazo físico de la miel a partir de un archivo ausente. Un intento de confirmar dos veces conserva el mismo folio y no muestra una segunda entrada.

**Móvil y salida.** Cada tarjeta tiene folio, cantidad grande, productor, fecha, estado y acción. Al cerrar el detalle se mantiene la posición en la lista. La imagen muestra ENT-0001 confirmada y su resumen.

### P06 · Registrar entrega

**Propósito y entrada.** Capturar una recepción con pocos pasos y suficiente claridad para uso en campo. Se abre desde P03, P04 o P05.

**Composición.** Diseño prioritariamente móvil con encabezado “Registrar entrega”, botón Volver y franja de organización/demostración. Tres secciones numeradas, visibles en un desplazamiento vertical: 1. Productor; 2. Recepción; 3. Evidencia. Se evita un asistente que obligue a cambiar de página para cada dato.

**Campos.** Productor obligatorio, seleccionado mediante búsqueda por nombre o folio; fecha y hora de recepción obligatorias; cantidad recibida obligatoria con sufijo fijo “kg”; procedencia general recuperada del productor, editable si corresponde a esta entrega; referencia de cosecha o apiario opcional; notas internas opcionales. La evidencia ofrece “Tomar foto” y “Adjuntar archivo”, con nombre, tamaño y opción Quitar antes de confirmar. La referencia de apiario no obliga a capturar coordenadas privadas.

**Ayudas.** Bajo cantidad: “Registra el peso neto recibido”. La ficha compacta del productor muestra PR-001 y municipio para evitar confusiones. Un resumen al pie muestra “Productor Demo 01 · 100.00 kg · 05 nov 2026”. La falta de un archivo se indica como pendiente documental cuando la política de la organización lo permita; nunca se rellena con un comprobante inexistente.

**Acciones y flujo.** “Guardar borrador” es secundaria; “Revisar entrega” abre un resumen con campos, documento y acción final “Confirmar entrega”. Tras confirmar: folio ENT-0001, estado y opción “Crear lote” hacia P07. La confirmación de la entrega no se representa por sí sola como una segunda entrada de inventario al crear el lote: ambos pasos forman una única recepción trazable.

**Errores y conectividad.** Cantidad vacía, cero o negativa impide continuar; fecha no válida y productor no seleccionado se marcan junto al campo. Sin conexión, la acción se llama “Guardar pendiente” y el mensaje explica “Todavía no afecta el inventario”. Al volver a tener conexión, se revisa en P16. Cerrar con cambios ofrece conservar el borrador. No se muestra Confirmada mientras siga pendiente.

**Imagen.** Captura móvil con PR-001, 100.00 kg, fecha de ejemplo y comprobante-demo.pdf, antes de revisar. En escritorio el formulario ocupa dos tercios y el resumen queda en una columna lateral.

### P07 · Lotes y creación de lote

**Propósito y entrada.** Localizar lotes y agrupar sus aportaciones sin perder la relación con entregas u otros lotes. Se accede desde el menú o desde una entrega confirmada.

**Composición.** Título “Lotes”, buscador por folio, filtros de fecha, condición y documentación; acción “Crear lote”. Tabla con Lote, Producto, Fecha, Orígenes, Entrada registrada, Existencia y Condición. En la vista terminada LOT-0001 tiene una entrega de origen, 100.00 kg de entrada y 80.00 kg de existencia.

**Panel de creación.** Se abre al costado o a pantalla completa en móvil. Contiene producto, fecha, referencia interna opcional y tabla “Aportaciones de origen”. Cada fila permite elegir una entrega confirmada o un lote disponible, ver su cantidad utilizable y especificar cuánto se aporta. Se muestra un total grande y una explicación: “Las aportaciones conservan su origen”. El producto de ejemplo es “Miel de abeja”. La condición inicial propuesta es “En revisión”; una condición distinta requiere la acción autorizada de la organización.

**Reglas visibles.** No se permite usar más de la cantidad disponible ni aportar desde el mismo lote que se está creando. Un mensaje evita relaciones circulares: “Este origen ya depende del lote seleccionado”. Si se crea un lote derivado, se muestran las cantidades que salen de sus orígenes y llegan al nuevo lote; esas transferencias no se presentan como nueva recepción externa. Crear un lote con una entrega ya registrada no vuelve a sumar sus kilogramos al balance general.

**Acciones y estados.** “Revisar lote” muestra una confirmación con aportaciones, total y procedencia. “Crear lote” abre P08. Si cambió la disponibilidad mientras se llenaba, el panel conserva la captura, indica la nueva cantidad y solicita revisar. Borradores y registros sin origen completo se identifican sin inventar vínculos. El detalle permite archivar un lote sin ocultar movimientos históricos; no hay eliminación silenciosa.

**Imagen.** Representa el instante previo a crear LOT-0001: lista todavía vacía y panel con ENT-0001, cantidad disponible 100.00 kg y aportación 100.00 kg. No debe mostrar ese mismo lote ya creado detrás del panel. La lista posterior se consulta en P08/P09.

### P08 · Detalle del lote y trazabilidad

**Propósito y entrada.** Responder qué contiene el lote, de dónde viene, qué movimientos tuvo y cuánto queda. Se abre desde listados, inventario, entregas o enlaces internos de origen.

**Composición.** Ruta “Lotes / LOT-0001”, título “LOT-0001”, producto y etiquetas separadas de condición, integridad documental y visibilidad pública. Acciones “Registrar movimiento” y “Compartir lote”. Primera fila con Entrada 100.00 kg, Salidas 20.00 kg, Pérdidas 0.00 kg y Existencia 80.00 kg.

**Pestañas.** “Resumen”, “Origen”, “Movimientos”, “Evidencias” e “Historial”. Resumen muestra fecha, organización, procedencia general, responsable y último movimiento. Origen presenta un recorrido de izquierda a derecha: PR-001 → ENT-0001, 100.00 kg → LOT-0001 → salida de 20.00 kg y existencia de 80.00 kg. Las flechas llevan cantidades. Los nodos abren registros concretos.

**Genealogías ampliadas.** Si hay mezclas o divisiones, cada origen se presenta con su aportación y cada destino con su cantidad. Una vista “Lista de aportaciones” reproduce la información para pantallas pequeñas y lectura accesible. El total del lote no suma nuevamente sus antecesores. Se distingue la salida a un lote derivado de la salida fuera de la organización.

**Condición y evidencia.** Un panel permite al perfil autorizado registrar “En revisión”, “Disponible”, “Bloqueado” o “Cerrado”, con motivo, fecha y documento cuando corresponda. La ayuda dice “Condición registrada por la organización”. El cierre exige saldo cero o una explicación/corrección trazable; no desaparece un saldo por cambiar la etiqueta. Un bloqueo muestra el motivo y limita las acciones compatibles.

**Estados.** Origen incompleto: advertencia localizada y acceso para completar la relación; movimiento pendiente: no modifica cifras confirmadas. Lote inexistente o sin permiso: pantalla neutral sin exponer contenido. Las correcciones remiten a Historial. En móvil, el balance se apila y el origen se muestra verticalmente.

**Imagen y salida.** La imagen muestra la pestaña Origen y el balance final del caso. “Registrar movimiento” lleva a P10; “Compartir lote” a P12; Evidencias a P11 filtrada por LOT-0001.

### P09 · Inventario y movimientos

**Propósito y entrada.** Consultar existencias confirmadas y conciliar entradas, salidas y pérdidas del periodo. Se accede desde el menú o desde una cifra del inicio.

**Composición.** Título “Inventario”, fecha de corte y botones “Registrar movimiento” y “Exportar”. Tarjetas de saldo inicial, entradas, salidas, pérdidas y saldo final. Para el ejemplo: 0.00, 100.00, 20.00, 0.00 y 80.00 kg, respectivamente. Una banda resume “Balance conciliado” porque las cantidades cuadran; no lo denomina certificación.

**Secciones.** Pestañas “Existencias por lote” y “Movimientos”. La primera tabla muestra LOT-0001, Miel de abeja, 80.00 kg, condición y última actualización. La segunda muestra MOV-0001, entrada 100.00 kg, y MOV-0002, salida 20.00 kg, con fecha, referencia, responsable y saldo posterior de 100.00 y 80.00 kg. Los signos y nombres ayudan a distinguir entradas y salidas.

**Filtros.** Periodo, lote, producto, tipo de movimiento y condición. Una búsqueda por folio abre el lote. El subtotal indica “Resultados filtrados” cuando no representa toda la organización. En las transferencias internas, se muestran origen y destino como pareja vinculada y un efecto neto general de cero.

**Conciliación.** Si se registra un conteo físico, se presenta en un panel con fecha, responsable, existencia registrada, cantidad observada y diferencia. Una discrepancia aparece como “Diferencia por revisar”; no se transforma automáticamente en pérdida. Para resolverla se requiere una corrección o pérdida documentada mediante P10, con motivo y referencia.

**Estados e interacción.** Se evita confundir cero existencias con información no cargada. Sin conexión, aparece la fecha de la última vista guardada. Los movimientos pendientes se consultan aparte y no se incluyen en el saldo confirmado. “Exportar” abre P14 conservando el periodo y filtros. En móvil se prioriza existencia por lote, con movimientos desplegables.

**Imagen.** Balance final y tabla de los dos movimientos. No incluye entradas duplicadas por la creación de LOT-0001.

### P10 · Registrar movimiento

**Propósito y entrada.** Registrar una variación o transferencia con su explicación y efecto visible antes de confirmarla. Se abre desde un lote o desde inventario.

**Composición.** Encabezado “Registrar movimiento”, selector del tipo y formulario a la izquierda; tarjeta de resumen a la derecha. Para el recorrido central: tipo “Salida”, lote LOT-0001 y saldo actual previo de 100.00 kg. No se muestra el saldo final de P09 como saldo inicial de esta captura.

**Campos.** Tipo, lote, fecha/hora, cantidad en kg, motivo, referencia o destino descriptivo y comprobante. El motivo es obligatorio para salidas, pérdidas y correcciones. Las entradas de recepción se registran desde Entregas, con un enlace a P06; no se ofrece repetir manualmente la misma recepción. Los tipos propuestos son Salida, Transferencia interna, Pérdida documentada y Corrección autorizada.

**Variantes.** Una transferencia solicita lote de destino y muestra ambos efectos. Una pérdida exige explicación y evidencia conforme al acuerdo de la organización; una corrección muestra el movimiento original y su efecto compensatorio. Ninguna variante borra el movimiento previo. Un destino descriptivo no crea automáticamente un cliente ni registra una venta.

**Resumen previo.** “Disponible antes · 100.00 kg”, “Salida propuesta · 20.00 kg”, “Saldo resultante · 80.00 kg”. Debajo: motivo “Salida de ejemplo” y distintivo de demostración. La operación se revisa mediante “Revisar movimiento” y se confirma después con lote, cantidad y consecuencia explícitos. Tras confirmar, se muestra MOV-0002 y enlaces a lote e inventario.

**Validaciones y estados.** Cantidades no positivas, saldo insuficiente, lote bloqueado o permiso faltante muestran explicación y no permiten confirmar. Si la disponibilidad cambió, se conserva la captura y se pide revisar el nuevo saldo. Sin conexión puede guardarse un borrador donde la propuesta lo permita, pero no una salida definitiva. El resumen entonces se llama “Estimación con la última información disponible”.

**Móvil e imagen.** La tarjeta de efecto se coloca debajo de cantidad y antes de las acciones fijas. La imagen de escritorio muestra 20.00 kg de salida antes de la confirmación y un saldo proyectado de 80.00 kg.

### P11 · Evidencias y revisión documental

**Propósito y entrada.** Encontrar documentos vinculados a productores, entregas, lotes o movimientos, y reconocer qué falta revisar. Se abre desde menú o con un filtro heredado de un registro.

**Composición.** Título “Evidencias”, acción “Adjuntar evidencia”, filtros por tipo, registro vinculado, fecha y estado. Tabla con Archivo, Tipo, Vinculado a, Fecha, Aportado por, Revisión y Visibilidad. La imagen muestra comprobante-demo.pdf vinculado a ENT-0001 y LOT-0001, con distintivo “Privado”.

**Panel de documento.** Al seleccionarlo aparece una vista previa o icono de archivo, nombre, descripción, fecha del documento, autor de la carga y vínculos. La previsualización de la maqueta se marca “Documento de ejemplo” y no imita firmas o documentos oficiales. Los botones son “Abrir”, “Descargar” y, para perfiles autorizados, “Registrar revisión”.

**Carga.** Panel con selector de registro, tipo documental, fecha, descripción y área para elegir o arrastrar un archivo. Propuesta inicial de interfaz: PDF, JPG o PNG y hasta 10 MB por archivo, límite a validar durante el diseño del producto. La pantalla informa estos límites antes de seleccionar. Muestra progreso individual y permite reemplazar una selección aún no confirmada.

**Revisión.** Estados propuestos: Pendiente de revisión, Revisado y Requiere corrección. El formulario de revisión pide observación, responsable y fecha. “Revisado” significa revisión documental registrada por la organización, no aprobación sanitaria o certificación automática. Una nueva versión conserva referencia a la anterior y explica el motivo de sustitución.

**Estados y privacidad.** Archivo no compatible, excede el tamaño, carga interrumpida o documento no disponible tienen mensajes distintos. Sin permiso no se revela la vista previa. La carga de un documento nunca lo publica en el QR. Los faltantes se muestran como lista de pendientes vinculada al registro, no como evidencia creada.

**Móvil y salida.** Lista de tarjetas con archivo, vínculo y estado; panel de detalle completo. Volver regresa al registro de origen y conserva el filtro. La imagen muestra el archivo seleccionado y su revisión pendiente.

### P12 · Compartir lote y preparar QR

**Propósito y entrada.** Decidir qué información mínima del lote podrá consultarse públicamente y previsualizarla. Se abre únicamente desde P08 mediante “Compartir lote”.

**Composición.** Dos columnas. Izquierda: “Información pública de LOT-0001”, selector de visibilidad y campos de publicación. Derecha: tarjeta de vista previa con marca, producto, folio público, procedencia general y un recuadro QR. El recuadro de la imagen lleva “QR ilustrativo · No escaneable”; no se presenta como código funcional.

**Contenido seleccionable.** Identificador público, producto y denominación pública de la organización; procedencia general autorizada; fecha o periodo autorizado; descripción breve de origen documentado. La vista previa no muestra teléfonos, domicilios, coordenadas de apiarios, identidad personal del productor, contactos, cantidades internas, costos, documentos privados o nombres de usuarios.

**Controles.** Visibilidad “No publicado / Publicado”, lista de campos con selección explícita y un aviso permanente “Comparte sólo la información autorizada”. El administrador revisa la vista antes de “Publicar vista”. Las acciones posteriores son “Abrir vista pública”, “Copiar enlace”, “Descargar QR” y “Retirar publicación”, siempre sujetas al permiso correspondiente.

**Flujo y confirmaciones.** Publicar solicita confirmar organización, lote y campos visibles. Retirar publicación explica que el enlace dejará de mostrar los datos y pedirá confirmación. Actualizar un campo requiere revisar la nueva vista. Un cambio pendiente no aparece como ya publicado. En la maqueta todas estas acciones son representaciones estáticas.

**Estados.** Lote sin información pública suficiente: lista de campos por completar. Sin permisos: vista de consulta sin controles de publicación. Sin conexión: publicación deshabilitada y explicación. Lote con alerta de la organización: se muestra el mensaje público autorizado si existe; la aplicación no inventa un dictamen de calidad.

**Móvil e imagen.** Campos arriba y vista previa abajo, con botón de revisión al final. La imagen representa el estado “No publicado”, campos permitidos seleccionados y previsualización de P13. La publicación visual debe distinguirse de un etiquetado comercial completo.

### P13 · Consulta pública del lote

**Propósito y entrada.** Permitir que una persona consulte la información autorizada del lote sin cuenta. Entrada desde QR, enlace compartido o vista previa. Esta pantalla no contiene menú interno ni selector de organización.

**Composición.** Diseño móvil de una columna, fondo marfil, marca CooperaLote arriba y franja “Demostración · Datos ficticios”. Una tarjeta principal muestra “Conoce el origen de este lote”, “Miel de abeja” y LOT-0001 como identificador visible de ejemplo. La jerarquía prioriza producto, procedencia y organización, no gráficos o estadísticas.

**Secciones.** “Procedencia” contiene Othón P. Blanco, Quintana Roo; “Organización” muestra Organización Demo del Mayab; “Registro del lote” muestra la fecha autorizada. “Recorrido documentado” utiliza tres pasos breves: recepción registrada, lote identificado y registro actualizado. No expone el nombre personal del productor ni los movimientos internos de 20 u 80 kg.

**Contexto de confianza.** Debajo aparece: “Información declarada por la organización. Este registro no es una certificación”. Un texto breve explica que el QR permite consultar la información compartida. No hay etiquetas “orgánica”, “libre de contaminantes”, “sostenible certificada” o escudos institucionales. La fecha se presenta como actualización del registro, no como caducidad del alimento.

**Acciones.** “Copiar enlace” y “Acerca de esta consulta” son secundarias. La segunda abre una explicación de procedencia, límites y privacidad. Un vínculo de contacto sólo se incorporaría si la organización autorizara uno público; no se inventa en el ejemplo. No hay compra, precio, carrito o pago.

**Estados.** Enlace inexistente: “No encontramos este lote”; publicación retirada: “Esta información ya no está disponible”; conexión fallida: “No pudimos cargar la consulta” y Reintentar. Ninguno de estos estados muestra información privada ni transforma la ausencia de registro en afirmación sobre la calidad del producto.

**Imagen.** Versión móvil de alta fidelidad. En escritorio, la misma columna tiene un ancho máximo de aproximadamente 640 px y se centra; no se agrega navegación de administración.

### P14 · Reportes y exportación

**Propósito y entrada.** Preparar una salida legible y portable de la información de la organización. Se abre desde menú o desde una lista con filtros preseleccionados.

**Composición.** Título “Reportes”, selector de periodo y tarjetas de tipo: Balance de inventario, Entregas por productor, Trazabilidad por lote e Integridad documental. Debajo se presenta una previsualización tabular; a la derecha un panel “Preparar exportación”. La imagen usa Balance de inventario para el 05 nov 2026.

**Reporte de ejemplo.** Encabezado con organización, periodo, fecha de elaboración y distintivo de demostración. Filas o columnas muestran saldo inicial 0.00, entradas 100.00, salidas 20.00, pérdidas 0.00 y saldo final 80.00 kg. El detalle vincula LOT-0001 y sus movimientos. El resumen explica si las transferencias internas se muestran en el detalle sin incrementar la recepción externa.

**Controles.** Selección de columnas, formato CSV o PDF, incluir resumen, incluir detalle y nombre propuesto de archivo. Una casilla para información privada sólo aparece si el usuario puede exportarla y explica qué campos agregará. Los adjuntos no se incluyen automáticamente. La interfaz distingue “Previsualizar” de “Descargar”.

**Indicadores.** Integridad documental muestra numerador, denominador, periodo y criterio: 1 de 1 lotes con origen y movimientos completos. Cuando falta información, muestra ND. No se representa un 100% de cumplimiento normativo ni se transforma cobertura documental en impacto ambiental. Las metas del proyecto no se mezclan con resultados de la organización.

**Estados e interacción.** Preparando, Listo para descargar y No se pudo generar son estados claros. Un reporte vacío explica los filtros. Una vista guardada sin conexión indica fecha de corte y no permite prometer una exportación actualizada. Cambiar filtros marca la previsualización como pendiente de actualizar. La descarga conserva los rótulos de demostración.

**Móvil e imagen.** Selector, resumen y opciones en una columna; las tablas anchas ofrecen una vista resumida. La imagen muestra la previsualización del balance y el panel con PDF seleccionado. El archivo de la maqueta es ilustrativo, no un reporte real generado.

### P15 · Historial de actividad

**Propósito y entrada.** Comprender quién registró o corrigió una operación, cuándo lo hizo y con qué motivo. Se abre desde menú o desde el historial de un registro concreto.

**Composición.** Título “Historial”, filtros por fecha, tipo de registro, persona y acción; búsqueda por folio. La zona principal es una lista cronológica con icono, descripción, hora, responsable y enlace al objeto. Un panel lateral muestra el detalle del evento seleccionado.

**Secuencia ficticia.** 09:00, alta de PR-001; 09:15, confirmación de ENT-0001; 09:30, creación de LOT-0001 y entrada vinculada MOV-0001; 09:45, condición disponible registrada por Usuario Demo; 10:00, salida MOV-0002 por 20.00 kg. Se agrupan eventos relacionados para que crear un lote y reconocer la recepción no parezcan dos entradas físicas.

**Detalle.** Fecha/hora con zona, actor visible según permiso, acción, objeto, motivo y documentos relacionados. En una corrección, bloque comparativo “Antes / Después” con campos cambiados y efecto sobre la operación. El historial no ofrece editar o borrar el evento. Un enlace lleva a la acción autorizada para solicitar otra corrección.

**Interacción.** Al abrir desde un lote se muestra un filtro fijo con su folio y opción “Ver todo el historial” cuando corresponda. Exportar historial requiere permiso y respeta el alcance mostrado. Pulsar un evento conserva la posición y actualiza el panel. Se evita depender de información accesible sólo al pasar el cursor.

**Estados.** Sin eventos: explicación según filtros; evento no accesible: mensaje neutral; carga incompleta: Reintentar sin borrar la selección. Los pendientes de un dispositivo no se presentan como operaciones confirmadas del historial general; se consultan en P16.

**Móvil e imagen.** Línea de tiempo vertical y detalle desplegable de ancho completo. La imagen muestra la salida de 20.00 kg seleccionada con el enlace a LOT-0001 y MOV-0002. Las horas son parte del caso sintético.

### P16 · Pendientes de envío y revisión

**Propósito y entrada.** Dar visibilidad a capturas aún no confirmadas y resolver diferencias después de trabajar sin conexión. Se accede desde el indicador de conexión, menú Pendientes o confirmación de guardado provisional.

**Composición.** Diseño prioritariamente móvil. Cabecera “Pendientes”, banda “Sin conexión”, hora de última actualización y un aviso: “Tus borradores todavía no afectan el inventario”. Pestañas o filtros “Por enviar”, “Requieren revisión” y “Confirmados”. Cada tarjeta muestra tipo de captura, referencia provisional, organización, fecha, cantidad y estado.

**Ejemplo representado.** Borrador BOR-0001, entrega de ejemplo de 100.00 kg para Productor Demo 01, guardado en el dispositivo. Este es un escenario alternativo del recorrido y no una segunda entrega del inventario mostrado en otras pantallas. Se indica “Escenario sin conexión”. La tarjeta ofrece “Revisar captura” y un control deshabilitado “Enviar al recuperar conexión”.

**Estados del proceso.** Guardado en este dispositivo → Listo para enviar → Enviando → Confirmado, o Requiere revisión/Rechazado con motivo. Mientras se envía no se crean nuevas tarjetas por cada intento. La confirmación sustituye la referencia provisional por el folio definitivo y permite abrir el registro. Una repetición del envío conserva el mismo resultado.

**Conflictos.** Si cambió el saldo o el productor ya no está disponible, el panel muestra “Tu captura” y “Información actual”, la diferencia y acciones “Editar borrador” o “Descartar”. No ofrece aceptar automáticamente el último valor. Descartar solicita confirmación y explica que afecta sólo a ese borrador. Una captura rechazada conserva su motivo y no aumenta el saldo.

**Cuidado de la tarea.** Antes de cerrar sesión o cambiar de organización, se informa cuántos pendientes quedan en ese dispositivo. Los pendientes se muestran agrupados por organización y nunca se reasignan silenciosamente. La pantalla no asegura que un borrador ya esté respaldado ni disponible en otro equipo.

**Escritorio y salida.** La versión de escritorio usa tabla y panel comparativo. Desde Confirmados se abre P05 o P08. La imagen es móvil y representa un único borrador alternativo, no un envío exitoso.

### P17 · Equipo y permisos

**Propósito y entrada.** Administrar quién puede consultar y operar los registros de la organización activa. Se accede desde el bloque Organización para perfiles autorizados.

**Composición.** Título “Equipo y permisos”, nombre de organización, botón “Agregar integrante” y pestañas “Integrantes” y “Roles”. La tabla muestra nombre visible, correo, rol, estado y acciones. La maqueta usa Usuario Demo, usuario@ejemplo.invalid, Administración y Activo. No usa los nombres de los cinco integrantes del proyecto.

**Panel de permisos.** Al seleccionar un rol se abre una matriz por módulo y acción: Consultar, Capturar, Confirmar/Revisar, Exportar y Administrar. Los controles explican qué alcance concede cada selección; no se usan interruptores ambiguos. Los perfiles predefinidos son Administración, Operación, Revisión y Consulta, sujetos a validación organizativa.

**Alta.** “Agregar integrante” abre un panel con nombre, correo, rol y resumen de permisos. La propuesta admite una invitación con estado Pendiente; enviar una invitación sería una acción explícita en el producto, no algo realizado por esta maqueta. Una confirmación muestra a qué dirección se enviará y para qué organización. No se solicitan cuentas bancarias, CURP o documentos de identidad para este ejemplo.

**Cambios.** Modificar rol muestra permisos que se agregan o retiran antes de guardar. Suspender acceso pide confirmar y conserva la atribución de actividades anteriores. La pantalla evita dejar a la organización sin un administrador activo y explica el motivo. Un integrante suspendido se distingue de una invitación aún no aceptada.

**Estados.** Correo con formato inválido, integrante ya existente, permisos insuficientes y cambios sin guardar tienen mensajes específicos. Un usuario de consulta no ve controles administrativos de otras personas. La configuración de esta organización no afecta a la segunda organización de demostración.

**Móvil e imagen.** Tarjetas de integrantes y permisos como listas por módulo. La imagen muestra un único integrante y la matriz de roles, sin fingir que ya se enviaron invitaciones reales.

### P18 · Configuración de organización y ayuda

**Propósito y entrada.** Ajustar la identidad visible, preferencias operativas y ayudas de uso de la organización. Se accede desde el menú; la ayuda también desde la barra superior.

**Composición.** Título “Configuración”, pestañas “Organización”, “Preferencias” y “Ayuda”. En Organización se muestran nombre interno, nombre público autorizado, municipio y entidad. Una tarjeta lateral resume cómo aparecerá el contexto en la barra superior. Debajo, texto que aclara que los datos públicos de cada lote se seleccionan en Compartir lote.

**Preferencias.** Idioma Español, zona horaria Quintana Roo, unidad base kg y precisión visual de dos decimales. La política de documentación muestra los tipos de evidencia solicitados y su carácter obligatorio u opcional, siempre como propuesta acordable. Los cambios en nombres y preferencias no reescriben sin explicación los registros históricos. Cambiar una unidad de presentación no convierte cantidades ni altera balances por sí solo.

**Perfil personal.** El avatar permite abrir un panel con nombre visible, correo, preferencias de lectura y cierre de sesión. La configuración de organización y la personal están rotuladas por separado. Antes de cerrar se avisa de borradores pendientes en el dispositivo, con acceso a P16.

**Ayuda.** Tarjetas de guía: “Registrar una entrega”, “Seguir el origen de un lote”, “Entender el inventario”, “Trabajar sin conexión” y “Compartir información por QR”. Cada guía abre un panel con pasos numerados, vocabulario sencillo y enlaces a la pantalla relevante. Incluye una leyenda de estados y la explicación de los distintivos de demostración. No se muestra un número de soporte, correo comercial o tiempo de respuesta que aún no esté definido.

**Acciones y estados.** “Guardar cambios” muestra qué sección se guardó; “Cancelar” restaura la última versión visible. Si falta un dato obligatorio se señala junto al campo. Los usuarios sin permiso ven una ficha de consulta o sólo Ayuda, según su acceso. Un error conserva la edición. No hay opciones de suscripción, cobro o compra de planes en el alcance inicial.

**Móvil e imagen.** Pestañas desplazables con títulos cortos y formulario en una columna. La imagen muestra Organización/Preferencias y un bloque de guías accesibles; los paneles de ayuda se consideran estados de esta pantalla.

## 6. Recorridos completos

### A. Demostración principal de cinco minutos

1. P01: elegir “Explorar demostración”; P02: abrir Organización Demo del Mayab.
2. P03: mostrar el inicio vacío; P04: registrar Productor Demo 01. El distintivo de demostración permanece visible.
3. P06: capturar 100.00 kg, revisar y confirmar ENT-0001; P05 muestra la entrega confirmada.
4. P07: crear LOT-0001 con la aportación completa de ENT-0001. P08 muestra su origen; P09 reconoce una única entrada de 100.00 kg.
5. P10: registrar salida de 20.00 kg. Revisar el efecto 100.00 − 20.00 = 80.00 kg y confirmar MOV-0002.
6. P09: comprobar el saldo de 80.00 kg; P08: consultar el origen y movimientos.
7. P12: revisar los datos autorizados de la vista pública; P13: mostrar cómo la verá un visitante. En estas imágenes el QR es ilustrativo.
8. P14: previsualizar una exportación con los mismos números. Indicar que las imágenes son una propuesta estática y no una aplicación navegable.

### B. Captura con conectividad limitada

P06 sin conexión → Guardar pendiente → P16 Por enviar → recuperar conexión → revisar/enviar → Confirmado → P05. Si existe una diferencia, P16 Requiere revisión → comparar → editar borrador → volver a revisar. Hasta la confirmación no cambian las cifras de P03/P09. La imagen P16 representa un ensayo alternativo y no se acumula al recorrido A.

### C. Revisión de un expediente

P08 Evidencias → P11 documento vinculado → registrar observación → volver al lote → P15 consultar quién y cuándo revisó. Un documento revisado no modifica por sí solo la condición del producto. Si se necesita una corrección de cantidad, se hace mediante la acción autorizada con motivo, y el historial conserva ambos valores.

### D. Publicación y retirada de una consulta

P08 Compartir lote → P12 seleccionar información mínima → previsualizar → confirmar publicación → P13. Para retirar: P12 Retirar publicación → confirmar → la vista pública muestra que la información ya no está disponible. El visitante nunca entra a las pantallas internas.

### E. Conciliación y diferencias

P09 comparar existencia registrada y conteo → diferencia por revisar → investigar movimientos/evidencias en P08/P11/P15 → registrar corrección o pérdida justificada en P10 → revisar nuevo balance → P14 exportar. No se llama merma a una diferencia cuya causa todavía se desconoce.

### F. Cambiar organización

Selector superior → comprobar cambios sin guardar y pendientes → P02 elegir otro contexto → P03 de esa organización. El nombre activo cambia antes de continuar. No se muestran registros, archivos, exportaciones ni saldos de la organización anterior.

## 7. Estados transversales y textos orientativos

| Situación | Mensaje visible propuesto | Acción disponible |
|---|---|---|
| Organización sin actividad | “Empieza registrando tu primer productor” | Registrar productor |
| Filtros sin coincidencias | “No encontramos registros con estos filtros” | Limpiar filtros |
| Captura provisional | “Guardado en este dispositivo. Aún no afecta el inventario” | Ver pendientes |
| Conexión recuperada | “Hay capturas listas para revisar y enviar” | Revisar pendientes |
| Saldo insuficiente | “La cantidad supera la existencia disponible” | Editar cantidad |
| Disponibilidad cambió | “El saldo cambió. Revisa tu movimiento antes de continuar” | Revisar diferencia |
| Registro confirmado | “Entrega ENT-0001 confirmada: 100.00 kg” | Crear lote / Ver entrega |
| Archivo faltante | “Todavía no se ha adjuntado esta evidencia” | Adjuntar evidencia |
| Permiso insuficiente | “Tu perfil no permite realizar esta acción” | Volver / Ver ayuda |
| Carga fallida | “No pudimos cargar la información” | Reintentar |
| Cambios sin guardar | “Tienes cambios sin guardar” | Guardar borrador / Descartar / Seguir aquí |
| Información no disponible | “No hay datos suficientes para calcular este indicador” | Ver criterio |
| QR retirado | “Esta información ya no está disponible” | Acerca de esta consulta |

Las advertencias se sitúan cerca de la tarea afectada. Los mensajes de conectividad permanecen mientras dure la situación. El estado “Sin datos” se usa sólo cuando la consulta terminó correctamente y no hay registros.

## 8. Correspondencia con la documentación y ampliaciones

| Necesidad documental | Pantallas que la cubren |
|---|---|
| Organización y usuarios | P01, P02, P17, P18 |
| Padrón y entregas | P04, P05, P06 |
| Lotes y genealogía | P07, P08 |
| Inventario, movimientos y cantidades coherentes | P03, P09, P10 |
| Evidencias y revisión atribuida a la organización | P08, P11, P15 |
| Consulta pública mínima por QR | P12, P13 |
| Historial y exportación | P14, P15 |
| Captura provisional y revisión de conflictos | P06, P16 |
| Legibilidad, capacitación y evaluación de tareas | Todas; guías en P18 |
| Separación de datos ficticios y resultados reales | Distintivos en todas las vistas y exportaciones |

Si se validan necesidades posteriores, se diseñarán pantallas nuevas de costos por lote, ventas y liquidaciones, conservando la relación con los registros de la organización. Sus imágenes no forman parte de este alcance porque todavía no existe definición aprobada de esos flujos. Los escenarios de adopción del proyecto son herramientas de planificación; no se convierten en una pantalla de predicción ni en promesas de ahorro dentro del producto.

## 9. Criterios para revisar las maquetas

- Existen 18 imágenes, una por pantalla del inventario, con nombres coincidentes y enlaces desde este documento.
- Las pantallas internas muestran organización activa y contexto de demostración; la pública conserva el rótulo de datos ficticios.
- El caso principal conserva 100.00 kg recibidos, 20.00 kg de salida, 0.00 kg de pérdidas y 80.00 kg finales. P06/P07/P10 son instantes previos; P16 es un escenario alternativo.
- Crear lote o recorrer antecesores no duplica entradas. Los borradores no se suman a existencias confirmadas.
- El QR público no muestra datos personales, archivos privados o cantidades internas. El patrón de QR de la imagen se identifica como ilustrativo y no escaneable.
- La navegación principal, los nombres de acciones y los estilos conservan coherencia. P06/P13/P16 se representan en móvil; las otras pantallas se representan en escritorio y describen su adaptación.
- Las imágenes permiten entender jerarquía, distribución y apariencia. Los estados alternativos, validaciones y acciones se especifican en el texto; no se afirma que una imagen estática permita ejecutarlos.
- Este documento es la referencia para textos, reglas y estados. Las imágenes generadas sirven como referencia de composición; cualquier abreviatura o variación tipográfica debe cotejarse con la especificación al implementar.

Los prompts de generación y la relación de archivos se conservan en [prompts-imagenes.json](prompts-imagenes.json). Las 18 imágenes se generaron con la herramienta integrada de generación de imágenes y están alojadas en `mockups/imgs`. La [galería local](galeria.html) permite compararlas y abrir cada archivo a tamaño completo.

En algunas imágenes se explora el acento miel en botones de captura o preparación; la especificación de componentes establece el verde como opción base de acción principal. Las dimensiones del lienzo descritas son referencias para el diseño adaptable, no una afirmación sobre la resolución exacta de los PNG. La revisión visual cubre legibilidad general, contenido esencial, balance del ejemplo y separación entre información privada y pública; no sustituye la prueba de accesibilidad o interacción de una aplicación implementada.
