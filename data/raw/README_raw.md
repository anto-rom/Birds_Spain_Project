# Raw Data (DWCA - Wildlife Sounds Birds)

Esta carpeta está destinada a los datos originales del proyecto.  
**Los archivos no se incluyen en el repositorio debido a su gran tamaño**:

- `Occurrence.txt`  
- `Multimedia.txt`

Ambos provienen del Darwin Core Archive (DWCA) publicado por Biodiversity Data Netherlands.

---

## Descarga de los datos originales

Los datos pueden descargarse desde el siguiente endpoint oficial:

https://api.biodiversitydata.nl/v2/specimen/dwca/getDataSet/wildlife-sounds-birds

Este enlace devuelve un archivo ZIP que contiene:

- `Occurrence.txt`
- `Multimedia.txt`
- `meta.xml`
- `eml.xml`

---

## Descripción general de los archivos

### **Occurrence.txt**
Contiene información taxonómica, geográfica y temporal sobre registros de aves:
- id, occurrenceID  
- scientificName, genus, family  
- latitudeDecimal, longitudeDecimal  
- eventDate, eventTime  
- behavior, sex, lifeStage  

### **Multimedia.txt**
Contiene información de archivos multimedia asociados a las observaciones:
- CoreId (relación con Occurrence.id)  
- Identifier (URL del audio)  
- type (generalmente “Sound”)  
- Rating (calidad del audio)

---

## Reproducir el pipeline

Una vez descargado el ZIP:
1. Extraer el contenido en la carpeta `raw/`
2. Ejecutar el notebook `notebooks/00_preparación.ipynb`
   para generar el dataset procesado (`birds_spain_joined.csv`) filtrado a España.

---

## Nota
Los datos permanecen bajo la licencia indicada en el archivo `eml.xml`.  
Este repositorio solo almacena **datos procesados**, no los archivos RAW completos.
