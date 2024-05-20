# Lidar_camera_sensorfusion
카메라와 라이다를 센서 퓨전하여 utm좌표로 객체의 위치를 나타내는 코드입니다.
## description

![autopg_rqt](https://github.com/ERP1-Team/LIdar_camera_sensorfusion/assets/140485388/8f3a9114-54d2-4612-8c58-449ec05884c3)
node들간의 구조는 위와 같습니다. 
      
## Installation
1. cd ~/ros1_ws/src
2. git clone https://github.com/ERP1-Team/LIdar_camera_sensorfusion.git
3. 압축해제 후
4. cd ..
5. catkin_make

## Usage
roslaunch sensor_fu lidar_yolo.launch 

위의 명령어를 통해 lidar, yolo, lidar_gps 를 실행한다. 
