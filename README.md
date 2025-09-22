
### **Segmentación de Clientes con K-Means**

Este proyecto utiliza un enfoque de **aprendizaje no supervisado** para segmentar la base de clientes de una tienda minorista. Mediante el uso de métricas clave como el **RFM (Recencia, Frecuencia, Monto Monetario)** y el algoritmo de clustering **K-Means**, el objetivo es identificar y analizar grupos de clientes con comportamientos de compra distintivos. El resultado es un análisis de negocio actionable que puede guiar las estrategias de marketing. 

---

### **1. Problema y Objetivo de Negocio**

El principal desafío en el análisis de clientes es comprender las necesidades y el comportamiento de una base de clientes diversa. El objetivo de este proyecto es:

* **Identificar segmentos de clientes** basados en su comportamiento de compra.
* **Crear perfiles detallados** de cada segmento para entender sus características.
* **Proporcionar recomendaciones de negocio** para personalizar las estrategias de marketing, mejorar la retención y optimizar la rentabilidad.

---

### **2. Metodología**

La metodología del proyecto se dividió en las siguientes fases:

* **ETL (Extracción, Transformación y Carga)**: Los datos transaccionales se agregaron para crear un DataFrame de clientes, donde cada fila representa un cliente único y sus métricas RFM.
* **Análisis Exploratorio de Datos (EDA)**: Se analizó la distribución de las variables RFM. Se realizó el **escalado de datos** utilizando `StandardScaler` para asegurar que las variables tuvieran la misma influencia en el modelo, ya que K-Means es sensible a la escala.
* **Modelado**: Se eligió **K-Means** por su eficiencia y la facilidad de interpretación de los resultados.
* **Selección del Número de Clústeres**: Para determinar el número óptimo de segmentos (`k`), se utilizó el **método de la silueta**, el cual evalúa la cohesión y separación entre los clústeres.
* **Análisis de Clústeres**: Los clústeres fueron analizados para entender sus características promedio de RFM. Se les asignó una clasificación descriptiva para convertirlos en información de negocio útil.

---

### **3. Resultados y Perfiles de Cliente**

El modelo identificó **tres segmentos de clientes** con perfiles de comportamiento claramente diferenciados:

* **Clúster 0: Clientes de Alto Potencial**
    * **Características**: Baja Recencia, Frecuencia baja, pero un Monto alto.
    * **Descripción**: Clientes que realizaron una compra grande recientemente. Tienen un alto valor potencial, pero aún no han demostrado lealtad.
* **Clúster 1: Clientes de una Sola Compra**
    * **Características**: Recencia alta, Frecuencia muy baja, y un Monto moderado.
    * **Descripción**: Este segmento representa a clientes que realizaron una única compra hace tiempo y están en riesgo de abandono.
* **Clúster 2: Clientes VIP**
    * **Características**: Baja Recencia, Frecuencia alta, y un Monto de gasto muy elevado.
    * **Descripción**: Los clientes más valiosos y leales para el negocio.



---

### **4. Conclusiones y Recomendaciones**

La segmentación de clientes proporciona una base sólida para estrategias de marketing personalizadas. Se pueden aplicar las siguientes recomendaciones de negocio:

* **Clientes VIP**: Implementar programas de lealtad o acceso exclusivo para asegurar su retención.
* **Clientes de Alto Potencial**: Fomentar una segunda compra con ofertas personalizadas y recomendaciones de productos.
* **Clientes de una Sola Compra**: Lanzar campañas de reactivación con descuentos o incentivos para reengancharlos.

---

### **5. Librerías y Dependencias**

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

---

### **6. Cómo usar el proyecto**

1.  Clona este repositorio: `git clone [URL_del_repositorio]`
2.  Ejecuta el notebook `segmentation_customer_model.ipynb` en un entorno de Jupyter.