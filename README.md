# LicensePlate_RoboflowAPI_Filters_PaddleOCR
Este proyecto detecta la matricula de coches mediante una API gratuita de Roboflow, somete a la imagen  de la matricula de coche  detectada a una bateria de filtros y obtiene el número de la matricula de coche mediante  paddleOcr

El rendimiento, 103 aciertos en 117 imagenes de prueba, es similar al obtenido con el proyecto:
https://github.com/ablanco1950/LicensePlate_Yolov8_Filters_PaddleOCR. Ambos proyectos solo se diferencian en la deteccion de matriculas de coche, uno usa la api de Roboflow y el otro con un modelo de yolov8 entrenado con un numero reducido de imagenes de Roboflow (245 en el train)

Requisitos:

La existencia e instrucciones para operar con la api de Roboflow que detecta placas de matricula de coche se detallan en el articulo;

https://blog.roboflow.com/how-to-crop-computer-vision-model-predictions/

En el que se indica que para obtener la cuenta que implica una  API_KEY gratuita hay que dirigirse al enlace:

https://app.roboflow.com/?ref=roboflow-blog

Debera tenerse instalado paddleOcr o seguir las instrucciones que se indican en
  https://pypi.org/project/paddleocr/

pip install paddleocr

also must be installed the usual modules in computer vision: numpy, cv2, os, re, imutils, parabolic

Una vez descargados los archivos del proyecto y descomprimido el directorio test6Training.zip que contiene las 117 imagenes de prueba. Estas imagenes van nombradas con su matricula de coche, lo que permite detectar aciertos o fallos en el numero de placa detectado

Se deberá asignar en la linea 10 del programa  GetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR.py la API_KEY asignada

Se ejecutara entonces el programa:
GetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR.py

Por pantalla del monitor se indican los aciertos y fallos que se van detectando y un resumen final.

En al archivo LicenseResults.txt quedan reflejadas las matriculas detectadas y las reales.

References:

https://blog.roboflow.com/how-to-crop-computer-vision-model-predictions/

https://app.roboflow.com/?ref=roboflow-blog

https://pypi.org/project/paddleocr/


https://public.roboflow.com/object-detection/license-plates-us-eu/3



https://medium.com/adevinta-tech-blog/text-in-image-2-0-improving-ocr-service-with-paddleocr-61614c886f93

https://github.com/ablanco1950/LicensePlate_Yolov8_MaxFilters

Filters:

https://gist.github.com/endolith/334196bac1cac45a4893#

https://stackoverflow.com/questions/46084476/radon-transformation-in-python

https://gist.github.com/endolith/255291#file-parabolic-py

https://learnopencv.com/otsu-thresholding-with-opencv/

https://towardsdatascience.com/image-enhancement-techniques-using-opencv-and-python-9191d5c30d45

https://blog.katastros.com/a?ID=01800-4bf623a1-3917-4d54-9b6a-775331ebaf05

https://programmerclick.com/article/89421544914/

https://anishgupta1005.medium.com/building-an-optical-character-recognizer-in-python-bbd09edfe438

https://datasmarts.net/es/como-usar-el-detector-de-puntos-clave-mser-en-opencv/

https://felipemeganha.medium.com/detecting-handwriting-regions-with-opencv-and-python-ff0b1050aa4e

https://github.com/victorgzv/Lighting-correction-with-OpenCV
