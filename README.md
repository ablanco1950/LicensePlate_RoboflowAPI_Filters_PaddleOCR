# LicensePlate_RoboflowAPI_Filters_PaddleOCR
This project detects the car license plate through a free Roboflow API, submits the detected car license plate image to a battery of filters and obtains the car license plate number using paddleOcr

The performance, 103 hits in 117 test images, is similar to that obtained with the project:
https://github.com/ablanco1950/LicensePlate_Yolov8_Filters_PaddleOCR. Both projects only differ in the detection of car license plates, one uses the Roboflow api and the other with a yolov8 model trained with a small number of Roboflow images (245 in the train).

Requirements:

The existence and instructions to operate with the Roboflow API that detects car license plates are detailed in the article;

https://blog.roboflow.com/how-to-crop-computer-vision-model-predictions/

In which it is indicated that to obtain the account that implies a free API_KEY you must go to the link:

https://app.roboflow.com/?ref=roboflow-blog

You must have paddleOcr installed or follow the instructions indicated in
https://pypi.org/project/paddleocr/

pip install paddleocr

Also must be installed the usual modules in computer vision: numpy, cv2, os, re, imutils, parabolic

Once the project files have been downloaded and unzipped the test6Training.zip directory that contains the 117 test images( These images are named with their car license plate, which allows  to detect hits or misses in the detected license plate number):

Line 10 of the GetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR.py program must be assigned the assigned API_KEY

The program will then be executed:
GetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR.py

The successes and failures that are being detected and a final summary are indicated on the monitor screen.

The LicenseResults.txt file shows the detected and real license plates.

References:

https://blog.roboflow.com/how-to-crop-computer-vision-model-predictions/

https://app.roboflow.com/?ref=roboflow-blog

https://pypi.org/project/paddleocr/

https://public.roboflow.com/object-detection/license-plates-us-eu/3

https://medium.com/adevinta-tech-blog/text-in-image-2-0-improving-ocr-service-with-paddleocr-61614c886f93

https://github.com/ablanco1950/LicensePlate_Yolov8_MaxFilters

filters:

https://gist.github.com/endolith/334196bac1cac45a4893#

https://stackoverflow.com/questions/46084476/radon-transformation-in-python

https://gist.github.com/endolith/255291#file-parabolic-py

https://learnopencv.com/otsu-thresholding-with-opencv/

https://towardsdatascience.com/image-enhancement-techniques-using-opencv-and-python-9191d5c30d45

https://blog.katastros.com/a?ID=01800-4bf623a1-3917-4d54-9b6a-775331ebaf05

https://programmerclick.com/article/89421544914/

https://anishgupta1005.medium.com/building-an-optical-character-recognizer-in-python-bbd09edfe438

https://datasmarts.net/en/how-to-use-the-keypoint-detector-mser-in-opencv/

https://felipemeganha.medium.com/detecting-handwriting-regions-with-opencv-and-python-ff0b1050aa4e

https://github.com/victorgzv/Lighting-correction-with-OpenCV
