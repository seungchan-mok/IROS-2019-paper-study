# Eigen-Factors_ Plane Estimation for Multi-Frame and Time-Continuous Point Cloud Alignment


- Author : Gonzalo Ferrer.

- [paper](https://www.researchgate.net/publication/335840674_Eigen-Factors_Plane_Estimation_for_Multi-Frame_and_Time-Continuous_Point_Cloud_Alignment)

- [gitbub](https://gitlab.com/gferrer/eigen-factors-iros2019)

- Write this by Dohyeong Kim(robotdevel@naver.com)
---

## Abstract

- 이 논문에서는 Eigen-Factor(EF)라는 방법을 소개함
- EF는 센서에 의해 묘사된 다른 자세에서 점구름 세트에서 표면을 추정하는데 있음  
- 본 논문은 관측된 일련의 Point Cloud(PC)에서 다중 프레임 정렬을 해결할 수 있도록 EF를 사용할 것을 권장함 
- 또한 EF의 최적화의 복잡성은 점의 수에 무관하지만 평면의 포즈의 수에 따라 다름
- Closed-form of the gradient는 포즈와 관련하여 최소 고유값을 구분하여 파생하므로 이런 까닭에 Eigen-Factor라 불림
- 추가적으로 EF의 time continous trajectory version이 제안됨
- EF 접근 방식은 시뮬레이션 환경에서 평가되며 두가지 ICP버전과 비교되어 EF의 성능의 우수성을 검증함
- ICP와 비교했을때 EF가 오류의 최적화 성능, 계산시간 모두 월등히 앞섬


## Main Contribution

- EFs are a reformulation of plane estimation for multiframe PC alignment. EFs’ complexity is independent of the number of points. 
- Closed-form derivation of the EFs’ gradients using SE(3) and Lie algebra. 
- A time-continuous derivation of EFs using interpolation in the manifold.

- gradient method 기법을 통한 최적화 작업 수행


## Experiments

- 랜덤 궤적을 생성하고 다양한 평면에 해당하는 합성 데이터를 시뮬레이션함(Generate random trajectory and various plane were simulated).
- EF는 매우 부드러운 평면을 계산 가능함(EFs are able to calculate very smooth planes at the cost of displacing trajectories)

- 제안하는 EF기반의 Plane matching 기법을 ICP(point to point), ICP(point to plane)방법과 비교함(proposed method were evaluated with ICP algorithm)
- ICP에 기반한 매칭 방법은 짧은 포즈(2-4 frame)사이에서 더 높은 성능을 보였지만 포즈의 갯수가 증가할 수록 EF의 성능이 높은 것을 확인할 수 있었음(ICP algorithm was better than EF method when they use 2~4 frames but EF method is more better on many frames)
- 또한 ICP 알고리즘은 여러 thread를 사용하여 동작하는 반면에 EF 방법은 단일 thread만을 사용하여 좀더 효율적임을 나타냄(ICP algorithm used few thread in PC but EF method need only a thread)

## Comments

