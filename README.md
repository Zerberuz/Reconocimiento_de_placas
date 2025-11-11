# Sistema de Reconocimiento Automático de Placas Vehiculares

## Objetivo
Desarrollar un sistema capaz de detectar y reconocer automáticamente las placas de vehículos a partir de imágenes, utilizando técnicas de procesamiento digital y reconocimiento óptico de caracteres (OCR).  

---

## Descripción Técnica

El sistema se basa en **Python**, haciendo uso de bibliotecas especializadas en visión por computador y OCR para identificar la placa y extraer su alfanumérico.  

### Flujo general del sistema:

1. **Captura de imagen:**  
   El usuario selecciona una fotografía del vehículo desde el entorno del programa.

2. **Preprocesamiento:**  
   - Conversión a escala de grises.  
   - Reducción de ruido con filtros.  
   - Aumento del contraste.  
   - Binarización para resaltar la placa.

3. **Detección de la placa:**  
   - Se localiza la región de interés (ROI) correspondiente a la placa.  
   - Se emplean filtros por color (amarillo en taxis, por ejemplo) y contornos para ubicar la zona rectangular.

4. **Reconocimiento de texto (OCR):**  
   - Se aplica **Tesseract OCR** para extraer los caracteres alfanuméricos.  
   - El texto se limpia y valida con una expresión regular (tres letras + tres números).

5. **Registro de resultados:**  
   - Se guarda la información en un archivo **CSV**, junto con la fecha, hora y nombre del archivo procesado.

---

## Dependencias

Antes de ejecutar el sistema, debe tener instaladas las siguientes librerías y herramientas:

```bash
pip install opencv-python
pip install pytesseract
pip install matplotlib
pip install numpy
```

Además, debe estar instalado el motor de OCR:

```bash
sudo apt install tesseract-ocr
```

---

## Ejecución del Sistema

1. Descargar el proyecto.
2. Colocar las imágenes a procesar en una carpeta principal.
3. Ejecutar el script principal:

```python
sistema_reconocimiento_placas()
```

4. El programa solicitará seleccionar una imagen y mostrará la placa detectada.
5. Los resultados se guardarán automáticamente en el archivo `registros_placas.csv`.

---

## 🧾 Ejemplo de salida

| Fecha       | Hora     | Placa  | Archivo     |
|--------------|----------|--------|--------------|
| 2025-11-11   | 13:45:30 | UAU629 | taxi.jpg     |


---

## Autores

- **Camilo Calderin Ogaza**  
- **Elizabeth Hosten**  
- **Álvaro Negrete**

---


© 2025 – Proyecto de Reconocimiento de Placas Vehiculares.
