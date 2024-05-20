# Lidar_camera_sensorfusion
카메라와 라이다를 센서 퓨전하여 utm좌표로 객체의 위치를 나타내는 코드입니다.
## description

![autopg_rqt](https://github.com/ERP1-Team/LIdar_camera_sensorfusion/assets/140485388/8f3a9114-54d2-4612-8c58-449ec05884c3)
node들간의 구조는 위와 같습니다. 

먼저, autopg_lidar packge에서 클러스터링 된 객체의 데이터를 /Lidar_object 토픽으로 발행한다. 메시지 타입은 아래와 같다.
<summary>
/Lidar_object 메시지
</summary>
string classes

uint16 idx

float32 x

float32 y

float32 z

float32 xMin

float32 yMin

float32 zMin

float32 xMax

float32 yMax

float32 zMax
</details>
두번째로, yolo_v8_msgs에서 raw_image를 subscribe하여 /yolov8/img(yolo 이미지)와 /yolov8/bboxes(바운딩박스 정보)를 pub한다. 
<summary>
/yolov8/bboxes의 메시지
  
</summary>

string class_name

float32 xMin

float32 yMin

float32 xMax

float32 yMax

float32 confidence

</details>
</details>
세번째로, yolo_v8_msgs에서 raw_image를 subscribe하여 /yolov8/img(yolo 이미지)와 /yolov8/bboxes(바운딩박스 정보)를 pub한다. 
<summary>
/yolov8/bboxes의 메시지
  
</summary>

string class_name

float32 xMin

float32 yMin

float32 xMax

float32 yMax

float32 confidence

</details>
      
## Installation
1. cd ~/ros1_ws/src
2. git clone https://github.com/ERP1-Team/LIdar_camera_sensorfusion.git
3. cd ..
4. catkin_make

## Usage
