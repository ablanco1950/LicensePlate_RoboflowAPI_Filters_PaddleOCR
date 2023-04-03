# LicensePlate_RoboflowAPI_Filters_PaddleOCR
This project detects the car license plate through a free Roboflow API, submits the detected car license plate image to a battery of filters and obtains the car license plate number using paddleOcr

The performance, 103 hits in 117 test images, is similar to that obtained with the project:
https://github.com/ablanco1950/LicensePlate_Yolov8_Filters_PaddleOCR. Both projects only differ in the detection of car license plates, one uses the Roboflow api and the other with a yolov8 model trained with a small number of Roboflow images (245 in the train, not augmented).

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

The video version is also included:

VIDEOGetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR_Demonstration.py (also needs to put the API_KEY in instruction 11)

operating on the attached video:

Traffic IP Camera video.mp4

downloaded from project: https://github.com/anmspro/Traffic-Signal-Violation-Detection-System/tree/master/Resources

In its execution, on the monitor screen, the detected license plates are detailed with a summary at the end, and images with delected plates

forming a video.

Three files are obtained:

VIDEOLicenseResults,txt with the registration of license plates detected with a lot of noise.

VIDEOLicenseSummary.txt with the following results, which seem pretty tight as can be seen visually from the video.


A8254S snapshots: 44 Duration = 86.52198147773743

AR606L snapshots: 5 Duration = 4.421922922134399

AE670S snapshots: 5 Duration = 6.123754978179932

AV6190 snapshots: 5 Duration = 6.075385808944702


The first field is the license plate detected and the second is the number of snapshots of that license plate.

As a maximum number of snapshots of 5 has been set (LimitSnapshot=5 parameter in the program), to avoid noise, the license plates of the cars A3K961 and AP8I88 do not appear (although it can be verified that they have been recorded in the VIDEOLicenseResults.txt registry file)

The program is prepared to run in a time of 800 seconds (parameter: TimeLimit) so you have to wait that time until it ends or pres the q key.

The results are different but similar to those obtained in the project https://github.com/ablanco1950/LicensePlate_Yolov8_Filters_PaddleOCR

The video demonstration.mp4 is also produced, which allows evaluating license plate recognition in a more apparent way.

Two videos of test results: demonstration1.mp4 and demonstration2.mp4 are attached.

More precise and exploitable results, although less apparent and more slowly, are obtained by executing VIDEOGetNumberInternationalLicensePlate_RoboflowModel_Filters_PaddleOCR.py

Other test videos can be downloaded from the addresses indicated in the program and in the references section.


References:

https://blog.roboflow.com/how-to-crop-computer-vision-model-predictions/

https://app.roboflow.com/?ref=roboflow-blog

https://pypi.org/project/paddleocr/

https://public.roboflow.com/object-detection/license-plates-us-eu/3

https://medium.com/adevinta-tech-blog/text-in-image-2-0-improving-ocr-service-with-paddleocr-61614c886f93

https://machinelearningprojects.net/number-plate-detection-using-yolov7/

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

https://medium.com/@yyuanli19/using-mnist-to-visualize-basic-conv-filtering-95d24679643e

Projects with videos to download to test:

https://github.com/anmspro/Traffic-Signal-Violation-Detection-System/tree/master/Resources "Traffic IP Camera video.mp4"

https://github.com/hasaan21/Car-Number-Plate-Recognition-Sysytem "vid.mp4"

//www.pexels.com/video/video-of-famous-landmark-on-a-city-during-daytime-1721294/ "Pexels Videos 1721294.mp4"
