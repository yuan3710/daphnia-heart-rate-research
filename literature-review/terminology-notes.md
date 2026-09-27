##### **High-throughput heart rate monitoring in Daphnia magna for sublethal ecotoxicological assessment 속 용어 이해**

###### 

###### **\[kernel density estimation]**

* 데이터 = 어떤 변수가 가질 수 있는 다양한 가능성 중 하나가 현실세계에서 구체화된 것
* 데이터의 관찰 -> 그 변수의 본질적 특성 파악을 위한 노력
* Density Estimation = 관측된 데이터들의 분포로부터 원래 변수의 분포 특성을 추정하고자 하는 것
* kernel function = 어떤 점 주위에 영향을 주는 범위와 그 영향의 크기를 정하는 함수 (특정지점에 어떤 현상이 발생했을 때 어디까지 영향을 받을 지(Bandwidth), 해당 지점으로부터의 거리에 따라 얼마나 영향을 받는지(= 함수의 형태) 결정
* kernel density estimation = 주어진 데이터들을 바탕으로 데이터가 어떤 분포를 이루는지 부드러운 곡선으로 추정하는 방법

###### 

###### **\[Gaussian decomposition]**

* 복잡한 데이터 분포를 여러 정규분포 성분의 합으로 모델링하여 잠재적인 하위 집단이나 패턴을 추정하는 방법
* =  복잡하게 섞여 있는 데이터 분포를 여러 개의 종 모양 정규분포로 나누어 이해하는 방법



###### **\[Third-order Fourier model]**



* Fourier series에서 기본 주파수와 그 주파수의 배수에 해당하는 성분들을 일정한 차수까지 사용하는 모델
* 이 논문에서는 third-order(3차) Fourier model을 사용

즉, 심장 신호를 하나의 단순한 파동으로만 표현하는 것이 아니라, 기본적인 심장 박동 주파수와 여러 harmonic 성분을 함께 사용하여 실제 심장 신호의 형태를 표현한다.



* 차수를 너무 낮게 설정하면

→ 실제 신호의 복잡한 형태를 충분히 표현하기 어려움

* 차수를 너무 높게 설정하면

→ noise까지 따라가는 overfitting이 발생할 수 있고 계산량도 증가함



따라서 fitting accuracy와 computational efficiency 사이의 균형을 위해 third-order model을 사용하였다.



###### **\[Levenberg–Marquardt algorithm]**



모델이 실제 관측 데이터와 최대한 비슷해지도록 parameter를 반복적으로 조정하는 최적화 알고리즘= 만든 곡선을 실제 데이터에 최대한 잘 맞게 조정하는 방법

이 논문에서는 Fourier series model을 실제 pixel intensity 신호에 fitting할 때 사용

FFT를 통해 대략적인 주파수를 찾은 뒤, Levenberg–Marquardt algorithm을 이용해 Fourier model과 실제 측정 신호의 차이가 최소가 되도록 parameter를 조정

* FFT

→ 대략적인 초기주파수 발견

* Fourier series model

→ 실제 심장 신호를 표현할 모델 생성

* Levenberg–Marquardt algorithm

→ 모델이 실제 신호와 최대한 잘 맞도록 조정





###### **\[Scott's rule]**



* KDE에서 사용할 bandwidth를 데이터의 표준편차와 표본 수를 이용해 자동으로 정하는 규칙
* h = 1.06 · σ · n^(-1/5)

  * σ가 클수록 데이터가 넓게 퍼져 있으므로 bandwidth 증가
  * n이 클수록 데이터가 많아 분포를 더 세밀하게 추정할 수 있으므로 bandwidth 감소



= KDE 곡선이 너무 울퉁불퉁하거나 너무 뭉개지지 않도록

데이터 특성에 맞는 smoothing 정도를 정하는 방법







##### ***단어 이해***



|high-throughput|많은 개체/데이터를 짧은 시간에 처리할 수 있는 고처리량 방식|
|-|-|
|sublethal|아치사. 생물이 죽지는 않지만 생리적·행동적 변화가 나타나는 수준|
|ecotoxicological assessment|생태독성 평가|
|Daphnia magna|큰물벼룩|
|stress-minimised immobilisation|스트레스를 최소화한 개체 고정 방법|
|probability-based statistical analysis|확률 기반 통계 분석|
|distribution-based convergence analysis|분포 기반 수렴 분석|
|hydrogen peroxide|과산화수소|
|reference substances|기준 물질. 연구에서 개발한 심박수 측정 방법이 알려진 반응을 제대로 감지하는지 검증하기 위해 사용한 물질 (과산화수소와 카페인)|
|environmental risk assessment|환경위해성 평가|
|acute endpoints|급성 평가 지표|
|immobilisation|움직임 억제|
|physiological endpoint|생리학적 평가 지표|
|solvent|용매|
|optoelectronic system|광전자 시스템|
|analytical consistency|분석 결과의 일관성|
|NP solution|나노입자 용액|
|double-distilled H₂O|이중증류수|
|sonication|초음파처리. 물질에 고주파 초음파(음파) 에너지를 가하여 분쇄, 분산, 균질화 또는 세척하는 과정|
|nominal concentration|명목 농도.  제조할 때 설정한 목표 농도|
|new neonates|갓 태어난 개체|
|ISO medium|ISO 기준에 따라 조성된 시험용 배양/노출 용액. Daphnia가 실험 조건에서 안정적으로 살 수 있도록 정해진 표준 조성의 물|
|ICP-MS (Inductively Coupled Plasma Mass Spectrometry)|유도결합플라즈마 질량분석법. 아주 적은 양의 금속이나 원소 농도를 정밀하게 측정하는 분석법|
|Phase-contrast inverted microscope|위상차 도립현미경. 무색투명한 살아있는 세포나 미생물을 염색하지 않고 하단에서 관찰할 수 있도록 만든 특수 광학 현미경|
|Probability density function(PDF)|확률밀도함수|
|Bandwidth|대역폭. 각 데이터 한 점이 주변에 얼마나 넓은 범위까지 영향을 미칠지를 정하는 값|
|smoothing|스무딩. 평활화. 데이터나 신호의 불규칙한 변동이나 노이즈를 줄이고 부드럽게 다듬어 전체적인 경향이나 패턴을 파악하기 쉽게 만드는 기법|
|convergence tolerance|반복 계산이 어느 정도까지 수렴했을 때 fitting을 완료된 것으로 판단할지를 정하는 기준|
|emerging contaminants|신흥 독성 물질|
|quantifiable, non-lethal physiological endpoint|정량화할 수 있고, 개체를 죽이지 않고 측정할 수 있는 생리학적 평가 지표|
|Cohen's distance|대조군과 노출군의 심박수 분포가 얼마나 멀리 떨어져 있는지를 나타내는 값. 값이 클수록 노출에 의해 심박수 분포가 더 크게 변했다는 의미|



