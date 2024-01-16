# stereo_vision_tracking_using_ground_plane_homography_and_km
stereo vision tracking of people using ground plane homography and sort tracker.
The sort tracker uses intersection over union to map detection to trackers, which causes ID switches for persons near each other.
the main idea is to use the ground plane homography transformation to find matches in the two cameras 
an idea that is used in this [paper] (https://arxiv.org/abs/2304.09471)\n
 stereo correspondence solves the occlusion or no detection for a period in one of the cameras. 
. the stereo correspondence tries to correct the ID using the nearest correspondence track ID from the other camera.
. if there is no correspondence track it initiates a new sort track in the camera.
. every unmatched detection checks if it has correspondence track in the other camera and assigns it an ID. 


