# Survey-Bot
NVIDIA academy project
Surveyor bot is a model that was with the "Different Terrain Types Classification" dataset by Durgesh Rao, which includes 799 images for each of four terrains—desert, forest, mountain, and plains. With Surveyor-Bot, one can skip the paperwork and automate the tedious work of land surveying!
> ![forest_008](https://github.com/user-attachments/assets/947d0e69-6ece-4298-bb31-913984f86125)

>Example training image
>  https://transportation.ky.gov/DistrictFour/Documents/KY251_Header%20Exhibit%203_ROW%20Info%20Mtg.pdf
># The Algorithm
>This model is a version of the resnet 18 convolutional neural network. ResNet-18 is a deep network that uses shortcuts to improve training. It has multiple stages with increasing filters and combines convolutional and residual blocks for better performance. The dataset that I fine tuned it with had a wide variety of satellite images of forests, deserts, plains and mountains. 
> # Downloading Instructions
1. Procure a Jetson Nano
2. Download the Jetson-Infrence library and Python 3 on to your Jetson nano
3. Create a folder named Survey-Bot inside your Jetson Nano, you can nam3e it anything
4. Go to the ResNet-18 model and dowload into the folder you just created 
> https://drive.google.com/file/d/1o6ZZfzubkEFxpqkgM5PF92GROECNXe4W/view?usp=sharing
5. Also download the labels into the same folder
> https://drive.google.com/file/d/1wHJMsfM20P0-p2eEazCpACeOxukZ6ii4/view?usp=sharing
6. Inside your folder create a folder named Images
7. Download any images you want to put thrugh survey bot into that folder
8. Go back to Survey-Bot and run this command in the command terminal
> imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=labels.txt"images/Survey-Bot/{file_name} output.jpg
>  # Demo Video
>  https://youtu.be/LlVTJG_UidQ
