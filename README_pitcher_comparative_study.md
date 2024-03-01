# Astros Technical Assessment - Pitcher Comparative Study

This document is to review and compare the various pitcher data that was provided on 26FEB2024 as a technical assessment for the Perforamance Engineer Role with the Houston Astros Organization.
___
___
___
## Raw and Cleaned/Processed Data
Raw and processed data can be independently reviewed per pitcher and game in each respective pitcher report that is organized by pitcher identification number - "README_pitcher_{pitcher_id}.md". This documentation has also been provided in *.pdf formatting for ease of review.

## Signal Processing Methodology - Density-Based Spatial Clustering of Applications with Noise (DBSCAN)
Details concerning DBSCAN implementation is outlined in each individual pitcher report.

## Measured Metrics to Identify Arm Path
Full details concerning each metric are outlined in each individual pitcher report.

## Observations
Review of the metrics below identify that Aggregate Mean Path, Total Path, Cumulative Distance Traveled per Joint, Curvature Profile and Velocity Profile differ significantly from pitcher to pitcher. Further, in review of Pitcher 669302 comparing games Sched 429650 and Sched 430322 all metrics show visually identical profiles and plots. 

However, in review of Pitcher 554430 when comparing Sched 429722 and Sched 429804 there are clear differences between Sched metrics. Joint Curvature Profiles are very different, showing that the rate of change of direction along curved movements is impacted greatly. Review of Joint Velocity Profiles also shows significant differences, identifying significantly lower velocities for all reviewed joints at ball release (time = 0) for Sched 429722. Total path length between both Sched's for the pitcher are also notably different. Though review of Aggregate Mean Path does not, at a quick glance, identify significant differences, there is some mutia that can be considered different. At -0.5 seconds there is a sharp dip along the x-axis of the right elbow in Sched 429804 that is slightly smoother in Sched 429722. Review of the Aggregate Mean Path along the z-axis for all joints also shows about 0.25 greater values along the entire path for Sched 429804 than Sched 429722.




___
___
___
### 1. Curvature Over Time Profile

<center> 
Pitcher 669302 - Sched 429650

<img src = "./images_and_output_data/pitcher_669302/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_669302/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_wrist_curvature.png" width = 25%>

Pitcher 669302 - Sched 430322

<img src = "./images_and_output_data/pitcher_669302/sched430322/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_wrist_curvature.png" width = 25%>

Pitcher 680689 - Sched 429650

<img src = "./images_and_output_data/pitcher_680689/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_680689/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_wrist_curvature.png" width = 25%>

Pitcher 554430 - Sched 429722

<img src = "./images_and_output_data/pitcher_554430/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_554430/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_wrist_curvature.png" width = 25%>

Pitcher 554430 - Sched 429804

<img src = "./images_and_output_data/pitcher_554430/sched_429804/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_wrist_curvature.png" width = 25%>

Pitcher 642547 - Sched 429722

<img src = "./images_and_output_data/pitcher_642547/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_642547/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_wrist_curvature.png" width = 25%>

Pitcher 641712 - Sched 429804

<img src = "./images_and_output_data/pitcher_641712/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_641712/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_wrist_curvature.png" width = 25%>

Pitcher 543243 - Sched 430322

<img src = "./images_and_output_data/pitcher_543243/r_hip_curvature.png" width=25%><img src = "./images_and_output_data/pitcher_543243/r_shoulder_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_elbow_curvature.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_wrist_curvature.png" width = 25%>
</center>

___
___
___

### 2. Velocity Over Time Profile
<center>
Pitcher 669302 - Sched 429650

<img src = "./images_and_output_data/pitcher_669302/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_669302/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_wrist_velo.png" width = 25%>

Pitcher 669302 - Sched 430322

<img src = "./images_and_output_data/pitcher_669302/sched430322/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_wrist_velo.png" width = 25%>

Pitcher 680689 - Sched 429650

<img src = "./images_and_output_data/pitcher_680689/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_680689/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_wrist_velo.png" width = 25%>

Pitcher 554430 - Sched 429722

<img src = "./images_and_output_data/pitcher_554430/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_554430/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_wrist_velo.png" width = 25%>

Pitcher 554430 - Sched 429804

<img src = "./images_and_output_data/pitcher_554430/sched_429804/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_wrist_velo.png" width = 25%>

Pitcher 642547 - Sched 429722

<img src = "./images_and_output_data/pitcher_642547/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_642547/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_wrist_velo.png" width = 25%>

Pitcher 641712 - Sched 429804

<img src = "./images_and_output_data/pitcher_641712/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_641712/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_wrist_velo.png" width = 25%>

Pitcher 543243 - Sched 430322

<img src = "./images_and_output_data/pitcher_543243/r_hip_velo.png" width=25%><img src = "./images_and_output_data/pitcher_543243/r_shoulder_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_elbow_velo.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_wrist_velo.png" width = 25%>
</center>

___
___
___
### 3. Cumulative Distance Traveled per Joint

<center>

Pitcher 669302 - Sched 429650 (L) & 430322 (R)

<img src = "./images_and_output_data/pitcher_669302/total_path_length.png" width = 50%><img src = "./images_and_output_data/pitcher_669302/sched430322/total_path_length.png" width = 50%>

Pitcher 680689 - Sched 429650

<img src = "./images_and_output_data/pitcher_680689/total_path_length.png" width = 50%>

Pitcher 554430 - Sched 429722 (L) & 429804 (R)

<img src = "./images_and_output_data/pitcher_554430/total_path_length.png" width = 50%><img src = "./images_and_output_data/pitcher_554430/sched_429804/total_path_length.png" width = 50%>

Pitcher 642547 - Sched 429722

<img src = "./images_and_output_data/pitcher_642547/total_path_length.png" width = 50%>

Pitcher 641712 - Sched 429804

<img src = "./images_and_output_data/pitcher_641712/total_path_length.png" width = 50%>

Pitcher 543243 - Sched 430322

<img src = "./images_and_output_data/pitcher_543243/total_path_length.png" width = 50%>
</center>

### 4. Aggregate Mean Path

<center>

Pitcher 669302 - Sched 429650

<img src = "./images_and_output_data/pitcher_669302/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_669302/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_669302/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/r_wrist_z_mean_path.png" width = 25%>


Pitcher 669302 - Sched 430322

<img src = "./images_and_output_data/pitcher_669302/sched430322/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_wrist_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_669302/sched430322/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_669302/sched430322/r_wrist_z_mean_path.png" width = 25%>

Pitcher 680689 - Sched 429650

<img src = "./images_and_output_data/pitcher_680689/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_680689/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_680689/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_680689/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_680689/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_680689/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_680689/r_wrist_z_mean_path.png" width = 25%>

Pitcher 554430 - Sched 429722

<img src = "./images_and_output_data/pitcher_554430/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_554430/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_554430/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/r_wrist_z_mean_path.png" width = 25%>


Pitcher 554430 - Sched 429804

<img src = "./images_and_output_data/pitcher_554430/sched_429804/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_wrist_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_554430/sched_429804/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_554430/sched_429804/r_wrist_z_mean_path.png" width = 25%>

Pitcher 642547 - Sched 429722

<img src = "./images_and_output_data/pitcher_642547/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_642547/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_642547/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_642547/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_642547/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_642547/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_642547/r_wrist_z_mean_path.png" width = 25%>

Pitcher 641712 - Sched 429804

<img src = "./images_and_output_data/pitcher_641712/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_641712/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_641712/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_641712/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_641712/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_641712/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_641712/r_wrist_z_mean_path.png" width = 25%>

Pitcher 543243 - Sched 430322

<img src = "./images_and_output_data/pitcher_543243/r_hip_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_543243/r_shoulder_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_543243/r_elbow_x_mean_path.png" width=25%><img src = "./images_and_output_data/pitcher_543243/r_wrist_x_mean_path.png" width=25%>
<img src = "./images_and_output_data/pitcher_543243/r_hip_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_shoulder_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_elbow_y_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_wrist_y_mean_path.png" width = 25%>
<img src = "./images_and_output_data/pitcher_543243/r_hip_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_shoulder_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_elbow_z_mean_path.png" width = 25%><img src = "./images_and_output_data/pitcher_543243/r_wrist_z_mean_path.png" width = 25%>

</center>