# Home-Based Yoga Self-Training Application

Implement paper： "Home-Based Yoga Self-Training Application" in 2023 CVGIP Conference

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

## Demo Video
[![Watch the video](https://i9.ytimg.com/vi_webp/bue8EUY3Pno/mq2.webp?sqp=CODT7L0G-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGH8gEygTMA8=&rs=AOn4CLCrhWVEGtCk_aU3jZ1hgy20Cou6SQ)](https://youtu.be/bue8EUY3Pno)
