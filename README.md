# **Clasificador de Imágenes con Redes Convolutivas**
___

## **Conjuntos de Datos**

Este proyecto utiliza dos conjuntos de datos distintos: uno compuesto por imágenes de piezas de ajedrez y otro por imágenes de flores. Ambos han sido empleados para explorar diferentes arquitecturas y configuraciones de redes convolutivas, con el objetivo de analizar su rendimiento en problemas de clasificación de imágenes.

---

**<h2>PIEZAS DE AJEDREZ</h2>**
<div style="text-align: center;">
    <table style="margin: 0 auto; border-collapse: collapse; width: 50%; text-align: center; border: 1px solid black;">
        <thead>
            <tr style="background-color: #000000; color: white;">
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Etiqueta (Inglés)</th>
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Etiqueta (Español)</th>
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Número de Imágenes</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Bishop</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Alfil</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">87</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">King</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Rey</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">76</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Knight</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Caballo</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">106</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Pawn</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Peón</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">107</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Queen</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Reina</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">78</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Rook</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Torre</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">102</td>
            </tr>
        </tbody>
    </table>
</div>

<p style="margin-top: 20px;">

El conjunto de datos utilizado contiene imágenes de seis tipos diferentes de piezas de ajedrez: **Alfil (Bishop), Rey (King), Caballo (Knight), Peón (Pawn), Reina (Queen) y Torre (Rook)**. Las imágenes han sido recopiladas principalmente del [conjunto de datos de Kaggle](https://www.kaggle.com/datasets/niteshfre/chessman-image-dataset/data), el cual incluye una variedad de recursos preprocesados para este tipo de proyectos. Este conjunto de datos proporciona 556 imágenes con diferentes dimensiones.

---

**<h2>FLORES</h2>**
<div style="text-align: center;">
    <table style="margin: 0 auto; border-collapse: collapse; width: 50%; text-align: center; border: 1px solid black;">
        <thead>
            <tr style="background-color: #000000; color: white;">
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Etiqueta (Inglés)</th>
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Etiqueta (Español)</th>
                <th style="border: 1px solid black; padding: 8px; text-align: center;">Número de Imágenes</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Daisy</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Margarita</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">764</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Dandelion</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Diente de León</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">1052</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Rose</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Rosa</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">784</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Sunflower</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Girasol</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">733</td>
            </tr>
            <tr>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Tulip</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">Tulipán</td>
                <td style="border: 1px solid black; padding: 8px; text-align: center;">984</td>
            </tr>
        </tbody>
    </table>
</div>

<p style="margin-top: 20px;">

El conjunto de datos utilizado contiene imágenes de cinco tipos de flores: **Margarita (Daisy), Diente de León (Dandelion), Rosa (Rose), Girasol (Sunflower), Tulipán (Tulip)**. Las imágenes han sido recopiladas principalmente del [conjunto de datos de Kaggle](https://www.kaggle.com/datasets/alxmamaev/flowers-recognition/data), el cual incluye una variedad de recursos preprocesados para este tipo de proyectos. Este conjunto de datos proporciona 4317 imágenes con dimensiones de 320x240 píxeles.

---

## **Análisis de resultados**

### **Conjunto de Piezas de Ajedrez**

| Clasificador          | Loss (Train) | Loss (Test) | Accuracy (Train) | Accuracy (Test) | Observaciones                                                                 |
|-----------------------|-------------------|------------------|-------------------|------------------|--------------------------------------------------------------------------------|
| **Sin parada temprana**| 0.0013           | 6.8532           | 100.0%            | 34.23%           | Presenta un alto sobreajuste con precisión limitada en los datos de prueba.            |
| **Con parada temprana**| 0.5773           | 2.5704           | 79.59%            | 33.33%           | Mejora el control del sobreajuste, pero no generaliza bien a datos nuevos.             |
| **4 capas convolutivas**| 0.7976          | 2.0862           | 70.52%            | 38.74%           | Logra una mejor precisión, aunque las confusiones entre clases persisten.             |
| **6 capas convolutivas y Dropout**|  1.7495              | 1.7752              | 25.85%               | 18.02%              | Dropout reduce el sobreajuste, pero la precisión sigue siendo baja. |
| **ResNet-18**         | 0.1250             | 0.2687          | 96.15%               | 90.99%              | Excelente rendimiento, minimizando errores en la mayoría de las clases. |

### **Conjunto de Flores**

| Clasificador          | Loss (Train) | Loss (Test) | Accuracy (Train) | Accuracy (Test) | Observaciones                                                                 |
|-----------------------|-------------------|------------------|-------------------|------------------|--------------------------------------------------------------------------------|
| **Sin parada temprana**| 0.0038           | 2.2678           | 99.86%            | 67.13%           | Muestra sobreajuste, afectando su capacidad de generalización.             |
| **Con parada temprana**| 0.1230           | 1.3885           | 96.52%            | 65.28%           | Controla el sobreajuste, pero su precisión no mejora significativamente.             |
| **4 capas convolutivas**| 0.1387          | 1.1888           | 95.25%            | 72.11%           | Mejor balance entre aprendizaje y generalización en comparación a modelos previos.            |
| **6 capas convolutivas y Dropout**|  0.2748             | 1.1449              | 90.56%               | 69.10%              | Dropout mejora la generalización, pero las confusiones aumentan. |
| **ResNet-18**     | 0.1796             | 0.6609          | 94.15%               | 81.71%              | Alto rendimiento con una notable reducción de errores en las predicciones. |
| **VGG-16**        | 0.0921             | 0.5434          | 96.84%               | 85.18%              | Ofrece el mejor rendimiento global con gran precisión y generalización.|

---

## **Autores** ✒️

* **Hernández Guerra, Luna Yue** - [lunahernandez](https://github.com/lunahernandez)
* **Casimiro Torres, Kimberly** - [Kimberlycasimiro](https://github.com/Kimberlycasimiro)

#### **Universidad de Las Palmas de Gran Canaria (ULPGC)**