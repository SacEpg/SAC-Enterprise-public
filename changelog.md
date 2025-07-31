# Bitácora de Cambios

## 3.5.2 (31/07/2025)
### Correciones de errores
- Se corrigen los errores de colisión de números de documentos al hacer registros simultáneos
- Se corrige el recálculo de costo promedio para artículos con código de mas de 20 carácteres
### Nuevas Funcionalidades
- Se mejora el rendimiento de la pantalla de Documentos Relacionados
- Se implementa parámetro de cantidad de dias máximo para emitir una Nota de Crédito
- Se implementa la actualización autómatica de secuencia de eNCF cuando es rechazada por uso previo
- Se implementa parámetro para forzar a usar el almacén del usuario al momento de facturar
- Se permite emitir facturas electrónicas en lote a traves de la pantalla de Documentos Preliminares de CxC
- Se anexa automáticamente a los documentos el archivo XML de los documentos electrónicos  

## 3.5.1 (20/06/2025)
### Correciones de errores
- Error al contabilizar recibo de producción
- Error al duplicar un documento de clase Servicio
- Error a hacer Nota de Credito electronica a factura de consumidor final que se envio en una fecha distinta de la que se hizo
### Nuevas Funcionalidades
- Permitir anular Facturas de Compra Electronica con Nota de Credito Proveedor

## 3.5.0 (02/06/2025)
### Nuevas Funcionalidades
- Inclusión del campo de longitud y latitud en el maestro de cliente, con visualización en Google Maps.
- Se agregaron los reportes de conciliación CxC y CxP al proyecto e instalador.
- Incorporación del reporte "Actividad de Clientes".
- Agregado el reporte MRP.
- Implementación del uso de costo histórico en salidas de inventario.
- Desarrollo de funcionalidades completas de ubicaciones en inventario:
  - Pantalla de definición de ubicaciones.
  - Validaciones de bloqueo y coincidencia entre ubicación y almacén.
  - Selección automática de ubicación por defecto en artículos.
  - Actualización de cantidades según ubicación.
  - Integración con documentos y transacciones.
- Inclusión del campo de ubicación en recibos de producción.
- Agregados íconos distintivos para reportes Premium.
- Implementado mapeo de campos de usuario para facturación electrónica.
- Se muestran los reportes personalizados en los menús.
### Correcciones de Errores
- Corregido error al aplicar eCNF afectado manualmente.
- Solucionado problema que impedía editar parámetros del reporte.
- Ajustada validación NCF para permitir eCF en pantalla de gastos menores.
- Corregido cálculo de balance facturas de compra con retenciones.
- Ajustado el formato de nómina electrónica del BPD.
- Arreglado error al generar reportes con stored procedures sin prefijo estándar.
- Corregido el nombre del reporte para el menú.
### Otros Cambios Técnicos y Refactorizaciones
- Añadido el proyecto de instalador del servidor al repositorio.
- Integración de librerías Skybound al repositorio.
- Cambios al esquema de validación de licencias por tipo de producto (deprecated).
- Mejoras en la lógica de autenticación de usuarios y visualización de compañías.
- Inclusión de campos omitidos en generación de INSERT desde Recordset.
- Refactor y mejoras en la validación de licencias.
- Inclusión del DLL de Ingenico en el repositorio.
- Se actualizó el campo NewCost tras cambio en el costo promedio.
- Cambios en la estructura de carpetas del instalador.
- Se actualizó la versión del ensamblado a 3.4.4.
- Se actualizó sac.license a .NET Framework 4.8.
- Refactor del evento BeforeChooseFromList.
- Varios merges de ramas como Ubicaciones y master.
- Implementación del evento BeforeChooseFromList personalizado.
- Reparado el insert en la tabla WarehouseTransactions.
- Solucionado error al hacer split del script de actualización y compatibilidad con statements multilinea.

## 3.4.4 (19/02/2025)
- Corrige error al cargar addons en Windows 11
- Corrige error al cancelar una nómina que ha sido pagada
- Se habilita el campo “Comentario” en los recibos de producción
- Se cambia al nombre a la pantalla “Control de Despachos”
- Se cancelas las Notas de Crédito por descuento en pago al anular una recibo de ingreso
- Se verifica el idioma del SQL server al conectarse a la base de datos
- Se permite definir las retenciones a aplicar desde la pantalla de factura proveedor (esto genera un pago a la factura con las retenciones)
- Se incluye el formato de nómina electrónica del banco ADEMI
- Se permite cerrar una recepción de mercancía
- Se incluyen los nuevos formatos de impresión de documentos por defecto
- Se incluye el reporte de Formulario IT1
- Se incluye el reporte “Valoración de Inventario Histórico”
- Se incluye el reporte “Balanza de Comprobación Detallada”
- Se incluye automáticamente el centro de costo en el detalle de los documentos cuando se pone en el encabezado
