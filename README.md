# Difference-between-YOLO-models-on-raspberry-Pi
Difference in testing time between two YOLO models (YOLOv3&amp;&amp;YOLOv3 tiny)
## Overall Discription
as mentioned before in recognizing LP [link](https://github.com/behnoudshafizadeh/License-Plate-Detection-using-Raspberry-PI-YOLOV3-), so we use another light-weight version of YOLOv3 model as tiny YOLOv3 to reduce the processing time in tiny version rather than basic YOLOv3 model. it means that you can have a real time system using tiny YOLOv3 , however you see the weak bounding boxes in localizing image objects because the YOLOv3 has a stronger (deeper layer) feature extractor rather than tiny version counterpart.you see the facts resulted by inventor of yolo models [darknet](https://pjreddie.com/darknet/yolo/) in below figures :

![why tiny](https://user-images.githubusercontent.com/53394692/130930060-da809f8c-2809-4332-b37a-c2caf0e9a7d9.PNG)

furthermore, you see the comparison between 2 versions, it shows that the YOLOv3 has a higher FPS (Frame Per Seconde) while has a large weight file rather tiny YOLOv3.

![comparison](https://user-images.githubusercontent.com/53394692/130930286-9233291c-9380-4749-adfc-d54e19ef6776.PNG)

and in this figure, you can see the difference between 2 architectures. the tiny YOLOv3 has `Darknet-19` as feature extractor while yolov3 has `Darknet-53` in its architecture.

![difference between yolov3 and tiny-yolov3 models](https://user-images.githubusercontent.com/53394692/130960721-1ee59a92-b091-4c0e-9aa7-cebdb68934f4.PNG)


## Tesing phase 
for comparising two versions, we applied both of them in our command line,such as below :

* YOLOv3 for detecting LPs:

![yolov3-lp-time](https://user-images.githubusercontent.com/53394692/130958164-ee2fb977-a3f9-4808-8b98-3df395d38b9e.PNG)
* tiny YOLOv3 for detecting LPs:

![tinyyolov3-lp-time](https://user-images.githubusercontent.com/53394692/130958175-e2ec33cb-abfa-460c-9979-37f8eb9643ce.PNG)

* YOLOv3 for detecting characters :

![yolov3-char-time](https://user-images.githubusercontent.com/53394692/130958249-195b1ff6-4a32-4ba2-99c4-9682bd7b852e.PNG)

## Conclusion
*If you want better accuracy, you use yolov3,but the time consumption is high(because of size of neural networks, number of layers, parameters,...)

* If you want better accuracy, you use tiny-yolv3,but the accuracy for estimating of bounding box is weak(because of having smaller network,weak feature extractor,small number of layers,…)

* you can see the comparison in the below table that it shows tiny YOLOv3 has a better performance in time :

![comparison between yolov3 and tiny yolov3](https://user-images.githubusercontent.com/53394692/130962081-94969e0c-46fc-4f59-b3c1-b34a7bf4c195.PNG)
 
while, you see the better bounding box localization when you compare these results :

|                         YOLOv3                                      |      tiny YOLOv3     | 
| ------------------------------------------------------------------- | -------------------- |
|  ![yolov3-a](https://user-images.githubusercontent.com/53394692/130963043-00f9a597-268e-4052-b0f5-68d964f8305c.png)  |  ![tiny yolov3-a](https://user-images.githubusercontent.com/53394692/130963311-702d8ba8-92ff-423e-a92f-0a5cb7eebeb5.png)  |
|  ![yolov3-b](https://user-images.githubusercontent.com/53394692/130963167-f45661af-f1bb-4e25-a098-428c2d342a8f.png)   |  ![tiny olov3-b](https://user-images.githubusercontent.com/53394692/130963236-227e64d6-dfa9-4ca8-8ecb-43e13988c28e.png)  |
































