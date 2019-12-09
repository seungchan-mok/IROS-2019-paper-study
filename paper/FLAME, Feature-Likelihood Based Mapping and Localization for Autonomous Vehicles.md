# FLAME: Feature-Likelihood Based Mapping and Localization for Autonomous Vehicles

- 저자 : Su Pang, Daniel Kent, Daniel Morris and Hayder Radha

## Method

- LiDAR Scan에서 Feature Detection한 결과를 Vector Data로 저장
- 기존의 방법보다 0.1%의 저장공간을 차지
- 평면, 기둥, 커브 Feature를 이용
- 3D Pointcloud Map에서 2D Feature Vector Map(FLAME)을 생성
- Cloth Simulation Filter로 지면 검출, 지면이 아닌 점들을 레스터화하여 xy평면에 나타냄
- 레스터화한 point cloud에서 3 class의 feature 검출
- 실시간으로 feature 검출, 위치인식 - [23] 프레임누적, feature 검출
- pointcloud map localization은 4-5m position error, 제안한 방법은 8-9m정도의 error
- 용량면에서 많은 이점이 있음