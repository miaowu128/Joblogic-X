# PocketCoach: 
# VideoPose3D-Based Online Exercise Pose Correction Software 
## – A free exercise coach that you can meet anytime and anywhere 
Authors: Hongwen (Olivia) Song, Liankun Zou, Shuai Zhang, Dengcheng Ji, Binglin Li

# Introduction
The trend of workout-from-home has rapidly accelerated since the Covid-19 pandemic. People were forced to figure out how to exercise differently as gyms closed and remote works set in. Fitness software has thus been increasingly used when more people choose to do in-door exercise. However, based on our extensive need-finding research, we discovered that 30% of users stopped using fitness software due to its lack of coaching system to give users timely feedback. On the other hand, an exercise coaching device, Fitness Mirror, gained lots of attention recently because of its sophisticated coaching function that helps exercisers to correct their postures while doing exercise at home. However, fitness mirrors inevitably have disadvantages in portability and affordability when compared to mobile phone apps. In this project, we aim to solve the pain points of existing fitness softwares and fitness devices and improve the user experience by introducing a computer-vision-based coaching module, PocketCoach, that performs posture corrections and other related functions for exercisers that can increase user stickiness and user acquisition rate in the long term.

# Discovery summary
## Need-finding exercise 1: Naturalistic observation
The common process of using fitness software is: selecting an exercise plan -> following the video instructions to do exercise -> stopping the video -> starting another exercise plan or stopping exercise. The videos that people follow often contain audio instructions, such as “keep going, one last group” and “lift your arms higher”, in order to encourage users to keep up with the pace and have better postures. However, it is hard for users to visually be aware of their posture, especially when their major attention is on following the fast-changing video instructions.
## Need-finding exercise 2: User interview
Based on our interviews, people who have regular exercise habits and those who have just started to do more exercise think that fitness apps are helpful for them. For example, they can find abundant fitness videos and track their progress on Keep, a popular fitness app in China. However, most of them think what’s lacking is a posture correction system that can detect their postures in real-time and make warnings when their postures are not correct, such that injuries can be avoided. One of them points out that it would be great if fitness apps could automatically recognize the user’s progress and improvement and make recommendations about an exercise plan for the next step. Another interesting observation from the interviews is that people found it hard to keep up the exercise without a workout mate.
## Business value analysis
The commercial value of our product is mainly reflected in the lower price to provide users with home fitness coaching services. Most of the companies in the market that can provide such services require users to spend $1000 on hardware before they can get the coaching services they expect. Our team found that we can reduce the purchase cost of users to a great extent by storing the movement correction model in the app by means of machine learning. Improve our user acquisition ability.
For user retention, our solution was to gamify our fitness product so that users would not only have a panel to show their results after each workout through our product. They can also share their fitness progress with their friends and family to encourage them to work out. This not only provides an additional user acquisition channel, but also increases user stickiness, and through healthy competition between users to achieve their desired fitness needs.
# Brainstorming summary
A summary of the brainstorming sessions is provided below:
1.	The product can reconstruct the customer’s movements and compare with the standard ones. Suggestions will be given based on the difference.
2.	 The product can track the customer’s progress, give feedback on the improvement and encourage them to give more on the workouts
3.	 The product can extract the customer’s physical fitness and give better suggestions including this information
4.	The product can give out the warnings on the wrong movements which will lead to injuries
5.	 The product can recommend the exercise plan based on the customer’s progress and physical fitness
6.	The product allows customers to share their progress or movements with friends.
7.	The product can let two people exercise at the same time, and the product would decide who does better based on the comparison of their poseture with the instructor. 
8.	Gif diagram remains the user's next movement before the next movement starts.

# Low fidelity prototyping
## Prototype 1: Exercise Coaching (Posture Recognition, Tracking, and Correction)
Based on the unmet needs collected above, we decided to develop a system that can detect the joints and major parts of the human body and estimate the pose in real time. The users can either follow the training plan or choose the free-training mode. The system is going to show the training video of the users on the screen and detect the key points. With different training, we will set up the suggested range of angles and distances between body parts and speed of the movements. The system will evaluate the quality of the pose (static) and speed of the movement (dynamic) to the users and suggestions will be provided. The information will be recorded so users can track their progress. If free-training mode is selected, the users are allowed to do any training they want and they can control how many groups they do for each of the training poses and how long each group is. The system will classify the training pose and then provide evaluation, suggestions and record the training procedure like the other mode.
## Prototype 2: Fitness Plan Customization (Recommendation System)
In this prototyping direction, we want to develop a recommendation system to deliver suitable fitness videos for users. In order to accomplish this goal, we would use CV technology to help recommendation models estimate the tolerance of user’s exercise intensity. We will create a testing fitness series which can dynamically adjust the difficulty level for new users to evaluate the tolerance of user’s exercise intensity. Then our recommendation system will provide several fitness videos based on the testing result.
# Evaluation: user interviews on the design
## Selection Criteria
1.	Addressing crucial needs of users. The “users” can come from a wide rage, including children, old people, hard-core or professional
2.	Bringing business value. Our product should be profitable.
3.	Realizability. The product is feasible under current technologies.  
# Final product solution design
## Verbal and paper prototype
### Prototype 1:
After logging into the application, users can either choose to select a training mode to start new training or browse the training record and plans of them and their friends. There are three main modes for training: normal training mode, free-training mode and personalized training mode. Normal training sets include many class videos and training plans for different purposes (HIIT, dumb bell, stretching, yoga...). Users can choose the training sets that fit them and follow the video to finish the training. In the training, the user’s pose will be recognized and evaluated in real time. The model will be implemented to recognize the key points of the users (joints and main body parts) in three dimensions. The angles and distances among these key points will be calculated to be used as a criterion to judge if the pose/movement is correct or not. Suggestions will be provided in the form of coaches’ voice and text on screen. For the free-training mode, users can schedule their own training with any poses and movement they want. The system will classify the pose first and then evaluate the pose and give suggestions. The personalized training mode will be discussed in detail in the next subsection (‘prototype 2’). The evaluation includes the quality of the poses and if the speed of the movement is appropriate. For example, if someone lowers his/her body too fast when doing push-ups, the system will deduct points on the speed evaluation and suggest the user to slow down when lower body to fully train the muscles. These evaluation and statistical data will be recorded, users can track their static and dynamic pose quality together with the movement frequency, heart rate, training time and pose changes at different time to help them make better decisions on the future training. Users can also schedule training with friends and work out together via the system. 

![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture1.png)
![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture2.png)


### Prototype 2:
When a new user logs in, they will take a test 10 min fitness video series to evaluate their tolerance of the user's exercise intensity. During the testing, CV will help users to reflect whether their movements are correct or not via the standard action area outlined by the dotted line. After that, a result dashboard would be shown to present the user performance and the recommended video would show below.
# SWOT Analysis
In order to create thoughtful business questions for our project, we decided to use SWOT analysis to address our product features and improvements we want to achieve that compare with popular fitness APPs.
1.	Strength: We have advanced pose recognition technologies to give professional feedback for user’s movements.
2.	Weaknesses: Due to the limitation of hardware and software capabilities, our product only covers several fitness projects which have lower requirements about movement speed.
3.	Opportunities:  Current fitness products which include pose correction function are overpriced. Users want this service to be used at home with lower cost. 
4.	Threats: Physical fitness center and personal fitness coach can provide a better fitness atmosphere to encourage user exercising.

# Competing product comparison 

Another product on the market, FITURE Fitness Mirror, provides somewhat similar features as our product does. Here are some comparisons between our product and the fitness mirror.
1.	Portability: FITURE Fitness Mirror weights 60 pounds, so it’s better used in a fixed place. Our product can be used on any mobile device with a camera, so it is easy to start exercising anywhere with our product. 
2.	Affordability: FITURE Fitness Mirror costs $1,459 whereas our app is free for users. Our app will make profit by in-app advertising and subscription of advanced users.
3.	Interactivity: FITURE Fitness Mirror recognizes users exercise posture, helps counting repetitions, and corrects users’ postures in real time manner. Our product supports scoring after the users finish each set of exercises. In addition, our app provides a peer competition function that users can use to compete with friends on their accuracy when doing the same exercise.
4.	Other: FITURE Fitness Mirror has a big reflective surface from where users can easily see their postures, but the size of the interactive screen of our product depends on the device users use. Also, FITURE Fitness Mirror already has a well-established instructor video database, whereas we still need to collect related data for our product.
In summary, our product has obvious advantages in portability and price. We believe our product can be a strong competitor of FITURE Fitness Mirror if we collect sufficient instructor videos.  
# Prototype Feedbacks
After gathering feedbacks from user interviews about the prototypes and making selections based on the aforementioned selection criteria, we decided to design a mobile application that provides workout coaching and workout competitions. The reason why we head towards this direction is because both functions fulfills the crucial needs of the users, as our needing finding interviews indicated that people are concerned about whether they are doing the workout correctly in terms of posture and pace, and that lacking workout partners is a reason people stopped exercising. These two functions will be able to resolve the stated concerns. According to a well-being survey of 335,050 adults done by Gallup polls, 51.6 percent of Americans report exercising three or more days per week for at least 30 minutes, and the trend of workout-from-home is continually increasing since the Covid-19 pandemic, the market for our product is deemed to be very promising. Our proposed product is also feasible under current technologies. The main tools we need to implement our product are web services and a pose recognition model. Web services are widely available and a pose recognition model is offered by multiple open source developers. 

# Main Functions 
Our product aims to promote in-home-workout and thus will provide functions that solve common problems faced by people when exercising at home. 

The first function is to provide coaching services for users, which is mainly reflected in the single training mode of our application. When exercising in this mode the movement and poses of the users will be captured, tracked, and evaluated. The evaluation is based on the poses and movements of a professional instructor, saved in a database. 

The second function, namely, competition mode, is to provide companionship and a sense of competition to people who work out at home. In this mode, users will be connected to another user through our online services, who can be a friend or a stranger. Both competitors’ movements and poses will be tracked and evaluated in real time, against a professional instructor. Each competitor will receive a score that is calculated based on the correctness and timeliness of their movements and poses. The competitor with the higher score wins the competition.

# Product System Architecture
![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture3.png)

# Product interface
The main interface in the app shows users’ daily training schedule. For each of the sessions, users are free to set up the time, training sets, training duration and training mode by themselves. Before starting the training set, users can review the details of the training in the ‘training details’ section and add or make changes to the training set. The training mode can either be solo mode, or competing mode. In competing mode, users can send invitations to the other app users to ask them to schedule a time to workout together. The details of these two modes will be shown in the next section. Time can be set for each of the sessions so the notification can be sent to remind the users to stick with their training plans. Our app will also record users activities and give suggestions based on users’ needs and exercise habits.

![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture4.png)

## Solo mode and competing mode interface
The figure below shows the solo mode (left) and competing mode (right) interface separately. 

In solo mode, we will focus on the pos/movement correction for the users. With the interface shown on the left in the figure below, the training video from the coach is shown above and users can rotate to change the view to get more details, which is beneficial especially for users who are not familiar with the specific training. The key points will be recognized from users’ videos and labeled on users’ bodies in real time. Important parameters such as the angles and distances among joints and body parts will be calculated and compared with the standard pose/movement. When the problems are found, the body parts with problems will be labeled in red and the corresponding suggestions will be provided in the form of coaches’ voice and text on screen. 

As for competing mode, we focus more on the participants’ poses and movement so the coaches’ video is placed on the top right corner of the screen. With the similar recognition technique, we will record how fast and accurately the training sessions are finished and provide grades for each of the participants. For both of the modes, more details like the training time, pose scores, targets of the training etc. would be recorded after the training session are done so users can keep track on their training progress and health status.

![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture5.png)

# Product technical solution design
## Data
As exercisers use our module, their videos will be uploaded to our online servers to be compared with the videos of the coaches that users are learning from. The input of our module are videos in mp4 format and the output are mp4/gif files with the exercise scores added to every frame of  the original video. An average score across the video will also be generated and sent to the backend for users’ progress record.

## Backbone algorithm
The backbone algorithm is based on a pre-trained model: VideoPose3D (ref. 2). There are two steps to reconstruct a human's 3D key joints. The first step is to get the 2D key joints for each frame. This process is based on a model called Detection2(ref. 3). The second step is to take the 2D pose sequences as input and reconstruct the 3D poses for each frame by using the convolutional network. For more details, you can refer to the paper: 3D human pose estimation in video with temporal convolutions and semi-supervised training (ref. 4) 

After getting the user's 3D key joints, we need to align these key joints of each frame with the ones of the instructor before calculating the difference.  The algorithm we used is called Coherent Point Drift (ref. 5). This algorithm is a probability method, which aligns two sets of points by maximizing the likelihood. Fortunately, a python library (pycpd, ref.6) provides an implementation for us.  

## Auto-coaching Mode
By auto-coaching, we aim to construct a scoring system that can automatically compare the difference between the posture of teachers (i.e. coaches) and students (i.e. users). The main challenge is to correctly compute the difference between the postures of teachers and students, and transform the difference into a sensible score in the range of 0-100. Based on feedback from user interviews, we are aware that the importance of posture is not unified across the whole period of the exercise. In general, the faster a movement is, the more important it is. For example, maintaining a correct static posture is usually more important than correctly following a teacher's inter-posture movement when doing yoga. What’s more, it makes sense to accommodate more differences between teacher and students when the movement is very fast as it is harder for the student to keep up with the movement. 

To implement this auto-coaching module, we first utilize our backbone algorithm to extract the 3D joints of the teacher and the students. Once complete, a numpy array of 3D keypoints across all frames is created and saved to a file. The array will be of size num_framesx17x3, since we have a matrix of keypoints for each frame, there are 17 joints that are being detected, and we are detecting 3D coordinates, hence a 3 at the end. Here is a rough diagram that outlines the 3D coordinates being detected in each frame, indexed by the joints 0-based index location in the array [1]. 
 
![](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture6.png)

Before we move forward, we deploy rigid registration through an expectation maximization algorithm using the pycpd library. In short, it finds the best possible match between the student and instructor without scaling the student coordinates or changing the angles between the student's limbs in the process. Now that we have the 3D keypoints across all frames, we then create a module for correcting the student's pose in reference to an instructor. This will consist of finding the angles between adjacent limbs for the instructor and student, and then getting the sum of absolute angular differences to create an error score for a frame. For each of the frames of videos of teacher and students, we calculated such an error score that represents the absolute difference between the posture of the teacher and the student. Then we define the speed of the movements as the sum of the distances of the movement made by both hands and both feet of the teacher in one second. After that, we calculate the reciprocal of the speed to derive the dynamic importance of the movements and take the rolling average to smooth the importance scores.Then, for each frame, we multiply the error score with its importance and then scale the results to the range of 0-100 the to get the final error score. Finally, the evaluation score for each frame is 100 minus the final error score. A higher evaluation score means the student is doing better. In addition, an animation is created which shows the overlap between student and instructor, as well as the overall evaluation score for a particular frame (smoothed out across multiple frames).
![Workflow for auto-coaching mode](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture7.jpg)

## Rule-based-coaching Mode 
The Rule-based-coaching mode aims to help the user fine tune a specific part of the body in reference to the standard pose. The function works by highlighting the bodyparts/limbs that do not match the standards of the correct form. The application achieves this function by calculating the angle between the adjacent limbs that make up the subject body part at a particular moment in the set, and compare it to a predefined, standard value. If the angle is off by a certain tolerance value then the skeletal outline of the subject body part will be highlighted.
![Workflow for rule-based-coaching mode](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture8.jpg)
 
 ## Competition Mode 
Based on the scoring systems of the above two coaching modes, we developed an additional function, competition mode. For this mode, the input would be the video of two users who want to compete against each other, and then the input videos will go through the same process as that of auto-coaching or rule-based-coaching (based on user's choice) and generate two series of evaluation scores for the two input videos respectively. The user who has a higher average score will be the winner in the competition.
![Workflow for competition Mode ](https://github.com/miaowu128/Joblogic-X/blob/main/gif_demo/pictures/Picture9.jpg)

## Fine Tuning 
The model works well with the exercise with simple movements. But the movements can be complicated sometimes, especially for dancing and HIIT exercises. During exercises the body parts can rotate, move so some of the other parts are blocked from the camera. The prediction results are not accurate without most of the body parts exposed in the camera view. The popular exercise movements videos with blocked body parts can be collected and labeled so with the blocked joints can be inferred.
We plan to fine tune to improve the performance of the model if we could have more labeled data. Fine tuning process can be done to tune the model so it works better for the exercise movements. The model is composed of two main parts: 2D pose detection part for joint and temporal model with convolutional architecture for 3D pose estimation. These models will be tuned separately. Parameters that were trained in the neural network are used as initialized parameters for our model. Exercise videos with labeled joints are collected and used as training datasets.  

## Evaluation
After implementing above three main functions, we evaluate our model performance from two perspective, system testing (time complexity) and user acceptance testing (UAT)

# Solution development and results
## Model Demonstration
In the GIFs below, we demonstrate the implementation of the three functions respectively. 

## Rule-based-coaching Mode
In rule-base-coaching mode, the animation in the middle shows the joints of students, whose video is to the right. Corresponding body part will turn red when the movements of this part violate the pre-defined rules.
![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/test3.gif)
![](https://github.com/miaowu128/Joblogic-X/blob/860cf55a8889e936eea9a3d76b922b9a372a6e03/gif_demo/gifs/test4_cut.gif)

## Auto-coaching Mode
In auto-coaching mode, the animation to the right shows the joints of students, whose video is in the middle. The red joints in the animation represent the movements of students, while the blue joints in the animation represent the movements of the teacher. The speed, importance, and evaluation score of student’s movements can also be found in the animation.
![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_bl_teacher_good_student_2_compare_cut.gif)

![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_bl_teacher_bad_student_2_compare_cut.gif)
 
## Competition Mode
In competition mode, the animation to the right shows the joints of the teacher and two competing students, with blue joints in the animation representing the movements of the teacher. 

![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/gifs/output_compete_2_cut.gif))


## Time Complexity
The code is running on a desktop equipped with a GTX 1080 GPU. For the first step (2D pose detection), the speed is about 0.15 second per frame.  For a 30 second video with 30 fps, it will take 135 seconds to finish.  For the second step (3D pose estimation), the speed is about 0.1 seconds per frame. It will take  90 seconds to transform a 30 seconds video with 30 fps.

## Accuracy Evaluation

![](https://github.com/miaowu128/Joblogic-X/blob/b104064e28ca7e387128c019be683984d618faf3/gif_demo/pictures/Picture10.jpg)

In order to evaluate the performance of our algorithm, we input the videos of four people: good student 1, good student 2, bad student 1 and bad student 2. Good student 1 and bad student 1 work out on the same exercise, while the other two work out on the same exercise. On average, the scores of good students are higher. Our algorithm works.   

## User acceptance testing
According to the user’s feedback, we found 90% of users are interested in this coaching system. 60% of users not only want voice prompts like “great” , “good job”; but also want more specific instructions such as “put your palms together”, “deep breathing”. 45% of users suggest that it would be great if the software can have voice prompts rather than plain text. They want our product to be like a real coach, who steps aside, watches their movements and gives specific feedback. What’s more, one user suggested that the two kinds of scoring systems (auto-scoring and rule-based-scoring) can be confusing for users. In this case, one solution is to provide the auto-scoring system for free for all users, while for more advanced users or subscribers, we provide them with the choice of rule-based-scoring, which is more labor-heavy for the development team.

## Limitations
Our ideal product is to detect body motion and provide constructive feedback in real time. However, our prototype is only aiming to showcase the core functionalities by processing pre-recorded videos. Real time video rendering requires better hardware setups such as more powerful GPU, and more comprehensive system design to reduce latencies for online functions. This is something that can be developed and improved for the final product. 

Since our product detects the joints between the limbs of the human body from a video input, it is important to make sure that all parts of the body are placed inside the camera throughout the whole video. If the reference limbs went outside the frame the program will not be able to detect joints and will lead to incorrect results. Our product may also have difficulty in detecting the joints if the limb is hidden behind a body part. This is something that can be optimized by further training the model.
# Summary
In summary, we developed three main functions (auto-coaching, rule-based coaching, and competition mode) that aim to solve the long-standing pain points existing in traditional fitness apps and coaching devices. Compared to those two, our product has advantages in portability, affordability, and interactivity. In general, our technical solution fits our original product solution design. However, because of hardware and computation limitations, we can only implement scoring functions as non-real time functions, even though we are confident that this function has strong potential to be developed into real time analysis function given a better GPU. 

The problem we want to solve via our product is creating a virtual fitness instructor who can coach and record the fitness progresses and achievements for each user. Compared with an actual coach, we can provide insightful feedback and status reports not only pointing out the movement issues during exercising, but also highlighting the progress or movement done perfectly that can encourage users to keep exercising. All in all, we provide professional and positive feedback to help our users raise a habit in exercising for their health with lower cost.

In order to better demonstrate the business value of our product, we first gamify the entire fitness process, for example, by scoring users' movements in real time so that they can get timely feedback in the fitness process, which not only increases their motivation to exercise, but also improves the user stickiness of our product. On this basis, we can profit through a subscription or membership model. In addition to this, we also intend to build the network effect of our product by organizing users' fitness progress and achievements into images that can be shared on social media. These shareable images will be used as a social currency to attract friends and family around the user to join the community. Finally, we will use the power of the community to expand our reach and partner with companies in the fitness field to provide consulting and technical support services to maximize the value of our product.

## Next steps

          To improve the user experience, we are planning to increase the accuracy of the pose estimation. One of the biggest challenges we have is the shooting angle of the camera can not be easily changed, which causes problems when some of the body parts are blocked. The incorrectly evaluated motion are mostly with abnormal poses (reversely bent joints) and weird  repeating patterns with short period. We are building up a model to classify the abnormal body poses and temporal patterns so we can send users alert to move around so their movements can be better evaluated. The other potential choice is to have a external hardware connected with the phone so the motion can be evaluated with multiple views or adjustable angles.

           Multi-people evaluation: we are also planning to make the app able to evaluate and track movements from multiple people at the same time. In addition to the existing models, we would add the segmentation module to the algorithm to recognize and track the positions of the people in the camera view. To prevent the interference of the people who are not doing exercises, we will further use the generated joints positions to automatically classify the movements for filtering and selecting the ones that are following the training videos.

## Final thoughts 

Our prototype takes the videos of the user as the input and our final product will use the user’s camera for real time evaluation and recording. Both scenarios are deemed as the collection of user specific data. In awareness of data privacy and security, the collected video data will only be used for the coaching evaluation processing and result review. The recorded videos will be deleted afterwards to prevent information leakage. However, under user consent, we may use user videos for product optimization activities such as model training and various functional improvements.

# References
1.	https://github.com/DrJessop/yoga-pose#anglespy
2.	https://github.com/ facebookresearch/VideoPose3D
3.	https://github.com/facebookresearch/detectron2 
4.	https://arxiv.org/pdf/1811.11742.pdf 
5.	https://arxiv.org/pdf/0905.2635.pdf 
6.	https://github.com/siavashk/pycpd 

# Annex
## Appendix A – Datasets
Yoga data: 
Standard yoga image, classified by pose, 1GB: https://www.kaggle.com/shrutisaxena/yoga-pose-image-classification-dataset 
Standard yoga, 302MB: https://www.kaggle.com/datasets/niharika41298/yoga-poses-dataset 
Standard Yoga data: https://laurencemoroney.com/2021/08/23/yogapose-dataset.html 
A famous yoga data for ml: https://drive.google.com/file/d/12hySxD-piXCuCH65doUMNXNLMo-Jwt_3/view  (Derived from: https://sites.google.com/view/yoga-82/home) 
Workout Data:
Libraries of proper workout poses and instructions:
https://www.acefitness.org/resources/everyone/exercise-library/
https://www.jefit.com/exercises/
https://www.bodybuilding.com/exercises/finder/?equipment=dumbbell
https://github.com/SravB/Computer-Vision-Weightlifting-Coach

## Appendix B – Interview transcripts

Gender	Male	Female	Female
Age	59	57	27
Fitness Frequency	7/week	3-4/week	4/week
Fitness Method	Swimming, walking, elliptical trainer	elliptical trainer, running, tai chi	elliptical trainer, running, pilates
Fitness Duration	1 hour	1 hour	1 hour
Is the movement standard during fitness?	yes	no	yes
Which Access to Learn standard movement?	video	Video, coach	coach
How long did it take when you learn a standard movement?	25 hours	32 hours	10 hours
Do you always pay attention to your own movements when exercising?	no	no	yes
Does non-standard movements do much harm to your body during fitness?	no	Yes, non-standard tai chi movement is bad for knee.	no

The fourth interviewee is a cs Ph.D. student who does not regularly exercise. She usually exercises in the gym because she does not like exercising at home. When talking about the pose correction software, she said that she would be more willing to use such apps for aerobics, such as yoga and dance, rather than on fitness exercises, such as weightlifting. She thinks that having such an app would encourage her to do more aerobics at home. The reason she prefers using the app at home rather than in the public workout room is that she feels awkward when taking out her phone and facing the camera in public. What’s more, she thinks that such an app is targeting green hands, and she is not so interested mainly because she is more advanced.
The fifth interviewee is a cs Ph.D. student who exercises a lot. He majorly uses workouts as his exercise. He thinks that he exercises much less since the start of the pandemic because he cannot go to the gym as often as before. When talking about the pose correction software, he said that this software would be very helpful for people who just started to do workouts. Compared to yoga and other aerobic dances, having correct poses during a workout is much more important, so that one would not hurt himself. He expects the app to be simple, and he does not need to look at the screen all the time so that he can focus on the feeling of his muscles. All in all, he thinks that for those new starters of exercise, this pose correction function can be very helpful and people would like to try it. 
The sixth interviewee is an accountant who exercises casually. When working out in the gym she likes to use equipment such as the rowing machine, stationary bicycle, leg curl machine, and etc. She thinks the equipment are easier to use because the machine itself would sort of adjust her postures, so she won’t have to worry too much about her postures being improper.  She would try to avoid using dumbbells because she thinks those would require the users to constantly monitor their postures in order to be effective. Sometimes she worries about being injured due to improper posture, and she relies on Youtube videos to adjust her postures. She said she will definitely try out the posture correction app if there is one.
The seventh interviewee is an engineer who usually work out at home. She said she is not a hardcore exerciser, she only likes doing less intensive exercises just to keep her in shape, and she is not even sure if her exercises are effective. She prefers to exercise at home instead of going to gym because she thinks it’s more convenient for her. When asked about if she would try out an app that helps her correct her postures, she said she would, and that it will be helpful for people without training on how to exercise properly, as well as those who do not have personal trainer to monitor their exercises.
The eighth and ninth interviewees are college students with one of them graduated. Both of them are not series exercisers. They like group sports, for example, football or basketball.  Before the epidemic, they will play football or basketball at least once a week. During the epidemic, they seldom go outside. Working out at home is not a good option for them. Both of them are interested in the App which can track their movements. One of them said there were a lot of apps like this, but most of them are useless. The App would be useful if it can provide professional advice like fitness coach.
The nineth interviewee: Age 45, postdoc, male, used to work out regularly in the gym. He is a gym rat and doesn’t need too much help with pose correction. However, he mentioned that exercise tracking can be a function that is helpful (track if the pose is consistent and how the frequency of the movement changes especially for interval trainings), so it would be easier for him to track his performance on the strength and endurance. He mentioned that working out with gym mate would help him the most to keep doing exercise. It can be interesting to have a program to count the numbers of movements like pull ups and pushups so they can compete with friends. The concern from him about the system is whether it is easy to set up in different environments like home, outdoors and gym... 
The tenth interviewee: Age 28, has been working for 2 years, basketball player, likes hiking. Mainly work out with dumbbells and hiit at home. He watches hiit videos to follow the movements. For familiar movements, they are easy to follow but for some of the comprehensive training movements, he doesn’t really know whether he did them well or not. It could also be annoying to pause the video and check the pose details. The hardest part of the training for him is stretching. He has body stiffness problems but it is hard for him to keep stretching everyday without company. Training pose commendation can be an attractive function for him. After completing some of the fundamental poses without problems, it would be great to update some of the training poses with more advanced ones (personalized recommendation).



