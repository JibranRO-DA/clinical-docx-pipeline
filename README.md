# ANVA

ANVA es un **pipeline en Python** desarrollado para **extraer información clínica no estructurada** a partir de notas médicas en formato `.docx`, con el objetivo de generar insumos confiables para **análisis epidemiológico y reportes en Power BI**.

El proyecto fue creado para resolver una **necesidad urgente de cumplimiento normativo**, por lo que está diseñado como una solución **puntual, cerrada y de uso único**.

---

## 🩺 Contexto del proyecto

Las notas médicas se encontraban en archivos Word (`.docx`) sin una estructura tabular reutilizable.  
ANVA automatiza la lectura de estos documentos, identifica campos clave mediante **expresiones regulares** y lectura de **contenido XML (checkboxes)**, y consolida la información en un dataset listo para análisis.

El resultado final fue utilizado para la elaboración de un **reporte epidemiológico**, incluyendo modelado de datos y visualización en Power BI.

---

## 📌 Información extraída

A partir de cada nota médica, el script identifica y procesa:

- Servicio / tipo de documento
- Fecha de atención
- Nombre completo del paciente
- Edad
- Sexo (a partir de checkboxes en el XML del documento)
- Diagnóstico(s)

Un mismo paciente puede generar múltiples registros si la nota contiene más de un diagnóstico.

---

## 🧠 Flujo de procesamiento

1. Iteración automática de carpetas y subcarpetas
2. Lectura exclusiva de archivos `.docx`
3. Extracción de texto plano del documento
4. Identificación de campos clínicos mediante regex
5. Lectura directa del archivo `document.xml` para obtener valores de checkboxes
6. Construcción de registros estructurados
7. Consolidación en un `DataFrame` con Pandas
8. Exportación del dataset final a Excel

---

## 🛠️ Tecnologías utilizadas

- **Python**
  - `python-docx`
  - `re` (expresiones regulares)
  - `xml.etree.ElementTree`
  - `zipfile`
  - `pandas`
  - `os`
- **Microsoft Excel**
- **Power BI** (consumo del dataset y visualización)

---

##👤 Público objetivo

Este proyecto está orientado a usuarios con conocimientos básicos de Python, principalmente para la ejecución de scripts y navegación por directorios.

Fue desarrollado para uso personal y específico, no como una herramienta genérica ni reutilizable.

---
##📊 Caso de uso

El dataset generado fue utilizado para:

Clasificación clínica de diagnósticos
Modelado de datos (tablas de hechos y dimensiones)
Análisis epidemiológico
Visualización y reporte en Power BI
Cumplimiento de requerimientos normativos

---
##📄 Estado del proyecto

✔ Proyecto finalizado
✔ Uso único
✔ Sin mantenimiento activo
✔ No se contemplan nuevas funcionalidades

---

##🔒 Consideraciones
No se incluyen datos reales ni documentos clínicos en este repositorio.
Los archivos .docx y .xlsx están excluidos mediante .gitignore.
El código refleja una solución desarrollada bajo un contexto real y urgente.
🧾 Licencia

Uso personal.
Todos los derechos reservados.

---

##✍️ Autor

Desarrollado por **Jibran Rosas**
Proyecto creado para resolver una necesidad clínica real en un entorno productivo.
