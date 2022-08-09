# finalProject
Here are the instructions to run the project

In the first place you have to clone this repository into your jetson nano in their home
<poner una imagen de donde va> ![image](https://user-images.githubusercontent.com/110059119/183576365-a72423a8-176d-4afd-86d6-1291cb619949.png)


Whit the comand 
git clone https://github.com/FranLlam/finalProject.git

Make sure that the directories are like that
![image](https://user-images.githubusercontent.com/110059119/183576537-8a40a242-3d82-4b41-a678-8ac0c73d4937.png)
![image](https://user-images.githubusercontent.com/110059119/183576622-436a7699-86fa-4e4d-9bdd-623cbdbd97ac.png)
![image](https://user-images.githubusercontent.com/110059119/183579141-6b90ac46-138c-4b61-b715-81d3d5f6286b.png)




Before leaving gitHub, download the 4 files into your nano

https://drive.google.com/file/d/1Iwz9hKfQSeUu-liyrTE3HNYB38pFhv8t/view?usp=sharing
https://drive.google.com/file/d/1Rrzzrb-tDRIIsGUqedW6CFAUEsNiCabF/view?usp=sharing
https://drive.google.com/file/d/1SuiwUc_fnoWYwuFSx_q2gY3VbtZAJb2a/view?usp=sharing
https://drive.google.com/file/d/145w6e79mPTDm_ai-6snDpnmrykKp98OG/view?usp=sharing

After download it into your nano, you will see the files in the downloads of your nano, cut them from downloads to this path in your nano monkeypoxtrailer/models/myModel and in this place paste it
![image](https://user-images.githubusercontent.com/110059119/183577499-1e0b8fde-107b-4152-86e2-42dab549f919.png)
![image](https://user-images.githubusercontent.com/110059119/183576863-95cfd7fd-4c80-494d-a556-581702c114f3.png)

Put this comand in the terminal to enter in the directory of the project

cd monkeypoxtrailer



In this directory set the next variables before running the project

NET=models/myModel

DATASET=data/my-recognition
![image](https://user-images.githubusercontent.com/110059119/183577930-78df9e4d-d58e-4b8b-bab2-64061fae17d2.png)


Then run the next comand to see the magic of AI 

python3 monkeypox3.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt /dev/video0
![image](https://user-images.githubusercontent.com/110059119/183578076-b01bf94b-feba-4236-92e7-cbd6a6f8b6c8.png)


In the last part it is important that make sure what kind of camera do you have (usb or CSI) and put your device. 
![image](https://user-images.githubusercontent.com/110059119/183578627-90c98eb3-de4d-4de7-9c4c-64369de2d104.png)

Make sure that the camera focus rigth in the skin, If you can put the camera closer the skin, It will classificate it better. 
