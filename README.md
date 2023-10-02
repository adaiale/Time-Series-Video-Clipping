# Time-Series-Video-Clipping

This repo focuses on clipping skateboard videos using time series model Inception Time and a custom YOLOv8 model that focuses on people and skateboards.  The main purpose of this project is data collection for another project. 

## Data format

Using a YOLOV8 custom bounding box model, we detected bounding boxes in each frame of a skateboard video, and we labeled each frame as one of:
 #### Unknown: Either no skateboarding involved, or skateboarder is not implementing a trick.
 #### Push: Skateboarder is pushing skateboard forward.
 #### Pop: Skateboarder is in the process of popping (jumping with) the skateboard.
 #### Trick: Skateboarder is performing a trick.
 #### Landing: Skateboarder has landed said trick. (may not be needed)

Using the width and height of each detected bounding box as features, we create a time series, with each frame being a segment of the series labeled as above.

## Inception Time
I have to give credit to
### https://github.com/hfawaz/InceptionTime
 for the time series prediction model.  I am still tuning hyperparameters, and have condensed the repo into a single python file for ease of use.



## License

[AGPLv3.0](https://choosealicense.com/licenses/agpl-3.0/)
