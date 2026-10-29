# Assessoria 3.0 Intelligence — MVP funcional

Dashboard de Business Intelligence ejecutado en el navegador. Importa el Excel exportado del CRM, explora filtros, gráficas, rankings, comisiones, incidencias y consultas deterministas.

## Iniciar
Abre `index.html` en Chrome, Safari o Edge con conexión a internet (para cargar SheetJS y ECharts). Arrastra tu Excel al apartado «Importar datos».

## Desplegar en Vercel
1. Crea un repositorio con `index.html` y `vercel.json`.
2. Importa el repositorio en Vercel.
3. Framework: «Other»; no hay comando de compilación. Directorio de salida: `.`.

## Funciones implementadas
- Importación local de `.xlsx`, `.xls`, `.csv` y cambio/fusión de datos de sesión.
- Normalización de provincias, fechas y campos de CRM.
- 13 vistas, filtros cruzados, gráficos interactivos, tablas y búsquedas.
- Ranking por empresa, usuario y ubicación; KPIs de comisiones separadas.
- Consultas estadísticas locales basadas en datos importados.
- Exportación a CSV con filtros y PDF desde impresión del navegador.
- Dark/light mode, responsive y controles de accesibilidad básicos.

## Limitaciones de esta primera versión
No es todavía una aplicación Next.js. Es una versión cero compilación y lista para desplegar en Vercel, elegida para entregar un archivo ejecutable sin infraestructura. Las librerías gráficas y Excel se cargan desde CDN; requiere conectividad. Los datos no se guardan al cerrar la pestaña, y no se transmiten a servidores desde el código de la aplicación. **No usar en entorno multiusuario sin desarrollar autenticación, permisos, base de datos, auditoría, RGPD y pruebas de seguridad**. Sin API de IA; solo respuestas deterministas. Mapa detallado aún sustituido por rankings geográficos. La fusión usa una clave aproximada y no ofrece garantía transaccional de identificador contractual único. Se ofrece exportación CSV, no XLSX nativo.

## Avisos de cálculo
- Clientes únicos: CIF/NIF no vacío.
- Fechas de referencia: carterización > tramitación > traspaso.
- Los consumos no se suman hasta conocer unidad y período.
- Comisiones de venta y subdominio son independientes y no se tratan como cobradas.
