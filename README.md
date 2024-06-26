# IoT Camera-Assisted Localization for AR in Simulated and Real-World Environments

This repository holds the code I write in the Spring 2024 semester as a part of my Duke ECE Independent Study.

## Research Overview:

### Background:
AR must track user movement and location with high accuracy and consistency. This study studies an AR tracking method that leverages third-view IoT cameras to enhance enhancing predictions concerning user location and pose.

### Experimental Procedure:
We set up three markers (an ArUco marker, a colored marker, and a Unity logo), and two environments (virtual 3D space in Unity and real-world lab environment. We then conducted multiple trials across different marker and environment combinations as well as camera settings to gather comprehensive data.

#### Markers for Movement Tracking:
Each marker was attached to an AR headset to track user position and orientation within a controlled trajectory in a simulated environment and along a fixed path in our lab.


<img width="290" alt="Screenshot 2024-05-03 at 12 08 20 PM" src="https://github.com/aliceyh7/Alice_ECE_IndependentStudy_S24/assets/167914381/032d05f4-da73-4ddb-997d-f7e1b91abac6">
<img width="290" alt="Screenshot 2024-05-03 at 12 08 31 PM" src="https://github.com/aliceyh7/Alice_ECE_IndependentStudy_S24/assets/167914381/df5c4796-1920-42ac-b245-c86125bebdcc">



### Data Analysis:
We employed YOLOv5 neural network models and OpenCV Toolbox for analyzing the data collected.

## Repository File Descriptions:

- `deterministic_pattern_recognition.ipynb`: Analyzes the results provided by the OpenCV Toolbox for deterministic AR marker recognition.
  
- `yolov5_marker1_combined.ipynb`: Analyzes the YOLOv5 model's performance on ArUco marker detection using a mix of simulated and real-world data
  
- `yolov5_marker1_realworld.ipynb`: Analyzes the real-world performance of the YOLOv5 model for ArUco marker detection
  
- `yolov5_marker1_unity.ipynb`: Analyzes the YOLOv5 model's performance on ArUco marker detection using only simulated data from Unity
  
- `yolov5_marker2_combined.ipynb`: Analyzes the YOLOv5 model's performance on colored marker detection using a mix of simulated and real-world data
  
- `yolov5_marker2_realworld.ipynb`: Analyzes the real-world performance of the YOLOv5 model for the colored marker detection
  
- `yolov5_marker2_unity.ipynb`: Analyzes the YOLOv5 model's performance on the colored marker detection using only simulated data from Unity

- `yolov5_marker3_combined.ipynb`: Analyzes the YOLOv5 model's performance on Unity Logo marker detection using a mix of simulated and real-world data
  
- `yolov5_marker3_realworld.ipynb`: Analyzes the real-world performance of the YOLOv5 model for Unity Logo marker detection
  
- `yolov5_marker3_unity.ipynb`: Analyzes the YOLOv5 model's performance on the Unity logo marker detection using only simulated data from Unity
  
- `yolov5_precision_recall_mAP_f1_results.ipynb`: Compiles results on precision, recall, mAP, and F-1 scores for different markers and models in both simulated and real-world contexts.

## Key Findings:

- ArUco markers yielded the highest average performance across all evaluated metrics, while colored markers exhibited the least robust performance.
- The integration of simulated and real-world data demonstrated an overall performance boost for all marker types.
- YOLOv5 significantly outperformed OpenCV in marker detection rates, particularly for ArUco markers.

## Future Work:

We plan to incorporate first-view camera data to validate the efficacy of our third-view tracking method further. Additionally, we will expand our dataset to include a wider range of real-world scenarios and lighting conditions to continue refining the capabilities of third-view tracking.

## References:
- [1] Chen, Y., Inaltekin, H., & Gorlatova, M. (2023). AdaptSLAM: Edge-assisted adaptive SLAM with resource constraints via uncertainty minimization. In Proc. IEEE INFOCOM.
- [2] Bultmann, S., Memmesheimer, R., & Behnke, S. (2023). External Camera-based Mobile Robot Pose Estimation for Collaborative Perception with Smart Edge Sensors.
- [3] Wen, Y., Singh, K. K., Anderson, M., Jan, W. P., & Lee, Y. J. (2021). Seeing the Unseen: Predicting the First-Person Camera Wearer’s Location and Pose in Third-Person Scenes. IEEE/CVF International Conference on Computer Vision Workshops (ICCVW).
