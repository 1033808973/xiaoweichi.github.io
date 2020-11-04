Xiaowei Chi


# EDUCATIONS
■	Educations
Beijing University of Posts and Telecommunications, Beijing, China			         09/2017-present

Bachelor of Engineering, Internet of Things

Major GPA: 4.00/4.00

# COURSEWORK & SKILLS
■	Curriculum Highlights

■	Probability Theory and Stochastic Process, Mathematical Models, Discrete Mathematics, Big Data Technology and Application, Data Structures, Database, Java Programming, Programming Practice, Digit Circuit and Logic Design

■	Software Operation

-	  Python, C, Java, MATLAB, PyTorch, TensorFlow

# RESEARCH EXPERIENCES
## Part-time Research Assistant                                                                                                     07/2019 –11/2020                                                                                                                                                                                                                                                                                                                                                                                                                                                            
Supervisor: Guoqi Li

Investigation on Removing Batch Normalization for Efficient Full 8-bit Integer DNN Online Training
### Step One:
■	Reproduction and Exploration of Thesis

-	8-bit Quantization

--	Referred to the paper's method and trained the ResNet network with ImageNet data set in the 8-bit data stream.

--	Utilized direct Quantization, constant Quantization, shift Quantization and other quantitative methods to quantize the data from 32-bit to 8-bit based on WAGEUBN, and observed the impact of the data stream.

•	Deep Neural Network without Batch Normalization (BN)

-	Applied Tensorflow to reproduce FixupNet and obtained the identical results as the original paper with ImageNet data set.
### Step Two:
■	Model Fusion based on 8-bit and without BN

•	Migrated all the quantitative methods mentioned above to FixupNet and screened the current quantitative methods by control variable method.

•	Utilized quantization methods based on WAGEUBN to quantize the parameters in FixupNet, it is found that the accuracy of 8-bit DNN without BN has little influence. 

•	Quantified the whole forward propagation and backward propagation to 8-bit respectively.

•	For the backward propagation, the scale error needed to utilize additional flag quantification method, and then tested the model to get the training method with the least impact on accuracy. 
### Step Three:
■	Feasibility Verification and Analysis

•	Analyzed the L2 normal form of gradient updating to find the network reaches block dynamic isometry (BDI) when the average trace of the Jacobian matrix of each block approaches to 1.

•	Analyzed the ResNet with BN and FixupNet without BN with mathematical theory, and they both reached BDI.

•	For the shortcomings of BN in small batch size, and the network without BN can be trained in small batch size for theoretical proof. And utilized ResNet-110 to verify the above content. 
### Step Four:
■	Result

•	Compared with ResNet-34 and ResNet-50, the accuracy of 8bit-Fixup34 and 8bit-Fixup50 models is only 1.69% and 3.46% lower than the former.

•	For ResNet-110 network models with different batch (1, 2, 4, 8,128), the accuracy of the model with BN is 22.74%, 85.05%, 88.41%, 90.36% and 92.84%, respectively, while without BN is 89.41%, 92.74%, 93.11%, 93.13% and 92.98%.

■	Conclusions

•	Batch Normalization can be replaced by appropriate initialization in the large DNN such as ResNet-110 and ResNet-101 to reduce the complex operations during the forward and backward propagation of BN. And provide a possibility to reduce the memory cost (training a DNN without large batch size).

•	The 8bit neural network training in the case of small batch size is realized, and the accuracy loss is almost 0. And the memory required for training is reduced by more than ten times.

•	A quantization method for networks without BN is proposed. Compared with the previous work using BN, this method can still maintain a very high accuracy while ensuring a small loss of accuracy. Even when without BN, training in small batches can be achieved without affecting accuracy.

## Part-time Research Assistant                                                                                                    09/2019 – 09/2020                                                                                                                                                                                                                                                                                                                                                                                                                                                            
Supervisor: Haiyuan Li

Research on Image Recognition of Coal and Gangue based on Convolution Neural Network (CNN) 
### Step One:
■	Data Acquisition and Problem Analysis

•	Collected original photos of coal and gangue under the same lighting and brightness environment and obtained more than 1,000 photos of each category. 

•	Utilized Gray Value+SVM, GLCM+SVM and traditional CNN methods to test the data above, it is found that the above method has a higher error recognition probability under the conditions of dim lights, dirty background, and blurred images.

•	Applied image analysis methods to conduct mathematical analysis on the grey value, grey entropy, inverse moment, correlation and energy and other parameters to verify the correctness of the above results.
### Step Two:
■	Model Establishment and Optimization: LCT-Net(Vision-Based Coal and Gangue Recognition Model)

•	Data Processing and Model Establishment

-	Collected the new data sets according to different resolutions and lights and compiled into numbers 1 to 4 to handle more complex environments.

-	Trained the data through VGG16 and ResNet-18, it is concluded that the classification accuracy is higher than that of previous methods mentioned above.

•	Model optimization and feature recognition

-	Extract target objects through semantic recognition and background separation.

-	Divided each original image into n*n small images to recognize the texture of coal and gangue independently due to the abnormal mineral morphology. And adjusted parameters to find the appropriate value n (the best state n is 5)

-	At the same time, the above method expands the original data set to more than 9w, and makes the model pay more attention to the texture difference of the two stones to reduce the interference of external factors.
### Step Three:

■	Result

•	On different data sets, the accuracy, recall rate of coal, and recall rate of gangue obtained by LCT-Net are all higher than existing models and methods.

•	The average accuracy of LCT-Net in the four data sets is 0.892, the average recall rate of coal is 0.888, and the recall rate of gangue is 0.897.

## Part-time Research Assistant                                                                                                     02/2020 – present                                                                                                                                                                                                                                                                                                                                                                                                                                                            
Supervisor: Haiyuan Li

Exploration of the Parameter Identification and Compliance Control of Linear Motor
### Step One:
■	Data Interaction of Motor

•	Utilized the serial port tools of MATLAB and Simulink to realize the UART communication with the motor and set up the data transmission format (the command frame is a 2B frame header, the length, motor number, command type and control table index are all 1B, the NB data segment, the checksum is 1B).

•	Visualized the received position, voltage, pressure and other parameters through MATLAB to facilitate subsequent observation.
### Step Two:
■	Unit Model Establishment (1 degree of freedom linear)

•	Motor Module

-	The First Part: Converted the voltage into current based on Hillhoff's Law and Laplace transform.

-	The Second Part: Obtained the torque by multiplying the current and the torque constant

-	The Third Part: Obtained the rotational speed with the torque balance equation of the drive shaft.
•	Mechanical transmission module

-	Changed the speed of the motor to the speed of the screw through the reducer and changed the rotation motion to the linear movement of the slider by the nut pair.
### Step Three:
■	Parameter Identification

•	Through Hillhoff's law and Laplace's equation, and for the voltage, current and linear speed parameters among them, curve fitting is performed to determine the back electromotive force constant and resistance.

•	By applying a stable voltage value, the linear speed at the end of the motor is obtained, and the screw and reducer are combined to obtain the torque constant and equivalent damping coefficient.

•	Obtained moment of inertia by fitting the values corresponding to the current and the motor position and combining with the ratio of the acceleration record and the angular acceleration.
### Step Four:
■	Compliant Control

•	Utilized Simulink slide rail to control the movement of the motor and Adjusted the three parameters of inertia, damping and stiffness to change the impedance effect.

•	Placed the motor horizontally and set its sensor value to 1852 to avoid the influence of the end of the motor on gravity, and obtained the force of the system through the position of the motor.

# PUBLICATIONS	
Yuting Xie, Xiaowei Chi, Haiyuan Li, Fuwen Wang. Coal and Gangue Recognition Method Based on Local Texture Classification Network. IEEE Robotics and Automation Letters (RA-L and ICRA). (under review)

