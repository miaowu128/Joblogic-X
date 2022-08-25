# Joblogic-X
This is a repository that contain the code for two data science projects (recommender systems and computer vision) while working for Joblogic-X.

# Instruction 
This directory contains the backbone algorithms for exercise coaching and codes used to generate the demo. There are three inputs:
1. video
2. 2D pose estimation 
3. 3D pose estimation
2D pose and 3D pose models refer to the pre-trained model, VideoPose3D (https://github.com/facebookresearch/VideoPose3D)

# Directory and files
1. auto_score: codes for generate demo of autoScore or competition. 
    + commom: codes for preprocess (most comes from VideoPose3D)
    + input_video: the videos for input
    + output_data_2d: 2d pose estimation 
    + output_joints: 3d pose estimation
    + output: the output of the demo
    + angles.py, angles_ol.py, angles_org.py: algorithm calculating the difference between two 3D pose 
    + animation_compare.py: code for generating animation
    + pose_match.py: code generating demo of autoScore. To run just type: `python pose_match.py`
    + competition.py: code generating demo of competition. To run just type: `python competition.py`
2. rule_based: codes for generate demo of rule based. The code structure is similar to auto_score
3. Group2-Project2-Final Report.pdf: the final report for this project
# Demo Sample (Please refer to the full report for more demo)
Below shows the animation of rule-base-coaching mode. The animation in the middle shows the joints of students, whose video is to the right. 
![](https://github.com/miaowu128/Joblogic-X/blob/23ab2cee6f7c661902f6bae447e9222a7f8c7081/gif_demo/gifs/test3.gif)

# License
This project is licensed under the terms of the MIT license
