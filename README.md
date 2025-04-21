# excel-desbloqueado
**rango de funcionalidades de Excel organizadas de básico a avanzado**, ideal para identificar tu nivel actual y avanzar paso a paso:

---

### **Nivel Básico**  
**1. Interfaz y operaciones esenciales:**  
- Familiarización con celdas, filas, columnas y hojas.  
- Formato básico (negrita, cursiva, bordes, colores).  
- Insertar/eliminar filas y columnas.  
- Ajustar anchos y alturas.  
- Guardar y exportar archivos (`.xlsx`, `.csv`).  

**2. Fórmulas básicas:**  
- `=SUMA()`, `=PROMEDIO()`, `=MÍN()`, `=MÁX()`.  
- Operadores matemáticos (`+`, `-`, `*`, `/`).  
- Referencias relativas y absolutas (`A1`, `$A$1`).  

**3. Funciones simples:**  
- `=CONTAR()`: Cuenta celdas con números.  
- `=CONCATENAR()` o `&`: Unir texto.  
- `=HOY()` y `=AHORA()`: Fechas y horas actuales.  

**4. Gestión de datos básica:**  
- Ordenar datos (ascendente/descendente).  
- Filtros simples (seleccionar valores específicos).  

---

### **Nivel Intermedio**  
**1. Funciones avanzadas:**  
- `=SI()`: Condicionales simples.  
- `=BUSCARV()` / `=BUSCARH()`: Búsquedas verticales/horizontales.  
- `=CONTAR.SI()` y `=SUMAR.SI()`: Criterios únicos.  
- `=ESERROR()`: Manejo básico de errores.  

**2. Herramientas de formato:**  
- Formato condicional (resaltar celdas, barras de datos).  
- Validación de datos (listas desplegables, restricciones).  
- Proteger hojas y celdas.  

**3. Gestión de datos intermedia:**  
- Tablas dinámicas (**PivotTables**) básicas.  
- Eliminar duplicados.  
- Texto en columnas (dividir datos).  

**4. Gráficos y visualización:**  
- Crear gráficos (barras, líneas, circulares).  
- Mini gráficos (**Sparklines**).  

---

### **Nivel Avanzado**  
**1. Funciones complejas:**  
- `=INDICE()` + `=COINCIDIR()`: Búsquedas flexibles.  
- `=SUMAR.SI.CONJUNTO()` / `=CONTAR.SI.CONJUNTO()`: Múltiples criterios.  
- `=SI.ERROR()` y anidamiento de funciones.  
- `=XLOOKUP()` (Excel 365+): Búsquedas mejoradas.  

**2. Tablas dinámicas avanzadas:**  
- Agrupar datos por fechas o rangos.  
- Campos calculados y medidas.  
- Segmentación de datos (**Slicers**).  

**3. Automatización:**  
- **Power Query**: Limpieza y transformación de datos.  
- **Macros** (grabación y VBA básico).  
- Integración con **Power BI** para dashboards.  

**4. Fórmulas matriciales y dinámicas:**  
- Funciones de matriz (`=TRANSPONER()`, `=FILTRO()`, `=ORDENAR()`).  
- Fórmulas con `Ctrl + Mayús + Enter` (ej.: `=SUMA(SI(...))`).  

**5. Análisis avanzado:**  
- **Solver**: Optimización con restricciones.  
- **Escenarios** y tablas de datos (análisis de sensibilidad).  
- **Previsión (Forecast Sheet)**: Predicciones basadas en datos históricos.  

**6. Integración y colaboración:**  
- Vincular hojas y libros (`=[Libro2]Hoja1!A1`).  
- Compartir en la nube (OneDrive/Teams).  
- **Power Automate**: Flujos automatizados.  

---

### **Nivel Experto**  
**1. Programación en VBA:**  
- Crear funciones personalizadas.  
- Automatizar procesos complejos.  
- Interactuar con APIs externas.  

**2. Modelado de datos avanzado:**  
- **Power Pivot**: Trabajar con grandes volúmenes de datos.  
- **DAX (Data Analysis Expressions)**: Crear métricas complejas.  

**3. Integración con otras herramientas:**  
- Conectar Excel con bases de datos (SQL, Access).  
- Usar **Power BI** para visualizaciones interactivas.  
- Automatización con **Python** (mediante complementos).  

---

### **Tips para progresar:**  
1. **Practica con proyectos reales**: Presupuestos, informes, dashboards.  
2. **Aprende atajos clave**: `Ctrl + Mayús + L` (filtros), `Alt + F11` (VBA).  
3. **Explora plantillas avanzadas**: Microsoft ofrece plantillas para finanzas, inventarios, etc.  
4. **Certificaciones**: MOS (Microsoft Office Specialist) o cursos en plataformas como Coursera.  

¡Perfecto! Aquí tienes **ejercicios prácticos organizados por nivel** (básico a experto) para dominar Excel. Cada ejercicio incluye un objetivo, pasos clave y ejemplos:

---

### **Nivel Básico**  
**Ejercicio 1: Crear una tabla de gastos mensuales**  
- **Objetivo:** Usar fórmulas básicas y formato.  
- **Pasos:**  
  1. En una hoja, crea columnas: **Fecha**, **Descripción**, **Categoría**, **Monto**.  
  2. Ingresa 10 filas de datos ficticios (ej.: "Netflix", "Comida", "Transporte").  
  3. En la última fila, usa `=SUMA()` para totalizar los gastos.  
  4. Aplica formato de moneda a la columna **Monto** y bordes a la tabla.  
- **Ejemplo:**  
  ```
  | Fecha    | Descripción | Categoría  | Monto  |
  |----------|-------------|------------|--------|
  | 01/01/24| Netflix     | Entretenimiento | $15  |
  | ...      | ...         | ...        | ...    |
  | Total    |             |            | =SUMA(D2:D11) |
  ```

---

**Ejercicio 2: Ordenar y filtrar datos**  
- **Objetivo:** Gestionar listas de información.  
- **Pasos:**  
  1. Crea una tabla con columnas: **Nombre**, **Edad**, **Ciudad**, **Puntuación** (20 filas).  
  2. Ordena los datos por **Edad** (ascendente).  
  3. Aplica un filtro para mostrar solo personas de "Madrid" con puntuación >70.  

---

### **Nivel Intermedio**  
**Ejercicio 1: Usar BUSCARV (VLOOKUP)**  
- **Objetivo:** Combinar datos de dos tablas.  
- **Pasos:**  
  1. Tabla 1: **ID_Producto**, **Nombre_Producto**.  
  2. Tabla 2: **ID_Producto**, **Precio**.  
  3. En Tabla 1, agrega una columna **Precio** con:  
     ```excel
     =BUSCARV(A2, Tabla2, 2, FALSO)
     ```  
  4. Verifica que los precios coincidan.  

---

**Ejercicio 2: Crear una tabla dinámica (PivotTable)**  
- **Objetivo:** Resumir ventas por región.  
- **Pasos:**  
  1. Usa una tabla de ventas con columnas: **Región**, **Producto**, **Cantidad**, **Ventas**.  
  2. Inserta una tabla dinámica y agrupa por **Región** y **Producto**.  
  3. Agrega **Ventas** a valores (suma) y **Cantidad** a valores (promedio).  

---

### **Nivel Avanzado**  
**Ejercicio 1: Combinar INDICE + COINCIDIR (INDEX + MATCH)**  
- **Objetivo:** Buscar datos en cualquier dirección.  
- **Pasos:**  
  1. Tabla con **Empleado_ID**, **Nombre**, **Departamento**, **Salario**.  
  2. Usa esta fórmula para buscar el salario por **Empleado_ID**:  
     ```excel
     =INDICE(D2:D100, COINCIDIR("ID_Buscado", A2:A100, 0))
     ```  
  3. Compara con BUSCARV y explica las ventajas.  

---

**Ejercicio 2: Limpiar datos con Power Query**  
- **Objetivo:** Importar y transformar datos sucios.  
- **Pasos:**  
  1. Descarga un CSV con datos desordenados (ej.: columnas mezcladas, duplicados).  
  2. Ve a **Datos > Obtener datos > Desde archivo CSV**.  
  3. En Power Query:  
     - Elimina filas duplicadas.  
     - Divide una columna combinada (ej.: "Nombre_Apellido" en dos).  
     - Filtra registros con errores.  
  4. Carga los datos limpios a Excel.  

---

### **Nivel Experto**  
**Ejercicio 1: Crear una función personalizada en VBA**  
- **Objetivo:** Calcular el IVA con una función propia.  
- **Pasos:**  
  1. Abre el editor VBA (`Alt + F11`).  
  2. Inserta un módulo y escribe:  
     ```vba
     Function IVA(monto As Double, tasa As Double) As Double
         IVA = monto * tasa
     End Function
     ```  
  3. En Excel, usa `=IVA(100, 0.16)` para calcular $16.  

---

**Ejercicio 2: Modelar datos con Power Pivot y DAX**  
- **Objetivo:** Analizar ventas con relaciones complejas.  
- **Pasos:**  
  1. Importa tablas **Ventas** y **Productos** a Power Pivot.  
  2. Crea una relación entre **Producto_ID**.  
  3. Usa DAX para crear una medida:  
     ```dax
     Ventas Totales = SUM(Ventos[Ventas])
     ```  
  4. Genera un informe dinámico con segmentaciones.  

---

### **Bonus: Ejercicio Integrado (Todos los niveles)**  
**Crear un dashboard de ventas:**  
1. **Básico:** Usa tablas y formatos para ingresar datos.  
2. **Intermedio:** Aplica BUSCARV para vincular tablas de productos y ventas.  
3. **Avanzado:** Usa Power Query para consolidar datos de múltiples archivos.  
4. **Experto:** Automatiza actualizaciones con VBA y muestra resultados en gráficos interactivos.  

---

**Consejo:**  
- Usa datos reales o descarga datasets de plataformas como [Kaggle](https://www.kaggle.com/). 