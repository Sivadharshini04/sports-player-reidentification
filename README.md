# Sports Player Re-identification 
This project proposes a solution for the task of **player re-identification in a single feed** in the given sports footage using the fine-tuned `Ultralytics YOLOv11` based `best.pt` model.
The goal is to detect and consistently identify players in the single-camera video, even if they go out of view and reappear into frame.

---

## Assignment Task

**Re-identification in a Single Feed**

> Given a 15-second video, identify each player and ensure that players who leave the frame and reappear are assigned the same identity as before.

---

## Repository Contents
sports-player-reidentification/  
├── taskb.ipynb # Jupyter notebook  
├── output.mp4 # Sample output video  
├── requirements.txt # Python dependencies  
├── sample_outputs/ # Sample output screenshots  
└── README.md 


---

### Requirements

Main dependencies:  

  ultralytics (YOLOv11)  
  opencv-python  
  matplotlib  
  numpy  
    
## Setup Instructions

### Clone the Repository

    git clone https://github.com/Sivadharshini04/sports-player-reidentification.git
    cd sports-player-reidentification


### Install Required Packages

    pip install -r requirements.txt

### Add the Model

    Note: Due to GitHub's 100MB file limit, the model file (best.pt) is not included.

Place the provided YOLOv11 model file into the project folder.
## How to Run

Open the notebook in Jupyter:
    
    jupyter notebook taskb.ipynb

Or open with VS Code and run all cells.  
The final output video will be saved as output.mp4.

## Results:

   Players are detected and assigned bounding boxes and IDs  
   Performance is acceptable on CPU, though better optimized with GPU

## Detected limitations:
   
   Players with similar appearance may be confused  
   Only two IDs were consistently assigned (Player 0, Player 1)

## Sample Output

    You can open output.mp4 to see the video version.

# NOTE
Another approach using `OCR` to identify players using `Jersey Numbers` has also been implemented by me.  
It has been shared as a Drive Folder link.

## Author

Sivadharshini Saminathan  
github.com/Sivadharshini04
