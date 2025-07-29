# ViziStock

## Python virtual environment
Create a python virtual environment:
- ```python -m venv vizistock```  
Activate the virtual environment:  
- Windows
  - ```vizistock\Scripts\activate```
- MacOS
  - ```source vizistock\bin\activate```

## Install required python packages
- ```pip install -r requirements.txt```

## Running Qwen 2.5 VLM
**Note: Make sure you are logged in to the VPN in order to access the VLM endpoint.**
- The VLM is called using the ```generate_vision``` function in uw_vlm.py
- The function accepts 3 parameters:
  - Prompt: LLM prompt to provide instructions to the VLM
  - Image path: Path to the image that you want to provide to the VLM
  - Fast: Choosing between Qwen and another model (set fast=False to use Qwen)
- Once you configure the parameters in uw_vlm.py
  - Run ```python uw_vlm.py``` in the command line to run the program

## Running YOLO
- Go into the yolo folder ```cd yolo```
- Run ```python yolo_webcam.py``` in the command line to run the program
- Notes:
  - There are models defined at the top of the script. You can test with any of these or choose another from the documentation.
  - You may need to edit the webcam resolution set on lines 14 and 15
    - ```cap.set(3, 1280)```
    - ```cap.set(4, 720)```
  - If you want to run the model on your Nvidia GPU set device='cuda' on line 43
    - ```results = model(frame, device='cuda')```

## Running SAM
- Go into the yolo folder ```cd sam```
- Run ```python sam_webcam.py``` in the command line to run the program