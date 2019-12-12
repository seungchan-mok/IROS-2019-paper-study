# RangeNet++: Fast and Accurate LiDAR Semantic Segmentation

- 저자 : Andres Milioto, Ignacio Vizzo, Jens Behley, Cyrill Stachniss

- [paper](http://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/milioto2019iros.pdf)

- [github](https://github.com/PRBonn/lidar-bonnetal)

---
## Method

- LiDAR-only Semantic Segmentation
- CNN기반, pointcloud를 구에 투영해 2D이미지로 변환
- 차량의 움직임을 고려해 이미지로 변환
- architecture는 기존 3D LiDAR Sementic Segmentation CNN과 유사
- 쓰인 FCN구조는 모래시계와 같은 구조를 갖고 있으므로 data손실이 발생
- 후처리에서 제안된 알고리즘을 GPU를 사용해 계산, 소요 시간과 손실을 줄임

## Comments
- Related work에서 언급된 논문도 봐야할 듯
- 알고리즘쪽 내용 추가예정