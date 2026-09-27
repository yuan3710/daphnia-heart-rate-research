# Daphnia Heart Rate Analysis – Independent Study

이 저장소는  
**“High-throughput heart rate monitoring in Daphnia magna for sublethal ecotoxicological assessment”**  
논문을 바탕으로 진행한 개인 학습 및 분석 내용을 정리한 저장소입니다.

논문 리뷰를 통해 연구의 실험 과정과 심박수 분석 방법을 이해하고, 이후 심박수 추정에 사용되는 계산적 방법을 직접 비교하기 위한 간단한 개인 연구를 진행했습니다.

\---

## 구성

이 저장소는 크게 다음과 같이 구성되어 있습니다.

### 1\. 논문 리뷰

논문의 연구 배경, 실험 방법, 심박수 측정 과정, 통계 분석, 주요 결과 및 한계점을 정리했습니다.

특히 다음과 같은 흐름을 중심으로 내용을 이해하고 정리했습니다.

* stress-minimised immobilisation
* high-speed imaging
* pixel intensity 기반 heart rate signal 추출
* FFT 및 Fourier fitting
* Kernel Density Estimation (KDE)
* Gaussian decomposition
* Cohen's distance를 이용한 분포 변화 분석

### 2\. 주요 개념 및 용어 정리

논문을 이해하는 과정에서 추가적으로 정리한 주요 개념을 별도의 문서로 작성했습니다.

주요 내용은 다음과 같습니다.

* Kernel Density Estimation (KDE)
* Gaussian decomposition
* Third-order Fourier model
* Levenberg–Marquardt algorithm
* Scott's rule
* Cohen's distance
* 기타 생태독성 및 실험 관련 용어

### 3\. 개인 Computational Study

논문에서 사용된 심박수 분석 방법을 보다 구체적으로 이해하기 위해 Colab 환경에서 별도의 computational benchmark를 진행했습니다.

합성 심박 신호를 생성한 뒤 다음 네 가지 방법을 비교했습니다.

* M1. FFT Peak Detection
* M2. FFT Peak + Parabolic Interpolation
* M3. Autocorrelation
* M4. Third-order Fourier Fitting

각 방법에 대해 주로 다음 요소를 비교했습니다.

* 추정 정확도
* observation duration
* noise 수준
* computational cost

이 실험의 목적은심박수 추정에 사용될 수 있는 여러 계산 방법의 특성과 차이를 이해하는 것입니다.

\---

## Repository Structure

```text
.
├── README.md
├── literature-review/
│   ├── paper-review.md
│   └── terminology-notes.md
└── experiment/
    └── heart-rate-estimation-benchmark.ipynb
```

