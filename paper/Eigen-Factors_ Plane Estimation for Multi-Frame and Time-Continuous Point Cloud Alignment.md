# Eigen-Factors_ Plane Estimation for Multi-Frame and Time-Continuous Point Cloud Alignment


- Author : Gonzalo Ferrer.

- [paper](https://www.researchgate.net/publication/335840674_Eigen-Factors_Plane_Estimation_for_Multi-Frame_and_Time-Continuous_Point_Cloud_Alignment)

- [gitbub](https://gitlab.com/gferrer/eigen-factors-iros2019)

- Write this by Dohyeong Kim(robotdevel@naver.com)
---

## Main Contribution

- EFs are a reformulation of plane estimation for multiframe PC alignment. EFs’ complexity is independent of the number of points. 
- Closed-form derivation of the EFs’ gradients using SE(3) and Lie algebra. 
- A time-continuous derivation of EFs using interpolation in the manifold.

## Experiments

- 랜덤 궤적을 생성하고 다양한 평면에 해당하는 합성 데이터를 시뮬레이션함(Generate random trajectory and various plane were simulated).
- EF는 매우 부드러운 평면을 계산 가능함(EFs are able to calculate very smooth planes at the cost of displacing trajectories)

- 제안하는 EF기반의 Plane matching 기법을 ICP(point to point), ICP(point to plane)방법과 비교함(proposed method were evaluated with ICP algorithm)
- ICP에 기반한 매칭 방법은 짧은 포즈(2-4 frame)사이에서 더 높은 성능을 보였지만 포즈의 갯수가 증가할 수록 EF의 성능이 높은 것을 확인할 수 있었음(ICP algorithm was better than EF method when they use 2~4 frames but EF method is more better on many frames)
- 또한 ICP 알고리즘은 여러 thread를 사용하여 동작하는 반면에 EF 방법은 단일 thread만을 사용하여 좀더 효율적임을 나타냄(ICP algorithm used few thread in PC but EF method need only a thread)

## Comments

