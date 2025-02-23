# Home-Based Yoga Self-Training Application

Implement paper： "Home-Based Yoga Self-Training Application" in 2023 CVGIP Conference

## Introduction
本論文探討如何結合硬體感測技術以及深度學習演算法，應用於擴增實境飛輪體驗系統。
在硬體方面，我們在自行車上裝設速度踏頻感測器偵測使用者騎乘的速度，並使用可變電阻偵測自行車的轉向，而非傳統的G-sensor，不但成本較低，也提升了轉向的穩定性。而軟體方面，我們使用InternImage偵測真實場景的道路範圍，再使用邊緣偵測等方法判斷道路的延伸方向，並應用YOLOv7偵測真實場景路上的人與車。
我們開發了一套結合軟硬體架構的擴增實境飛輪系統。使用者可以透過踩踏踏板與旋轉龍頭控制系統中的虛擬人物，使虛擬人物保持在兩側道路線內，並同時避開道路上的障礙物，模擬現實中的道路情況，希望能讓使用者在家中也能享受到具有挑戰與趣味性的飛輪體驗。


## Demo Video
[![Watch the video](https://i9.ytimg.com/vi_webp/bue8EUY3Pno/mq2.webp?sqp=CODT7L0G-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGH8gEygTMA8=&rs=AOn4CLCrhWVEGtCk_aU3jZ1hgy20Cou6SQ)](https://youtu.be/bue8EUY3Pno)

## Pre-Requisites
1. Clone this repository.
	```bash
	git clone https://github.com/joannhsiao/yoga.git
	```
2. Open anaconda and activate your environment.
	```bash
	conda activate your_env
	```
3. Switch to the yoga directory.
	```bash
	cd yoga/
	```
4. Install the required packages by type this command below:
	```bash
	pip install -r requirements.txt
	```
5. Download the videos from [google drive](https://drive.google.com/drive/folders/1noSRIhCsv7EMgpzv8V5nwREaCGVpt6FW?usp=drive_link), and put the video directory `video/` under `data/`.
6. Make sure the yoga mat is connected with your device.

## Notes
- Note that you could commit the part of the heatmap if you don’t need to use it or the yoga mat is not connected. Otherwise, you will get the error and the application cannot be started.

## How to Use?
- Start the yoga application using the the command below: 
	```bash
	python Application.py
	```
## File explanation
- UI
	- Calibration.py
	- Menu.py
	- PlayingSence.py
	- StartPage.py
	- TeachStage.py
- data: Some UI resource
	- image
	- music
	- video
- tools: tools for UI
- yoga_toolkit
	- JsonFile: Sample angle of each pose
		- ...
	- SampleVideo: Video used to sample pose angles
		- ...
	- AngleNodeDef.py: Define the joints used in each pose based on the joint points of the mediapipe
	- correction_toolkit.py: 
	- toolkit.py: Functions used in yogaPose.py
	- yogaPose.py: Class YogaPose contains sample function and detect function, sample function used to sample yoga pose video to json file(developer use), detect function used to receives UI frame to detect user's pose
	- yogamat.py
- Application.py: UI Main function
- README.md
- requirements.txt
- yoga_toolkit_test.py: used to test yoga_toolkit function (developer use)
