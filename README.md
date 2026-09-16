# QA Test Matrix — Sauce Demo (Excel)

## Objetivo

Proyecto de portafolio QA enfocado en diseño y gestión de pruebas manuales en Excel: matriz de casos de prueba, trazabilidad de requisitos, bitácora de defectos y un dashboard de resultados calculado por fórmulas — todo aplicado sobre [saucedemo.com](https://www.saucedemo.com).

## Contenido del workbook (`qa-test-matrix.xlsx`)

| Hoja | Contenido |
|---|---|
| Instrucciones | Cómo está organizado el archivo y qué significa cada hoja |
| Dashboard | Resumen automático (fórmulas) de resultados de ejecución y defectos encontrados, con gráfico |
| Requisitos | Requisitos funcionales del sitio, cubriendo Login, Inventory, Cart y Checkout |
| Matriz de Trazabilidad | Vincula cada requisito con los casos de prueba que lo cubren (cálculo automático, sin edición manual) |
| Casos de Prueba | Más de 40 casos diseñados y ejecutados sobre los 4 módulos del sitio |
| Bitácora de Bugs | Defectos documentados; los campos de contexto (módulo, prioridad, pasos, resultados) se autocompletan por fórmula al escribir el ID del bug, referenciando la hoja de Casos de Prueba |

## Técnicas de diseño de pruebas aplicadas

- Clases de equivalencia
- Análisis de valores límite
- Tabla de decisión
- Transición de estados

## Hallazgos destacados

Durante la ejecución se documentaron varios defectos reales, entre ellos:

- El checkout permite avanzar al flujo de compra aunque el carrito esté vacío, sin ninguna validación que lo impida.
- El formulario de checkout no valida el formato de los campos "First Name", "Last Name" y "Postal Code" — acepta números donde debería haber letras y texto no numérico en el código postal, solo revisa que no estén vacíos.

## Cómo revisar el archivo

Descarga `qa-test-matrix.xlsx` y ábrelo en Excel. La vista previa integrada de GitHub muestra una tabla básica, pero no refleja el formato condicional ni el gráfico del Dashboard — eso solo se ve completo al abrirlo directamente.
