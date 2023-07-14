# Power BI Report Samples

Bienvenido(a) al repositorio de ejemplos de informes de Power BI! Aquí encontrarás una colección de informes de muestra que muestran diversos escenarios de análisis de datos y demuestran el uso de fórmulas DAX. Estos informes están diseñados para ayudarte a aprender y explorar las capacidades de Power BI.

## Lista de Informes

### 1. Panel de Desempeño de Ventas

Este panel proporciona una visión general del rendimiento de ventas para diferentes regiones y categorías de productos. Incluye visualizaciones como ventas por región, productos más vendidos y crecimiento de ventas año tras año. Se utilizaron las siguientes fórmulas DAX:

- **Total Sales**: `Total Sales = SUM(Sales[Amount])`
- **Year-over-Year Growth**: `YoY Growth = DIVIDE(SUM(Sales[Amount]), CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR(Dates[Date]))) - 1`

### 2. Análisis de Segmentación de Clientes

Este informe analiza la segmentación de clientes basada en su comportamiento de compra. Incluye visualizaciones como distribución de clientes, valor promedio de compra y valor de vida del cliente. Se utilizaron las siguientes fórmulas DAX:

- **Purchase Frequency**: `Purchase Frequency = COUNTROWS(Sales) / DISTINCTCOUNT(Sales[CustomerID])`
- **Customer Lifetime Value**: `CLTV = SUMX(Sales, [Average Order Value] * [Purchase Frequency] * [Average Customer Lifespan])`

### 3. Panel de Gestión de Inventario

Este panel proporciona información sobre los niveles de inventario y movimiento de stock. Incluye visualizaciones como niveles de stock actuales, tasa de rotación de stock y productos más vendidos. Se utilizaron las siguientes fórmulas DAX:

- **Stock Turnover Rate**: `Stock Turnover Rate = DIVIDE(SUM(Sales[Quantity]), SUM(Inventory[Stock]))`
- **Average Days to Sell**: `Avg Days to Sell = DIVIDE(DISTINCTCOUNT(Dates[Date]), SUMX(Inventory, IF([Stock]>0, 1, 0)))`

## Empezando

1. Clona o descarga el repositorio en tu máquina local.
2. Abre la aplicación de Power BI Desktop.
3. Selecciona "Abrir" y navega hasta el archivo del informe descargado (.pbix).
4. Explora las visualizaciones, filtros e interacciones del informe.
5 .Revisa las fórmulas DAX en el panel "Campos" y la pestaña "Modelado".

Siéntete libre de personalizar y mejorar estos informes según tus necesidades específicas. ¡Esperamos que estos ejemplos te inspiren a aprovechar al máximo Power BI en tus proyectos de análisis de datos!

Si tienes alguna pregunta o sugerencia, no dudes en comunicarte con nosotros. ¡Disfruta del análisis de datos con Power BI!

