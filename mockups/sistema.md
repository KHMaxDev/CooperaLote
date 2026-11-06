# CooperaLote · Interfaz y experiencia de usuario v2

Versión 2.0 · 5 de noviembre de 2026 · Especificación visual y de interacción.

## 1. Para quién diseñamos

CooperaLote está dirigido a productores independientes, productores integrantes de organizaciones y organizaciones dedicadas a recibir, administrar y comercializar productos apícolas. Su interfaz debe responder a las tareas de esas personas: registrar producción, preparar entregas, conocer existencias, vender y consultar sus registros.

**Administrador es una responsabilidad adicional, no el usuario universal del producto.** Las imágenes v1 mostraban principalmente la operación interna de una organización con permisos amplios. Faltaba representar un espacio propio del productor y un recorrido comercial. Esta versión corrige esa orientación.

Una misma persona puede producir, vender y administrar su espacio. No necesita cuentas distintas para cada tarea. Un productor integrante, en cambio, no debe ver automáticamente los inventarios colectivos, contactos o ventas de otros miembros. Registrar a alguien en el padrón no equivale a otorgarle acceso al sistema.

### Alcance y fuentes

Se conservan como antecedentes el [documento maestro](../docs/documento_maestro_cooperalote.md), las [decisiones](../docs/decisiones.md) y el [prototipo](../docs/prototipo.md). El equipo de CooperaLote ofrece el producto digital; sus usuarios producen y comercializan.

Este replanteamiento incorpora **diseño del espacio del productor y del recorrido comercial**. Amplía la propuesta visual anterior, que posponía ventas; no afirma que las funciones estén implementadas ni modifica por sí mismo el calendario del proyecto. El diseño distingue:

- Base operativa: productores, entregas, lotes, inventario, documentos, historial y QR.
- Experiencia del productor: producción propia, entregas a organizaciones y consulta de sus registros.
- Experiencia comercial: clientes, pedidos, preparación, salidas vinculadas y cobros registrados.
- Gestión del espacio: integrantes, permisos y preferencias.

El seguimiento comercial registra operaciones declaradas por los usuarios. No incorpora transferencias bancarias, facturación fiscal, contabilidad integral ni cálculo automático de liquidaciones. Una entrega recibida no se interpreta automáticamente como compra o deuda con el productor.

### Situación de las imágenes existentes

La [especificación v1](sistema-v1.md), la [galería v1](galeria-v1.html), sus prompts y las primeras imágenes de `imgs` quedan como antecedentes. **No son las maquetas v2 ni representan sus nuevos perfiles.** La [galería vigente](galeria.html) presenta la nueva serie organizada por productor, organización y ventas. Las imágenes seleccionadas se alojan en `imgs/v2/` y su cobertura exacta se documenta en la [matriz v2](cobertura-v2.md).

## 2. Espacios, perfiles y navegación

| Persona / responsabilidad | Alcance de información | Tareas principales | Menú de entrada |
|---|---|---|---|
| Productor integrante | Registros propios y aportaciones compartidas expresamente | Declarar producción, preparar entregas y consultar recepción | Mi resumen, Mi producción, Mis entregas, Mis documentos |
| Productor independiente | Producción, existencias y ventas de su espacio | Producir, controlar inventario, vender y registrar cobros | Mi resumen, Producción, Inventario, Ventas |
| Operación de organización | Registros operativos autorizados de esa organización | Recibir entregas, formar lotes y registrar movimientos | Resumen, Productores, Entregas, Lotes, Inventario |
| Comercial | Clientes, disponibilidad y operaciones comerciales autorizadas | Preparar pedidos, coordinar entregas y registrar cobros | Resumen comercial, Clientes, Pedidos, Disponibilidad |
| Revisión | Registros y evidencias autorizados | Revisar documentación, diferencias y trazabilidad | Por revisar, Lotes, Evidencias, Historial |
| Administración del espacio | Configuración y accesos; otras tareas sólo según permiso | Asignar responsabilidades y preferencias | Equipo y permisos dentro de Configuración |
| Visitante | Información pública mínima | Consultar procedencia por QR | Vista pública sin navegación interna |

### Contexto siempre visible

La cabecera identifica “Mi producción · Productor Demo 01” o “Organización Demo del Mayab”. Cambiar de espacio cambia claramente los registros y nunca agrega saldos de diferentes organizaciones. El usuario puede tener varias responsabilidades, pero el menú conserva un orden estable y sólo muestra las tareas habilitadas.

En el primer ingreso se pregunta qué necesita hacer: registrar producción propia, gestionar recepciones o gestionar ventas. Esa selección orienta el recorrido; **no concede permisos sobre una organización**. Participar requiere una vinculación o invitación explícita. Trabajar independientemente crea un espacio propio y no obliga a inventar una cooperativa.

Un productor puede consultar sus entregas agrupadas por destinatario. En un lote colectivo ve su aportación y los datos compartidos, no automáticamente identidades, contactos, cobros o aportaciones de otras personas. Su inventario propio y el de la organización no pueden presentar simultáneamente una misma entrega confirmada como disponible para vender.

## 3. Sistema de diseño único

### Biblioteca centralizada

Las maquetas v2 se construyen desde una plantilla maestra y una biblioteca de componentes. Una futura implementación puede expresar estas reglas mediante un tema de Tailwind CSS, coherente con el antecedente del proyecto. No se mezclan apariencias de Bootstrap y Tailwind ni se eligen estilos de botones por pantalla.

La biblioteca define variables de color, tipografía, espacio, bordes y estados; cada componente tiene un contrato visual y de comportamiento. Una imagen generada no puede redefinir esas reglas. El uso de una biblioteca tampoco demuestra accesibilidad por sí solo.

### Variables visuales

| Variable | Valor | Aplicación |
|---|---|---|
| Fondo | `#F8F6EF` | Marfil general |
| Superficie | `#FFFFFF` | Tarjetas y formularios |
| Principal | `#163C35` | Texto principal, títulos y botones |
| Secundario | `#52635D` | Ayudas y metadatos |
| Acento decorativo | `#B47C24` | Marca y detalles; no botones con texto blanco |
| Aviso | Fondo `#FFF3D6`, texto `#694500` | Pendientes, siempre con icono y texto |
| Error | Fondo `#FFF1EE`, texto `#8A2E22` | Error con explicación |
| Éxito | Fondo `#E9F2EB`, texto `#163C35` | Confirmación de registro |
| Borde decorativo | `#D9DED8` | Separadores de superficies |
| Borde de control | `#6B7C73` | Reconocer campos sobre blanco |
| Foco | Verde oscuro con separación blanca | Contorno visible y continuo |

Todos los botones principales son verdes con texto blanco. Se elimina la alternancia de botones verdes y miel de las imágenes v1. La marca conserva el nombre CooperaLote y un símbolo hexagonal sencillo; no utiliza sellos institucionales ni de certificación.

Tipografía: Inter o alternativa de sistema equivalente; cuerpo 16 px, ayuda 14 px, sección 20 px y título 28–32 px. Cifras tabulares en tablas. Escala de espacios: 4, 8, 12, 16, 24, 32 y 48 px. Tarjetas con radio de 12 px; controles de 8 px. Campos y botones de al menos 48 px de alto. Áreas táctiles mínimas de 44 × 44 px como regla de producto. Sombras discretas, sin degradados ornamentales.

### Contratos de componentes

| Componente | Apariencia y comportamiento constantes |
|---|---|
| Acción principal | Verde, verbo concreto y una acción dominante por sección: Revisar entrega, Confirmar pedido |
| Acción secundaria | Fondo blanco y borde verde; Cancelar o Volver sin competir con la principal |
| Acción destructiva | Rojo, objeto y consecuencia explícitos; confirmación cuando corresponda |
| Botón ocupado | Conserva ancho; Guardando…; impide repetición y mantiene el formulario |
| Campo | Etiqueta persistente, ayuda debajo, error asociado; placeholder no sustituye etiqueta |
| Selector con búsqueda | Nombre más folio, navegación de teclado y estado sin resultados |
| Estado | Icono y palabra; mismas denominaciones en lista, detalle y reporte |
| Lista | Título, filtros, resultados, paginación; conserva posición al volver del detalle |
| Panel lateral | Consulta o edición breve; título y cierre; en móvil ocupa pantalla completa |
| Formulario extenso | Pantalla propia; no se apilan diálogos para capturar una operación |
| Confirmación | Resumen, consecuencia, Cancelar y verbo final; devuelve foco al control de origen |
| Aviso persistente | Conexión, conflicto o impedimento; permanece hasta resolver la situación |
| Resultado | Mensaje con folio y resultado; también actualiza el registro, no sólo una notificación fugaz |
| Resumen de operación | Antes → cambio propuesto → resultado; igual para cantidades e importes |
| Ayuda | En posición constante, pasos breves y ejemplo; nunca accesible sólo al pasar el cursor |

### Adaptación real a móvil

Escritorio: lateral de 232 px, cabecera de 72 px y margen de 32 px; formularios con ancho de lectura limitado. Móvil: una columna, margen de 16 px y controles amplios. No se reduce una captura de escritorio para aparentar una pantalla móvil.

Navegación inferior del productor: Inicio, Producción, Entregas, Más. Comercial: Inicio, Pedidos, Clientes, Más. Operación: Inicio, Entregas, Lotes, Más. El resto de módulos autorizados queda en Más. Dentro de un formulario se sustituye el menú inferior por sus acciones. Las barras fijas nunca ocultan el foco, el contenido final o el teclado.

Las tablas pasan a tarjetas con los mismos datos esenciales; las etiquetas de campos van arriba, no a un lado. Los diagramas tienen lista equivalente. Ruta y botón Volver conservan filtros y posición. Cambiar de espacio con edición pendiente ofrece guardar borrador, descartar o seguir editando.

## 4. Accesibilidad y prevención de errores

Referencia: [guía rápida oficial de WCAG 2.2 de W3C](https://www.w3.org/WAI/WCAG22/quickref/), objetivo nivel AA. Es una meta verificable para el producto, no una declaración de conformidad de imágenes estáticas.

Se comprobará contraste de texto de al menos 4.5:1 —3:1 para texto grande— y 3:1 para información visual necesaria en controles. La navegación debe funcionar con teclado, foco visible y no oculto. Se verificará ampliación de texto al 200% y reorganización del contenido a 320 píxeles CSS considerando las excepciones aplicables. Los lectores de pantalla deben reconocer etiquetas, encabezados, errores y mensajes de estado. El acceso debe permitir gestores de contraseñas y pegado de credenciales. La revisión incluirá pruebas manuales, no sólo comprobaciones automáticas.

Reglas de producto:

- El color no comunica por sí solo estado, selección o error. Cada indicador tiene nombre e icono cuando ayude.
- Etiquetas, orden de lectura y acciones equivalentes se mantienen entre perfiles. Los diálogos contienen el foco y lo devuelven al cerrar.
- Fecha, cantidad y destinatario se revisan juntos antes de confirmar una entrega. La unidad siempre es visible.
- Se acepta coma o punto decimal sin alterar la magnitud. Los importes muestran MXN y dos decimales.
- No exigir recapturar información ya elegida. Permitir corregirla en el resumen.
- Borrador y Confirmado son estados distintos. Guardar provisionalmente no modifica inventario o cobros confirmados.
- Reservar confirmaciones para consecuencias importantes: salida, publicación, cancelación o acceso; no interrumpir cada guardado sencillo.
- Un registro confirmado se corrige con motivo e historial. No se borra silenciosamente una entrega, salida o cobro.
- Un error conserva campos; si hay adjuntos que no pudieron conservarse, se informa cuáles volver a seleccionar.
- Sin dato no es cero. Sin denominador se muestra No calculable. Pedido, entrega y cobro tienen estados independientes.
- Todas las demostraciones y exportaciones ficticias llevan una marca visible.

## 5. Estados obligatorios

Todas las pantallas deben contar con las variantes aplicables; no basta dibujarlas llenas de datos.

| Estado | Qué ve el usuario | Acción / prevención |
|---|---|---|
| Primera vez | Explicación de la tarea, sin métricas inventadas | Crear primer registro |
| Sin coincidencias | Filtros conservados y mensaje específico | Limpiar filtros |
| Cargando | Esqueleto con forma del contenido y progreso comprensible | Evitar saltos y controles prematuros |
| Sin conexión con copia | Franja persistente y fecha de actualización | Consultar copia sin presentarla como actual |
| Sin conexión sin copia | Mensaje específico, sin cifras | Reintentar o abrir borradores disponibles |
| Provisional | Guardado en este dispositivo; referencia temporal | Revisar pendientes; no sumar a saldos |
| Error de campo | Mensaje asociado y resumen con enlaces al inicio | Corregir sin perder los demás datos |
| Error de carga/envío | Identifica la tarea fallida; no parece lista vacía | Reintentar conservando captura |
| Conflicto | Tu captura frente a información actual | Editar o cancelar, sin resolución silenciosa |
| Éxito | Folio, resultado y siguiente paso | Abrir registro, sin envío duplicado |
| Falta de permiso | Explicación neutral sin datos protegidos | Volver o contactar al responsable |
| Sesión vencida | Explicación y acceso | Recuperar tarea disponible sin prometer sincronización inexistente |

## 6. Pantallas v2

Los identificadores siguientes son estables. Una pantalla común comparte componentes, no todos sus datos. Cada definición hereda la adaptación y estados anteriores.

### A01 · Acceso y recuperación

**Usuarios:** todos los usuarios privados. Formulario con correo, contraseña, Mostrar, Entrar y Recuperar acceso. Mensaje “Organiza tu producción, entregas y ventas”. La demostración es una entrada separada. No hay un selector administrador/usuario que conceda permisos.

Recuperación en panel breve con respuesta neutral al envío de instrucciones. Error conserva correo; sin conexión explica que no se puede iniciar sesión nueva. Móvil de una columna. Salida a A02 o último espacio autorizado.

### A02 · Elegir o iniciar espacio

Tarjetas de Mi producción y organizaciones vinculadas, con tareas habilitadas; no agrega sus saldos. Quien aún no tiene espacio puede iniciar uno independiente o revisar una invitación. La guía inicial pregunta qué necesita hacer y explica espacio propio frente a participación.

Cambiar con captura abierta requiere resolver cambios pendientes. Invitación inválida muestra ayuda y reintento; nunca abre registros ajenos. En móvil, tarjetas verticales y acción explícita Abrir espacio.

### P01 · Mi resumen — productor

Inicio por tareas: Registrar producción o Preparar entrega según modalidad. Tarjetas Disponible propio, Entregas en revisión y Última entrega recibida. Secciones Qué necesitas atender y Mis últimos registros. Cada cifra indica unidad y fecha/periodo.

No muestra el padrón completo, ventas de terceros o ingresos inexistentes. Si sólo registra entregas y no lleva inventario propio, no inventa ese inventario. Primera vez ofrece una acción clara; sin conexión muestra fecha de la copia. Las tarjetas enlazan a P02/P03.

### P02 · Mi producción — productor

Lista de cosechas/registros: fecha, producto, procedencia general, cantidad y disponibilidad propia. Filtros por periodo/estado; Registrar producción. En móvil, tarjetas con cantidad principal y siguiente acción.

Formulario: fecha, producto, cantidad neta en kg, origen general y evidencia/notas opcionales. Revisión muestra espacio y cantidad. No positivos o fecha inválida impiden confirmar sin borrar captura. Una producción confirmada puede preparar entrega o abastecer venta propia sin duplicarse. Sin registros, explicar qué capturar; enlace de detalle muestra movimientos propios asociados.

### P03 · Mis entregas — productor

Lista agrupable por destinatario: organización, fecha, cantidad declarada y estado. Estados Borrador, Enviada, En revisión, Recibida, Con diferencia y Cancelada. Enviada significa registro remitido; no recepción aceptada.

Preparar entrega elige destinatario autorizado y origen. Si no lleva inventario propio, se captura como entrega declarada sin crear una cosecha automática. Detalle con línea de tiempo, cantidades declarada/recibida, motivo de diferencia y comprobante. La organización confirma recepción; el productor aporta aclaraciones pero no altera esa confirmación. Sin conexión queda provisional. En móvil, la acción y destinatario siempre visibles antes de revisar.

### P04 · Mis documentos y actividad — productor

Comprobantes y archivos propios, filtros por tipo/destinatario/periodo, previsualización y descarga autorizada. Muestra estado de revisión y privacidad. Vacío explica cuándo aparecerán documentos; archivo fallido ofrece reintento.

La actividad muestra sus registros. En lotes colectivos se presenta su aportación y el alcance compartido, no datos de otros miembros. Volver conserva filtros; móvil usa vista de documento a pantalla completa.

### O01 · Resumen de operación — organización

Acción Recibir entrega. Indicadores recepción del periodo, salidas, pérdidas documentadas y existencia al corte. Por revisar reúne entregas remitidas, diferencias y expedientes incompletos; cada elemento lleva a la tarea correspondiente.

Primera vez ofrece registrar productor/recepción, sin obligar a configurar equipo si el usuario ya tiene acceso. Balance distingue entradas externas de transferencias internas. No muestra datos comerciales a quien no tiene permiso. La versión móvil prioriza pendientes y captura.

### O02 · Productores — operación

Padrón con identificador, nombre, procedencia y estado. Ficha lateral con entregas y aportaciones; contactos privados sólo con permiso. Alta breve, búsqueda y aviso de posible duplicado que permita revisar homónimos. Vacío ofrece Registrar productor.

Vincular acceso del productor es una acción separada del alta: muestra persona, espacio y registros que podrá consultar antes de confirmar. Archivar conserva historia. Móvil abre ficha completa; guardar retorna a la lista conservando selección.

### O03 · Recepción de entregas — operación

Pestañas Por recibir y Recibidas. La entrega remitida llega con sus datos, sin recaptura; también existe captura por operador para quien no tiene cuenta. Detalle: productor, procedencia, cantidad declarada, peso recibido, fecha, evidencia y observación.

Diferencia de peso solicita motivo y revisión, sin sobrescribir lo declarado. Confirmar resume destinatario y cantidad aceptada; P03 recibe ese resultado. No se crea otra entrega al aceptar una existente. Sin conexión sólo guardado provisional. Error mantiene captura. En móvil se prioriza productor, cantidad y revisión final.

### O04 · Lotes — operación o productor independiente autorizado

Lista de folio, producto, fecha, procedencia, existencia y condición. Crear lote abre aportaciones con origen, cantidad utilizable, cantidad asignada y total. Evita exceso de disponibilidad y duplicación de recepción.

Detalle con Resumen, Origen, Movimientos, Evidencias e Historial. Genealogía y lista equivalentes, cantidades por vínculo. Condición operativa y publicación separadas. Productor integrante ve sólo alcance compartido de su aportación. Conflicto conserva propuesta y solicita revisión; primera vez explica relación entre entrega y lote. Acciones Movimiento y Compartir sólo según permiso.

### O05 · Inventario y movimientos

Ámbito de organización o espacio propio explícito. Cuando hay ventas, separar existencia física, comprometido y disponible para nuevas ventas. Disponible = existencia utilizable menos compromisos activos. Preparar pedido no reduce saldo físico.

Movimientos: folio, fecha, tipo, cantidad, motivo y saldo. Salida, transferencia interna, pérdida documentada y corrección autorizada muestran antes/cambio/después. La salida comercial nace del pedido y aparece vinculada aquí, sin una segunda captura.

Saldo insuficiente impide confirmar. Diferencia de conteo se llama Diferencia por revisar, no merma automática. Transferencia interna no aumenta producción. Borradores excluidos. Tablas se convierten en tarjetas; exportar conserva filtros. Sin conexión se rotula la antigüedad de la disponibilidad.

### O06 · Evidencias y revisión

Archivo, registro vinculado, autor, fecha, revisión y privacidad. Panel de previsualización y observaciones. Adjuntar solicita tipo, fecha, archivo y vínculo; límites de formato y tamaño visibles antes de seleccionar.

Pendiente de revisión, Revisado y Requiere corrección. Revisado no significa certificación. Un documento faltante es tarea pendiente, no archivo creado. Error conserva el registro de destino y permite reintentar. Los archivos privados nunca se publican automáticamente por QR. En móvil, documento y revisión en una columna.

### V01 · Resumen comercial

Para responsable comercial o productor independiente que vende. Prioriza Pedidos por preparar, Entregas pendientes y Cobros por registrar. Acción Nuevo pedido; agenda de entregas y actividad. Importes con periodo y MXN; pedidos confirmados separados de cobros registrados.

Sin ventas ofrece crear cliente/pedido; no muestra márgenes sin costos ni interpreta un pedido como dinero cobrado. El productor integrante no adquiere acceso a ventas colectivas por estar en el padrón. Móvil prioriza próximos pedidos sobre indicadores.

### V02 · Clientes

Lista con nombre, contacto autorizado y pedidos. Alta: nombre, tipo y contacto opcional; dirección sólo si hace falta entregar. Ficha con pedidos, acuerdos y notas privadas. Posibles duplicados se revisan dentro del espacio activo.

Puede crearse un cliente desde el pedido y regresar sin perder captura. Archivar conserva operaciones. Sin registros ofrece una única acción inicial; error no borra el formulario. Los contactos no aparecen en QR ni se comparten entre espacios.

### V03 · Pedidos

Lista con folio, cliente, fecha comprometida, importe y estados independientes de pedido, entrega y cobro. Filtros por cada estado y periodo. Detalle con líneas, cantidades/unidades, precios, total, lotes asignados, actividad y siguiente acción.

Pedido: Borrador, Confirmado, Cancelado. Entrega: Sin preparar, Preparado, Parcial, Entregado. Cobro: Sin cobro registrado, Parcial, Registrado completo. Entregar no cambia automáticamente el cobro. Falta de registro no demuestra por sí sola que el cliente no haya pagado.

Cancelar sin despacho libera compromisos tras confirmar. Si hubo salida, requiere revisar devolución/corrección; no repone existencias automáticamente. Vacío distinto de búsqueda sin resultados. En móvil cada tarjeta conserva los tres estados rotulados.

### V04 · Crear o editar pedido

Pantalla completa con cliente, fecha de entrega, líneas de producto/presentación, cantidad, unidad, precio MXN y notas. Cada línea muestra disponibilidad y subtotal; resumen final indica qué conceptos incluye sin presumir reglas fiscales.

Envasado requiere equivalencia explícita: 40 unidades de 500 g = 20.00 kg. Las presentaciones las define el usuario; no son productos ya validados por CooperaLote. No sumar unidades a kilogramos directamente.

Guardar borrador no compromete existencias. Revisar y confirmar muestra cliente, cantidades y total; confirma compromiso sólo con disponibilidad suficiente. Si no alcanza, conservar borrador y permitir modificar, sin prometer entrega imposible. Precio/cantidad inválidos conservan resto. Sin conexión, sólo borrador con disponibilidad no actualizada. En móvil, líneas como tarjetas editables y total antes de confirmar.

### V05 · Preparar entrega comercial

Desde pedido: solicitado, preparado y pendiente por línea. Seleccionar lote y cantidad, referencia de entrega y evidencia opcional. Mostrar origen y efecto en saldo antes de confirmar salida.

Confirmación produce una única salida vinculada, reduce existencia y libera compromiso correspondiente. Entrega parcial conserva pendiente. Pulsación repetida no crea otra entrega. Lote bloqueado o saldo cambiado exige revisión; no sustituye origen silenciosamente. Resultado muestra folio, cantidad despachada y saldo; no registra cobro. Móvil permite revisar cantidades con controles amplios.

### V06 · Registrar cobro

Pedido con Total, Cobros registrados y Saldo por registrar. Formulario importe, fecha, medio declarado, referencia y comprobante opcional. Texto “Registrar un cobro recibido”; no ordena transferir dinero.

Revisión muestra cliente, pedido, importe y saldo resultante. Impide valores no positivos o superiores al saldo en este recorrido; anticipos/sobrepagos requieren una definición adicional. Corrección conserva motivo e historia. Borrador offline no modifica saldo. Registro de cobro no cambia inventario. En móvil el resumen precede la acción final.

### C01 · Compartir lote y consulta pública

Dos vistas distintas: gestión y visitante. Gestión selecciona campos autorizados y muestra previsualización antes de publicar. Publicar, copiar enlace, descargar QR o retirar publicación según permisos; retirada requiere confirmación. Visitante ve producto, identificador, organización y procedencia general autorizada, sin menú interno.

No publica contactos, documentos, cantidades internas ni identidades personales sin definición/autorización expresa. Explica que son datos declarados por la organización, no certificación. QR estático rotulado ilustrativo. Enlace inexistente, retirado y error de conexión se distinguen. Consulta pública móvil de una columna, sin tienda o compra implícita.

### C02 · Pendientes y conflictos

Cola agrupada por espacio: referencia temporal, tipo, fecha, estado y acción. Por enviar, Enviando, Requiere revisión, Rechazado y Confirmado. Mensaje “Guardado en este dispositivo; todavía no afecta tus saldos”.

Comparación captura/información actual para resolver conflicto. Editar, descartar con confirmación o reintentar después de revisar. No reasignar al cambiar espacio. Avisar de pendientes antes de cerrar sesión sin prometer disponibilidad en otros dispositivos. En móvil tarjetas; escritorio permite comparación lateral.

### C03 · Reportes e historial

Productor: producción y entregas propias. Organización: balance, lotes y documentos. Comercial: pedidos, entregas y cobros, diferenciando importes y volúmenes. Periodo, filtros, vista previa y descarga CSV/PDF según autorización.

Historial con fecha, persona, acción, objeto, motivo y comparación antes/después; sin borrar eventos. Exportación incluye espacio, periodo y marca ficticia cuando aplique. No incluye contactos/documentos privados por defecto. Sin denominador, ND; exportación fallida ofrece reintento. En móvil resumen y detalle desplegable.

### G01 · Equipo y permisos

Administración del espacio, como tarea secundaria. Lista de integrantes, responsabilidades, alcance y estado. Agregar integrante resume destinatario, espacio y accesos antes de invitar. Integrante con cuenta y productor del padrón son conceptos distintos.

Permisos por tareas: producción propia, recepción, inventario, ventas, revisión, exportación y gestión. Comercial no concede automáticamente modificar inventario o permisos. Suspender conserva autoría; evitar dejar espacio sin responsable. Falta de permiso muestra salida útil. Móvil organiza permisos por módulo, sin matriz ilegible.

### G02 · Preferencias, perfil y ayuda

Separar preferencias personales y de espacio. Idioma, fechas, unidades y zona horaria explícitas. Cambiar presentación no transforma cantidades históricas. El independiente gestiona su espacio sin configurar una estructura cooperativa.

Guías por tarea: producción, entrega, recepción, inventario, pedido y trabajo sin conexión. Pasos breves y posición constante. Guardado informa sección afectada; error conserva edición; no inventar contactos de soporte. Cerrar sesión revisa pendientes. En móvil, pestañas cortas y una columna.

## 7. Recorridos y datos coherentes

Todos los ejemplos son ficticios; los precios no son recomendaciones comerciales.

### Productor integrante → organización

1. A01 → A02 Mi producción → P01. P02 registra 100.00 kg propios.
2. P03 prepara entrega de 100.00 kg a Organización Demo del Mayab. Mientras se revisa, muestra comprometidos para entrega, sin permitir venderlos otra vez como libres.
3. O03 confirma recepción de 100.00 kg. P03 muestra Recibida. Espacio propio queda con 0.00 kg y organización reconoce 100.00 kg, sin llamarlos nueva producción regional.
4. O04 relaciona recepción y lote sin duplicar entrada. P04 conserva comprobante y aportación propia.

Si se reciben 98.00 kg frente a 100.00 declarados, los 2.00 kg son diferencia pendiente de aclarar. No se convierten automáticamente en merma ni en saldo propio disponible sin resolver su destino.

### Organización → venta → entrega → cobro

1. V02 Cliente Demo; V04 pedido de 40 unidades de 500 g a $90.00 MXN: 20.00 kg y $3,600.00 MXN, precio ilustrativo.
2. Confirmar compromete 20.00 kg: existencia física 100.00, comprometido 20.00, disponible 80.00 kg.
3. V05 entrega 20.00 kg de LOT-0001: existencia física 80.00, comprometido 0.00, disponible 80.00 kg. O05 muestra una sola salida.
4. V06 registra cobro parcial de $1,800.00 MXN: total $3,600.00, cobro registrado $1,800.00 y saldo por registrar $1,800.00. No altera existencias.
5. C03 separa pedidos, salidas y cobros en el reporte.

### Productor independiente que vende

A02 espacio propio → P02 producción → O05 inventario propio → V02 cliente → V04 pedido → V05 entrega → V06 cobro. No requiere entregar primero a una organización ni darse de alta como su propio proveedor.

### Conectividad limitada

Captura → guardar borrador → C02 → recuperar conexión → revisar → confirmar o resolver conflicto. Hasta confirmar no cambian saldos. No confirmar definitivamente pedidos, salidas o cobros usando una copia desactualizada de disponibilidad.

## 8. Plan y aceptación de mockups v2

### Archivos y cobertura de la serie generada

La nueva serie se aloja en `imgs/v2/`, con nombres por identificador, estado y dispositivo; por ejemplo, `P03-principal-mobile-r2.png` y `O03-sin-conexion-mobile-r2.png`. Los sufijos de revisión distinguen correcciones de una misma vista. El [índice de selección](indice-v2.json) indica qué archivos utiliza la galería; los borradores iniciales se conservan como antecedentes de generación.

La serie incluye una lámina de componentes, 25 vistas principales de los 23 identificadores funcionales —C01 y C03 requieren dos subvistas—, 3 adaptaciones móviles adicionales y 21 variantes de estados y situaciones: **50 imágenes seleccionadas**. La [matriz](cobertura-v2.md) distingue estados dibujados frente a estados sólo especificados. No se presenta como validación de campo ni aprobación del diseño por parte del usuario.

La galería abre con el recorrido del productor. Permite cambiar de perfil, filtrar vistas principales o situaciones, elegir dispositivo, buscar y ampliar cada imagen. Las explicaciones externas a las imágenes aclaran el momento del recorrido y los escenarios alternativos; estos últimos no se suman al balance principal. Las capturas son propuestas visuales, no componentes interactivos ni evidencia de cumplimiento de accesibilidad.

| Grupo | Vistas prioritarias | Variantes obligatorias |
|---|---|---|
| Productor | P01–P04 móvil | Inicio vacío, cantidad inválida, entrega con diferencia, pendiente |
| Organización | O01–O06 escritorio; O03 móvil | Padrón vacío, carga, recepción offline, saldo insuficiente, archivo fallido |
| Comercial | V01–V06 escritorio; V04/V05 móvil | Sin pedidos, disponibilidad cambiante, entrega parcial, cobro parcial/error |
| Común | A01/A02 y C01–C03 | Acceso fallido, espacio no vinculado, QR retirado, conflicto, exportación fallida |
| Gestión | G01/G02 | Sin permiso, invitación pendiente, cambios sin guardar |

### Criterios de revisión

- Los componentes tienen idéntico estilo y comportamiento entre perfiles. Las acciones principales no alternan entre miel y verde.
- El productor reconoce sus tareas sin interpretar un panel administrativo. El independiente puede producir y vender en su propio espacio.
- El comercial sigue un pedido hasta entrega y cobro registrado. Reservar no despacha; despachar no cobra; cobrar no modifica inventario.
- El caso conserva 100.00 kg recibidos, 20.00 kg despachados y 80.00 kg finales. Un volumen entregado no queda disponible simultáneamente en dos espacios.
- Dos productores ficticios ven sólo sus registros autorizados; dos organizaciones mantienen contextos separados; un comercial no ve gestión de accesos sin permiso.
- Cada flujo tiene una variante vacía, carga, error y conectividad pertinente. Los errores permiten recuperar la tarea sin empezar de cero.
- Se comprueban contrastes usados, foco, teclado, ampliación, lectura asistida y mensajes. Las imágenes evalúan apariencia; un prototipo navegable o implementación permite comprobar interacción accesible.
- Las pruebas de tareas incluyen productor, operación y comercial, con diversidad de experiencia digital. Registrar dificultades, éxito y tiempo; no presentar pruebas internas como validación de campo.

La v2 se considera visualmente lista cuando los tres recorridos principales son reconocibles, los controles son predecibles y los estados críticos están representados. Usar Tailwind o una captura limpia no basta para declarar accesibilidad o usabilidad comprobadas.
