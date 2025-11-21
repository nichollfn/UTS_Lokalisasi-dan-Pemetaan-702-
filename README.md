# UTS_Lokalisasi-dan-Pemetaan-702-

Nicholas Aditya F N (4222201035)

# Turtlebo4 Navigation dari Point A ke Point B
Proyek ini dibuat untuk ujian tengah semester, tujuannya adalah bergerak ke titik A, menyalakan buzzer satu kali, kemudian pergi ke titik B dan menyalakan buzzer dua kali.

# cara kerja
Buat Folder Workspace
```
mkdir -p Winner/src
cd Winner/src
```
Instal package dan dependencies
```
cd ../ && rosdep install --from-paths src --ignore-src -r -y
```
Build Package
```
colcon build
```
sambungkan pc dan turtlebot (Via Ethernet)
```
ssh ubuntu@192.168.185.3
```
Melakukan Mapping
```
ros2 launch turtlebot4_navigation slam.launch.py
ros2 launch turtlebot4_viz view_robot.launch.py
```
# Menjalankan Nav2

menjalankan Lokalization
```
source install/setup.bash
ros2 launch winner1 localization.launch.py
```
menjalankan Navigation
```
source install/setup.bash
ros2 launch winner1 uts_nav.launch.py
```
menjalankan Rvis
```
ros2 launch turtlebot4_viz view_robot.launch.py
```
menjalankan program goal point ke point
```
source install/setup.bash
ros2 run winner1 winner1
