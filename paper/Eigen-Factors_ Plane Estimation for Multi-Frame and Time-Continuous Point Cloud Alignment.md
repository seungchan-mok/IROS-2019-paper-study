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

## Experimentss

- 랜덤 궤적을 생성하고 다양한 평면에 해당하는 합성 데이터를 시뮬레이션함(Generate random trajectory and various plane were simulated).
- EF는 매우 부드러운 평면을 계산 가능함(EFs are able to calculate very smooth planes at the cost of displacing trajectories)


## Comments

