# 📊 TechCore - Business Intelligence Dashboard

## 📌 Descripción

Proyecto de Business Intelligence desarrollado en **Power BI** para analizar el comportamiento comercial de TechCore y facilitar la toma de decisiones mediante indicadores, visualizaciones interactivas y segmentación de información.

El proyecto abarca desde la preparación y estructuración de los datos hasta la construcción de un modelo relacional y el desarrollo de un dashboard interactivo.

---

## 🎯 Objetivos

- Transformar datos comerciales en información útil para la toma de decisiones.
- Analizar el comportamiento de ventas, clientes y vendedores.
- Construir indicadores clave de desempeño (KPIs).
- Facilitar la exploración de información mediante dashboards interactivos.
- Implementar controles de acceso a la información según el perfil del usuario.

---

## 🛠️ Tecnologías utilizadas

- **Power BI**
- **Power Query**
- **DAX**
- **Excel**
- **CSV**

---

## 🔄 Proceso del proyecto

### 1. Preparación y modelado de datos

Se realizó la estructuración y validación de la información comercial para construir un modelo relacional preparado para su integración en Power BI.

El modelo está compuesto por las siguientes entidades:

- Facturas
- Detalle de Facturas
- Productos
- Clientes
- Vendedores
- Ciudades
- Sucursales
- Métodos de Pago

Se validó la integridad de las relaciones entre las tablas y posteriormente se exportó el modelo para su carga en Power BI.

### 2. Modelo de datos

Se construyó un modelo de datos con estructura dimensional para facilitar el análisis de la información comercial y la creación de medidas e indicadores.

### 3. Dashboard interactivo

El dashboard se estructuró en tres secciones principales:

#### 📈 Ventas
Análisis del desempeño comercial desde perspectivas temporales, geográficas y de producto.

**KPIs principales:**
- Ventas Totales
- Ticket Promedio
- Cantidad de Facturas
- Participación de Ciudad en Ventas

**Visualizaciones:**
- Evolución de ventas
- Ventas por marca
- Distribución geográfica
- Productos más vendidos

#### 👥 Clientes
Análisis del comportamiento y características de los clientes.

**KPIs principales:**
- Clientes Únicos
- Ticket Promedio por Cliente
- Valor Total de Compras

**Visualizaciones:**
- Clientes por ciudad
- Métodos de pago
- Rango de edad
- Distribución por género
- Top 5 clientes por compras

#### 👤 Vendedores
Análisis del desempeño comercial individual.

**KPIs principales:**
- Ventas por Vendedor
- Ticket Promedio
- Facturas Gestionadas
- Ranking de Vendedores

**Visualizaciones:**
- Comparación de ventas
- Ranking comercial
- Evolución temporal
- Participación comercial

---

## 📐 Medidas DAX

Se desarrollaron medidas DAX para calcular y soportar los principales indicadores del dashboard, incluyendo:

- Ventas Totales
- Ticket Promedio
- Cantidad de Facturas
- Clientes Únicos
- Participación porcentual por ciudad
- Ranking de Vendedores
- Segmentación por rango de edad

---

## 🎛️ Interactividad

Se implementaron segmentadores dinámicos para facilitar el análisis por:

- Ciudad
- Sucursal
- Marca
- Método de Pago
- Fecha
- Rango de Edad

Los segmentadores fueron sincronizados entre las diferentes páginas del dashboard.

---

## 🔐 Seguridad a Nivel de Fila (RLS)

Se implementó **Row Level Security (RLS)** mediante `USERPRINCIPALNAME()` para controlar el acceso a la información según el usuario autenticado.

Se definieron tres perfiles:

- **Director General:** acceso completo a la información.
- **Gerente Regional:** acceso a las ventas correspondientes a su ciudad.
- **Gerente de Sucursal:** acceso únicamente a la información de su sucursal.

---
## 📊 Principales insights

El análisis del comportamiento comercial permitió identificar los siguientes hallazgos:

- **Concentración geográfica:** Medellín y Bogotá concentran el mayor volumen de ventas, representando aproximadamente el **45 % y 31 %** de las ventas totales, respectivamente.
- **Marcas líderes:** Lenovo presenta el mejor desempeño, seguida por HP y Dell, reflejando una mayor preferencia de los clientes por estas marcas.
- **Desempeño comercial:** los vendedores con mejores resultados se concentran principalmente en las sucursales de Medellín, destacándose Ana Sofía Llopis Blázquez como la vendedora con mayor desempeño.
- **Métodos de pago:** la tarjeta de crédito es el medio de pago más utilizado, mientras que el efectivo presenta la menor participación.
- **Perfil de clientes:** los segmentos de edad **36-45 y 26-35 años** presentan las mayores participaciones en ventas, con aproximadamente 29,4 % y 29,1 %, respectivamente.
- **Oportunidades comerciales:** las ciudades con menor participación y las marcas con menor rotación representan oportunidades para desarrollar estrategias comerciales específicas.

## 💡 Recomendaciones

A partir de los hallazgos obtenidos, se plantean las siguientes recomendaciones:

- Desarrollar **estrategias comerciales diferenciadas por región** para fortalecer las ciudades con menor participación.
- Fortalecer las relaciones con proveedores y evaluar la ampliación de inventario para marcas de alto desempeño como **Lenovo, HP y Dell**.
- Diseñar estrategias que aprovechen la preferencia de los clientes por **medios de pago electrónicos**.
- Identificar buenas prácticas de los vendedores de alto desempeño y desarrollar **programas de capacitación** para replicarlas en otros equipos.
- Utilizar la segmentación demográfica para diseñar **campañas de marketing y fidelización personalizadas**.
- Impulsar las marcas de menor rotación mediante promociones, bundles y campañas digitales dirigidas a segmentos específicos.

---
## 📁 Estructura del proyecto

```text
TechCore-BI/
│
├── data/
│   ├── ModeloVentas.xlsx
│   └── users.csv
│
├── dashboard/
│   └── TechCore_Dashboard.pbix
│
├── README.md
└── images/
    └── dashboard.png
