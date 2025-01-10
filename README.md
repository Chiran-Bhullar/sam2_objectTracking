# SAM2 Real-Time Detection and Tracking

This repository adapts **[SAM2](https://github.com/facebookresearch/sam2)** to include real-time multi-object tracking. 
It allows users to specify and track a fixed number of objects in real time, integrating motion modeling 
from **[SAMURAI](https://github.com/yangchris11/samurai)** for improved tracking in complex scenarios.  

### About SAM2
**SAM2** (Segment Anything Model 2) is designed for object segmentation and tracking but lacks built-in capabillities 
for performing this in real time.

### About SAMURAI
**SAMURAI** enhances SAM2 by introducing motion modeling


## Key Features

- **Real-Time Tracking**: Modified SAM2 to track a fixed number of objects in real time.
- **Motion-Aware Memory**: SAMURAI leverages temporal motion cues for robust object tracking without retraining or fine-tuning.

The core implementation resides in `sam2_object_tracker.py`, where the number of objects to track must be specified during instantiation.

---

# Setup Instructions

### 1. Create Conda Environment
```bash
conda create -n safetyWhat python=3.11
```

### 2. Clone SAM2 Realtime Repo
```
git clone https://github.com/zdata-inc/sam2_realtime
```

### 2. Install SAM2
```
cd sam2_realtime
pip install -e .
pip install -e ".[notebooks]"
```


### 4. Download SAM2 Checkpoints
```bash
cd checkpoints
./download_ckpts.sh
cd ..
```

---

## Usage
### Demo
Run the demo notebook to visualize real-time SAM2 object tracking in action:  
`notebooks/video_tracker.ipynb`
