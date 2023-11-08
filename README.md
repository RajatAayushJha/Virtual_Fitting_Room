# Virtual_Fitting_Room

## Report : 
https://drive.google.com/file/d/1dWKWZ_4AkLLFX5jjrNk6bEWGkGo1T8-9/view
## Demo : 
https://drive.google.com/file/d/1PXJFkb-dNqZaWAmx3GgAA1xgYt0LsgLY/view

## Required Software’s and Dependencies:

1. Unity 3D.
2. openCv DLLs
## Description
An Augmented Reality Virtual fitting room allows customers to virtually try on clothes and accessories items before buying it,
made using Unity (C#) and OpenCV.

## Process 

#### Mapping model to the user body

Fitting process is done by using Iterative closest point (ICP) algorithm to transform the three dimensional model to the joints of human body.
The algorithm iteratively revises the transformation (combination of translation and rotation) needed to minimize an error metric, usually a distance from the source to the reference point cloud, such as the sum of squared differences between the coordinates of the matched pairs.

Now, to finally place the model on the user's body, the coordinates of ICP transformation are set to the anchors of model.

The following 2 transformational components are then set and passed to Unity,
1. **Position**: The model is placed on the position of body joints
2. **Rotation**: The model is rotated by an angle equal to the angle made by the joints of human body

## How it works?

1. Run ```virtualFittingRoom.exe```  OR run ```/Assets/FittingRoom.unity``` to open it in edit mode.
1. Stand in front of the Kinect sensor and open your arms as T-Pose to be in control.
1. the controllers will be moved depending on the movement of your hands.
1. move the controller to select your gender; male/female.
1. according to your gender a list of clothes and accessories items will be shown in different categories.
1. you can select different items from different categories to be fit in your body.
1. you can resize the item by clicking on plus and minus button.
1. you can change the texture of the item by select one of the texture in the textures list.
