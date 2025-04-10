Player Behaviour Analysis

This project analyzes player behavior in a football match using YOLOv5 for object detection.

Project Overview

We used YOLOv5 to detect and analyze players from a football match video. The main goal was to extract behaviors and movement patterns of players using computer vision.
	•	Input Video: matchh.mp4
	•	Detection Output: Saved in runs/detect/exp/
	•	Platform: Google Colab
	•	Detection Count: ~2833 frames analyzed
 How to Run
	1.	Open the notebook on Google Colab.
	2.	Upload the input video matchh.mp4.
	3.	Run the YOLOv5 detection cell:
 !python detect.py --source matchh.mp4 --weights yolov5s.pt --conf 0.4
 4.	Output will be saved in the runs/detect/exp/ folder.

Output Samples
	•	Detected video is saved as runs/detect/exp/matchh.mp4.
	•	You can visualize it using the following code in Colab:
 from IPython.display import HTML
from base64 import b64encode

video_path = '/content/yolov5/runs/detect/exp/matchh.mp4'
mp4 = open(video_path,'rb').read()
data_url = "data:video/mp4;base64," + b64encode(mp4).decode()
HTML(f'<video width=700 controls><source src="{data_url}" type="video/mp4"></video>')
Installation Notes

To install the required packages manually:
pip install torch torchvision torchaudio opencv-python matplotlib
## Run on Google Colab

[Open the notebook](https://colab.research.google.com/drive/https://colab.research.google.com/drive/11RMjL3hW31KnmZyUiND0WHlD7svU1wkA?usp=sharing)

 
