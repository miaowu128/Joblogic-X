# Joblogic-X
This is a repository that contain the codes for the computer vision projects for Joblogic-X.

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

## Model Demonstration (Please refer to the full report for more demo)
In the GIFs below, we demonstrate the implementation of the three functions respectively. 

### Rule-based-coaching Mode
In rule-base-coaching mode, the animation in the middle shows the joints of students, whose video is to the right. Corresponding body part will turn red when the movements of this part violate the pre-defined rules.
![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/test3.gif)
![](https://github.com/miaowu128/Joblogic-X/blob/860cf55a8889e936eea9a3d76b922b9a372a6e03/gif_demo/gifs/test4_cut.gif)

### Auto-coaching Mode
In auto-coaching mode, the animation to the right shows the joints of students, whose video is in the middle. The red joints in the animation represent the movements of students, while the blue joints in the animation represent the movements of the teacher. The speed, importance, and evaluation score of student’s movements can also be found in the animation.
![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_bl_teacher_good_student_2_compare_cut.gif)
![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_bl_teacher_bad_student_2_compare_cut.gif)
 
### Competition Mode
In competition mode, the animation to the right shows the joints of the teacher and two competing students, with blue joints in the animation representing the movements of the teacher. 

![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_compete_2_cut.gif)


# License
This project is licensed under the terms of the MIT license
