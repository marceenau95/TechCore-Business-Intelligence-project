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
