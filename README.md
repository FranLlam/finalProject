# finalProject
Here are the instructions to run the project

In the first place you have to clone this repository into your jetson nano in their home
<poner una imagen de donde va>

Whit the comand 
git clone https://github.com/FranLlam/finalProject.git

Make sure that the directories are like that


Before leaving gitHub, download the 4 files into your nano
https://drive.google.com/file/d/1Iwz9hKfQSeUu-liyrTE3HNYB38pFhv8t/view?usp=sharing
https://drive.google.com/file/d/1Rrzzrb-tDRIIsGUqedW6CFAUEsNiCabF/view?usp=sharing
https://drive.google.com/file/d/1SuiwUc_fnoWYwuFSx_q2gY3VbtZAJb2a/view?usp=sharing
https://drive.google.com/file/d/145w6e79mPTDm_ai-6snDpnmrykKp98OG/view?usp=sharing

After download it into your nano, you will see the files in the downloads of your nano, cut them from downloads to this path in your nano monkeypoxtrailer/models/myModel and in this place paste it
 
Put this comand in the terminal to enter in the directory of the project

cd monkeypoxtrailer



In this directory set the next variables before running the project

NET=models/myModel

DATASET=data/my-recognition

Then run the next comand to see the magic of AI 

python3 monkeypox3.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt /dev/video0

In the last part it is important that make sure what kind of camera do you have (usb or CSI) and put your device. 

Make sure that the camera focus rigth in the skin, If you can put the camera closer the skin, It will classificate it better. 
