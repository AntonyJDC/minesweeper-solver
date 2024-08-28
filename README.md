# Minesweeper Solver

Este proyecto es una herramienta de solución automatizada para el juego de Buscaminas. El código captura la cuadrícula del juego desde la pantalla, analiza el contenido de las celdas utilizando OCR (Reconocimiento Óptico de Caracteres) y luego aplica un algoritmo para determinar las celdas seguras y las posibles minas.

![Descripción de la imagen](https://i.imgur.com/9Yv8Szo.png)


## Características

- **Captura de pantalla:** El programa captura una imagen de la cuadrícula del Buscaminas desde la pantalla.
- **Procesamiento de imagen:** Convierte la imagen a escala de grises y detecta números en las celdas utilizando `pytesseract`.
- **Algoritmo de solución:** Implementa un algoritmo basado en BT-FC-DO para identificar celdas seguras y minas.
- **Visualización:** Muestra gráficamente la cuadrícula del Buscaminas con las celdas seguras y las minas identificadas.

## Requisitos

- Python
- Librerías Python:
  - `numpy`
  - `opencv-python`
  - `pytesseract`
  - `matplotlib`
- Tesseract OCR instalado:
  - Puedes descargarlo desde [aquí](https://github.com/tesseract-ocr/tesseract).

## Instalación

1. Clona este repositorio:

   ```bash
   git clone https://github.com/AntonyJDC/minesweeper-solver.git
   cd minesweeper-solver
   ```

2. Instala las dependencias:

    ```bash
    pip install numpy opencv-python pytesseract matplotlib
    ```

3. Configura la ruta de Tesseract en tu sistema:
    
    ```bash
    pytesseract.pytesseract.tesseract_cmd = r'C:\\Program Files\\Tesseract-OCR\\tesseract.exe'
    ```

4. Ajusta las coordenadas de la cuadrícula en la pantalla según tu configuración:

    ```bash
    left, top, right, bottom = 195, 356, 575, 736
    ```

## Uso

1. Ejecuta el script principal para capturar la cuadrícula del Buscaminas y procesarla:

    ```bash
    python minesweeper_solver.py
    ```

2. El programa identificará y mostrará la primera celda segura que puede ser seleccionada. Además, se resaltarán visualmente las celdas seguras y las minas en la cuadrícula.

## Notas:

- Asegúrate de que la cuadrícula del Buscaminas esté visible en la pantalla en las coordenadas especificadas antes de ejecutar el script.
- El algoritmo intenta inferir la configuración del tablero basándose en la información disponible y utilizando CSP para darle solución.
