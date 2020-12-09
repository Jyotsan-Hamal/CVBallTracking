# Basketball Tracking 🏀⛹🏻‍♀️⛹🏿‍♂️

Created by [Brett Fazio](http://linkedin.com/in/brett-fazio/) and [William Chen](https://www.linkedin.com/in/william-chen-6474a216b/)

![](assets/bron.gif)

![](assets/davis.gif)

## Overview

## Requirements 

The libraries to run the code are cv2, numpy, pandas, and h5py (if trying to run/evaluate on the A2D dataset). 

Additionally access to the YOLO tracker is required but this is already included in the `/src/yolo` folder. However, you must download the weights for the YOLO model. It can be done as follows:

```
cd src/yolo/weights
cd weights/
bash download_weights.sh
```

To run on the A2D dataset, the Release of the dataset itself is also required. It is available [here](https://web.eecs.umich.edu/~jjcorso/r/a2d/) and the unzipped folder entitled `Release` should be placed in the `/a2d` directory.

## Usage

The main entry point for this project is `main.py`. To avoid errors, please run it from the `src` directory. 

The most basic usage for the project would be to run on a single input video. It can be done as follows:

```
python3 main.py --video PATH
```

Where `PATH` is a path to a video file, for example:

```
python3 main.py --video ../sample_data/lebron_on_court.mp4
```

### Forward Pass Only
![](assets/forwards.gif) 

### Track Backwards + Forwards
![](assets/full.gif)

## References / Credit

This project builds on the work of eriklindernoren's PyTorch Yolo implementation as a base, specifically the pre-trained model. The repo can be found [here](https://github.com/eriklindernoren/PyTorch-YOLOv3).
