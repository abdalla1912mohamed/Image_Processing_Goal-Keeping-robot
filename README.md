






# Image_Processing_Goal-Keeping-robot
in this project, a Goal Keeper Robotic Arm using Image Processing techniques was designed and simulated to track a ball
with a 1 DoF robotic arm implemented as one Servo Motor. The techniques used in this project are: Image Acquisition, Image
Filtration, Color Detection, Contour Detection. Then the ball center is extracted and the angle to be followed by the robotic
arm is calculated and sent to the Arduino to actuate the motor, hence block the ball from entering the goal such as the human
goalkeepers.




##in our project, Hough transform was not enough to detect the ball , so we had to add another limitation to our target
ball ( orange color) we have obtained the hse lower and upper limit for the specific color we used which is pale orange so
that the ball could be efficiently detected . Moreover , our first limitation is the circular contour detected by findcontour()
function where the center of the ball is detected also and printed , the process of finding contour comes after an opening
process ( erosion then dilation ) to eliminate any unnecessary noise and to filter our image . our second limitation is the
color of the ball which occurs in a range of specific lower and upper hsv bounds so by using both limitation the ball center
can be efficiently detected. Eventually, Two important values are calculated by subtracting the center of the ball from the
center of our image so that X and Y displacements are used to calculate the required angle needed to move the servo so
that its center and the ball coincides resulting in a goal-keeping behaviour.
