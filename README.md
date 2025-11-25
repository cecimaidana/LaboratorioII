# 📊 Laboratorio II: El Poder de Power BI

## 📘 Descripción del Proyecto 
Este repositorio aloja el proyecto de Power BI Desktop (LaboratorioII.pbix) desarrollado para un análisis integral de ventas y rendimientos. El informe fue construido sobre datos sintéticos de una cadena de tiendas con sucursales distribuidas en 5 países y enfocada en la comercialización de productos segmentados en 8 categorías.

🛠️ Proceso ETL (Editor Power Query)
🏗️ Modelado de Datos
📈 Medidas DAX y Cálculos Clave
🖥️ Dashboard Interactivo

### 🌟 Estructura del Modelo (Copo de Nieve)

El informe se basa en un modelo que centraliza las métricas en la tabla de hechos `salesF` y se extiende a través de múltiples tablas de dimensión:

| Tabla | Tipo | Función en el Modelo |
| :--- | :--- | :--- |
| **`salesF`** | Hecho | Contiene las transacciones y métricas clave (`Quantity`, `SaleID`, `SalesDate`). Es el centro del modelo. |
| **`products`** | Dimensión | Datos de los productos vendidos. Conectada a `salesF` y a la dimensión `categories`. |
| **`categories`** | Dimensión | Detalles de las 8 categorías de productos. |
| **`Calendar`** | Dimensión | Tabla de fechas utilizada para segmentar y filtrar por tiempo. |
| **`customers`** | Dimensión | Información de los clientes. Conectada a `salesF` y a la dimensión geográfica `cities`. |
| **`employees`** | Dimensión | Información de los vendedores. Conectada a `salesF` y a la dimensión geográfica `cities`. |
| **`cities`** | Dimensión | Nombres de ciudades. Actúa como puente entre `countries` y las dimensiones `customers` y `employees`. |
| **`countries`** | Dimensión | Detalles de los 5 países. Dimensión final en la jerarquía geográfica. |

## 🛠️ Requisitos
Para poder abrir y trabajar con este archivo, es necesario tener instalado:
1.  **Power BI Desktop**: Software gratuito de Microsoft.

## 👩‍💻 Autor
**Cecilia Patricia Maidana**

