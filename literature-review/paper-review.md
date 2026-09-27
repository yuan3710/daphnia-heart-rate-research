##### **High-throughput heart rate monitoring in Daphnia magna for sublethal ecotoxicological assessment**

###### **= 아치사 생체독성 평가를 위한 Daphnia magna의 고처리량 심박수 모니터링**

###### 

###### **\[Highlights]**

다수의 Daphnia magna들의 heart rate를 빠르게 측정하고 단순 평균이 아닌 집단 전체의 반응 분포를 분석함으로써 기존 독성 시험보다 더 이른 단계에서 영향을 찾아낼 수 있다.



###### **\[Keywords]**

* Daphnia magna (큰물벼룩)
* Heart rate distribution (심박수 분포)
* Sublethal effects (아치사 영향)
* Nanoparticle toxicity (나노입자 독성)
* Fourier analysis (푸리에 분석)



###### **\[0. ABSTRACT]**



논문의 도입부인 Abstract 부분에서는 기존 Daphnia magna 심박수 기반 독성평가의 한계를 제시하고, 이를 개선한 고처리량 심박수 분석 시스템의 핵심 결과와 생태독성 평가에서의 활용 가능성을 요약한다.



&#x09;Daphnia magna의 심박수를 모니터링하는 방법은 생태독성 평가에서 sensitive physiological indicator(민감한 생리학적 지표)로의 활용 가능성을 가지고 있지만 이 방법을 널리 사용하는데에는 기존 심박수 측정은 처리량이 낮고, 개체 간 차이가 크며, 평균값 위주로 해석한다는 한계가 있었다.

이를 해결하기 위해

* stress-minimised immobilisation (스트레스 최소화 개체 고정 방법)
* high-speed imaging (고속 영상 촬영)
* Fourier-based analysis

를 결합한 integrated methodology로 시간당 약 150마리의 심박수를 측정할 수 있게 했다.



&#x09;또한 많은 개체의 심박수 데이터를 확보한 뒤 Kernel density estimation과 Gaussian deconvolution을 이용해 평균값이 아니라 전체 분포와 subpopulation을 분석했다.

분포 안정성 분석 결과 N ≥ 63에서 안정적인 추정이 가능했고, 이후 실험에서는 조건당 N = 100을 사용했다.

이 방법은 hydrogen peroxide와 caffeine으로 검증되었고, paraquat, potassium dichromate, CuONPs, AuNPs에서도 기존 독성 기준보다 낮은 농도에서 나타나는 심박수 변화를 감지했다.



&#x09;결국 이 연구의 핵심은 많은 개체의 심박수 분포를 이용해 기존 독성시험에서 놓칠 수 있는 초기 sublethal stress를 더 민감하게 탐지하는 것으로 next-generation environmental risk assessment(차세대 환경 위해성 평가도구)로 활용될 가능성을 제시한다.

&#x20;

###### **\[1. INTRODUCTION]**



&#x09;Introduction에서는 왜 기존 생태독성 평가와 심박수 측정 방식만으로는 초기 아치사 반응을 충분히 보기 어려운지 설명하고, 이를 보완하기 위해 고처리량·자동화·분포 기반의 심박수 분석이 왜 필요한지를 제시한 뒤, 이 논문이 제안하는 연구 방향과 목적을 소개한다.



&#x09;Daphnia magna는 생태독성 연구에서 널리 사용되는 대표적인 모델 생물이다. 기존의 표준 독성시험에서는 주로 immobilisation, mortality 와 같은 acute endpoints(급성 평가 지표)를 이용한다. 하지만 이러한 지표는 생물이 실제로 큰 이상을 보이거나 죽는 단계의 반응을 중심으로 보기 때문에, nanoparticle이나 microplastic처럼 상대적으로 독성이 낮은 물질이 일으키는 변화를 충분히 감지하지 못할 수 있다.



&#x09;그 한계를 보완하기 위해 최근에는 Daphnia의 heart rate를 민감한 physiological endpoint(생리학적 평가 지표)로 활용하는 방식이 제시되었으나 노동력이 과중하며, 측정시간이 길고, 재현성이 낮으면 개체간 차이가 크다. 이를 해결하기 위해서는 high-throughput, automated, reliable 하도록 개선해야한다. 또한, Daphnia를 측정하기 위한 점성 물질의 투입 ,접착 물질 사용, 물리적 고정이 개체에게 주는 physical, chemical stress가 heart rate 자체에 영향을 줄 수도 있으며 한 개체씩 처리하는 방식이 처리량을 낮추고 전체 실험 시간을 늘리는 것은 물론 측정 전 대기시간으로 인해 생물이 받는 스트레스가 증가한다.



&#x09;기존 심박수 측정의 다양한 문제를 해결하기 위해 최근 연구들은 video-assisted systems의 사용이 증가하였으나 높은 컴퓨팅 자원을 요구하며 저장공간이 과도하게 필요하다. 다음은 최근 기술들에 대한 간단한 요약이다.

* Santoso et al : video-based tracking으로 D.magna의 심장반응과 행동반응 동시 측정
* Tkaczyk et al : optoelectronic system(광전자 시스템)이용 -> 대규모 적용에는 한계 존재
* Ibbini et al, Saputra et al : 투명한 생물체에서 심박수와 heart rate variability(심박변이도)를 자동으로 측정할 수 있는 open-source solution을 제시

그러나 대부분의 연구는 여전히 single individual를 분석하는 데 초점을 두고 있으며, population-level variability(집단 수준의 개체 차이)와 sublethal sensitivity distribution(아치사 반응 민감도의 분포)를 충분히 반영하지 못한다.



따라서, 본 논문은 기존 심박수 측정 방식의 한계를 보완하기 위해 스트레스를 최소화한 고정 방법, 자동 실시간 영상 분석, Fourier 기반 신호 추출을 결합한 고처리량 심박수 모니터링 시스템을 제안한다. 이를 통해 여러 Daphnia magna 개체의 심박수를 빠르고 비침습적으로 측정하고, KDE와 Gaussian peak deconvolution을 이용해 평균값이 아닌 집단 전체의 심박수 분포를 분석함으로써 기존 방법에서 놓칠 수 있는 초기 아치사 독성 영향과 집단 수준의 반응 차이를 탐지하고자 한다.



###### **\[2. Materials and methods]**



&#x09;Materials and methods에서는 연구 과정에서 무엇을 어떻게 실험하였는지에 대한 세부 내용을 다루고 있다. 따라서 해당 chapter에서는 실험 설계의 큰 흐름과 왜 이런 방법을 선택하였는지 그 근거를 이해하는 것을 주요 목적으로 삼고자한다.



&#x09;**2.1 Solution preparation**에서는 다음 물질을 활용하여 용액을 준비하는 과정을 설명한다.



\- Hydrogen peroxide (H₂O₂)

\- Caffeine

\- Paraquat

\- Potassium dichromate

\- Copper oxide nanoparticles (CuONPs)

\- Gold nanoparticles (AuNPs)



나노입자 용액은 stock solution을 만든 뒤 shaking과 sonication을 통해 분산시키고, ISO medium으로 실험 농도까지 희석하여 사용하였다.

또한 nanoparticle의 실제 노출 농도를 확인하기 위해 대표 시료의 용존 금속 농도를 ICP-MS로 측정하여 명목농도와 비교하였다.



&#x09;**2.2 D. magna sample preparation for heart rate monitoring**에서는 D.magna 샘플을 만들고 심박을 측정하는 방법까지를 서술한다.



1. 실험 그룹마다 100마리의 개체를 무작위로 선택 후 투입하는데 이때 개체는 OECD TG 211에 따라 생후 21일 미만인 건강한 개체의 3\~5번째 번식에서 갓 태어난 개체를 선택한다.  이후 개체들을 지정된 농도의 시험물질에 24시간 동안(caffeine은 2시간) exposure한다.
2. 각 treatment group에서 20마리씩 titanium tweezers를 사용하여 5mg의 처리되지 않은 의료용 유기면(솜)이 고르게 펼쳐진 6-well plate로 옮긴다.
3. 그 다음 well 중앙에서 micropipette을 사용하여 배지를 제거한 후 같은 용액을 1.6mL 투여한다. 이는 전체 용액의 부피 오차를 줄여준다.
4. 섭씨 20도에서 30분간 배양하며 개체가 심박수를 안정시키며 이완되도록 한다.



위와 같은 방법으로 D.magna sample을 준비하면 다음으로 심박수를 촬영할 수 있다.

영상 촬영은 phase-contrast inverted microscope로 이루어진다. 이에 CCD 카메라를 장착한 광학 장비 설정은 심장 움직임을 구분하기에 충분한 해상도를 제공한다.

단순히 영상을 저장한 뒤 사람이 직접 심박수를 세는 방식이 아니라, Basler Pylon SDK와 PySide6를 기반으로 자체 개발한 GUI(Graphical User Interface) 프로그램을 사용하여 심장 신호를 실시간으로 분석한다.

이 GUI 프로그램에서는 Daphnia의 심장 가장자리 영역을 ROI(region of interest)로 지정하고, 해당 영역의 pixel intensity(픽셀 밝기)가 시간에 따라 어떻게 변화하는지를 frame-by-frame으로 분석하였다. 구체적으로는 5×5 pixel 영역의 평균 밝기를 계산하여 심장 수축과 이완에 따른 주기적인 밝기 변화를 시간 신호(time-series signal)로 변환하였다. 이렇게 얻은 신호를 기반으로 심박수가 지속적으로 계산되고 프로그램 화면에 실시간으로 표시되었다. 즉 이 소프트웨어는 단순한 영상 확인 도구가 아니라, **영상 입력 → ROI 설정 → pixel intensity 추출 → 시간 신호 생성 → 심박수 계산 → 실시간 표시**의 과정을 하나의 분석 시스템으로 자동화하는 역할을 한다. 이처럼 high-throughput이 가능했던 이유는 고속 카메라에 더해 영상에서 심장 신호를 자동으로 추출하고 즉시 분석하는 소프트웨어가 함께 사용되었기 때문이다.



심장 신호는 100 fps의 sampling rate로 1초 동안 기록되었다. 심박수를 정밀하게 계산하기 위해 먼저 Fast Fourier Transform(FFT)을 사용하여 시간에 따른 intensity 신호에서 대략적인 주파수를 추정하였다. 이후 이 초기값을 Fourier series model에 적용하고, Levenberg–Marquardt algorithm을 이용한 non-linear least-squares fitting으로 주파수를 보다 정밀하게 보정하였다. 또한, fitting accuracy와 computational efficiency 사이의 균형을 위해 third-order Fourier model을 사용하였으며, 마지막으로 계산된 fundamental frequency에 60을 곱하여 beats per minute(bpm) 단위의 심박수로 변환하였다.



&#x09;**2.3. Probability density function(PDF) modelling**에서는 개별 Daphnia의 심박수를 측정한 이후, 한 마리의 심박수 값 자체보다 전체 집단에서 심박수가 어떤 형태로 분포하는지를 분석하고자 하였다. 즉, 이 단계부터는 단일 개체의 심박수 측정보다 population-level variability를 해석하는 것이 핵심적으로 서술된다.



먼저, 각 개체의 심박수 값을 이용해 histogram을 구성하였다. 이 때 histogram의 bin width는 Fourier fitting 과정에서 발생하는 measurement uncertainty의 약 2.5배인 6 bpm으로 설정하였다. bin width가 지나치게 작으면 측정 noise까지 세부적인 변화처럼 나타날 수 있고, 반대로 지나치게 크면 실제로 존재하는 분포의 특징이 사라질 수 있다. 따라서  측정 불확실성을 고려하여 noise와 실제 생물학적 variation 사이의 균형을 맞출 수 있음을 확인할 수 있다.



하지만 histogram은 데이터를 일정한 구간으로 나누어 막대로 표현하는 방식으로, 실제 underlying distribution을 연속적으로 표현하는 데에는 한계가 있어서 보완을 위해  Kernel Density Estimation(KDE)을 적용하여 부드러운 probability density function(PDF)을 생성한다.

KDE에서는 Gaussian kernel을 사용하였다. 각 관측값 주변에 작은 Gaussian-shaped kernel을 배치하고 이를 모두 합산함으로써 전체 데이터가 어떤 밀도 분포를 이루는지를 연속적인 곡선으로 표현하는 방식이다. 이를 통해 단순히 평균 심박수를 보는 것이 아니라 어느 심박수 구간에 개체가 많이 존재하는지 분포가 여러 peak를 가지는지 등을 쉽게 확인할 수 있다.



KDE에서 중요한 요소 중 하나는 bandwidth이다. bandwidth는 각각의 데이터가 주변에 어느 정도 범위까지 영향을 미칠지를 결정하고 분포 곡선의 smoothing 정도를 결정한다. bandwidth가 너무 작으면 곡선이 지나치게 울퉁불퉁해져 개별적인 noise까지 구조처럼 나타날 수 있고, 반대로 너무 크면 서로 다른 반응 집단이 하나의 분포로 뭉개질 수 있다. 본 연구에서는 bandwidth를 Scott’s rule을 이용하여 계산한다.



&#x09;**2.4. Quantitative subpopulation analysis**에서는 KDE를 통해 얻은 전체 심박수 분포가 항상 하나의 균일한 집단을 의미하는 것은 아니라고 보고 동일한 물질에 같은 농도로 노출되더라도 Daphnia 개체마다 생리적 민감도가 다를 수 있기 때문에, 하나의 전체 분포 안에 서로 다른 심장 반응을 보이는 여러 subpopulation이 함께 존재할 가능성을 탐구한다. 이러한 잠재적인 하위집단을 분석하기 위해 KDE를 통해 얻은 PDF를 Gaussian component로 분해하였다. 즉, 복잡한 전체 분포를 여러 개의 종 모양 정규분포가 겹쳐진 형태로 해석하고, 각각의 Gaussian component를 서로 다른 심박수 특성을 갖는 잠재적인 subpopulation으로 간주한다.



&#x09;먼저, 전체 분포 안에서 분포 곡선의 기울기 변화가 어떻게 바뀌는지를 분석(second derivative analysis)하여 실제 peak가 존재할 가능성이 높은 위치를 탐색하였다. 이렇게 탐지된 후보 peak들은 이후 Levenberg–Marquardt algorithm를 통해 반복적으로 fitting된다. 이 알고리즘은 각 Gaussian component가 실제 KDE 곡선에 최대한 잘 맞도록 위치, 폭, 높이 등의 parameter를 조정하는 역할을 한다. 이 fitting 과정에서는 convergence tolerance를 10⁻²⁰으로 설정하였다.



&#x09;또한, 전체 분포에서 아주 작은 튐까지 모두 하나의 독립된 subpopulation으로 해석하면 overfitting 문제가 발생할 수 있다. 이를 방지하기 위해 기여도의 5% 미만을 차지하는 peak를 제거하여 매우 소수의 개체 때문에 발생한 작은 분포 변화는 독립적인 population으로 해석하지 않도록 하였다. 추가로 Gaussian component의 값이 음수가 되는 비현실적인 결과를 방지하기 위해 non-negativity constraint를 적용하였다. 이는 확률밀도나 개체 비율이 음수가 될 수 없다는 물리적·통계적 조건을 모델에 반영한 것이다.



&#x09;이후 Gaussian decomposition으로 얻은 exposure group의 peak가 control group과 비교하여 얼마나 이동했는지를 정량적으로 평가하기 위해 Cohen’s distance를 계산하였다. 이는 control에서 나타나는 자연적인 개체 간 변동성을 고려했을 때 exposure로 인한 변화가 충분히 큰지를 평가하기 위해서이다.

논문에서는 exposure group의 peak가 control PDF의 FWHM(Full Width at Half Maximum) 범위를 넘어 이동했다는 것을 의미하는 d ≥ 1을 중요한 기준으로 활용한다.  FWHM은 분포의 최대 높이의 절반이 되는 지점들 사이의 폭으로 control group에서 정상적으로 나타날 수 있는 심박수 분포의 대표적인 폭을 나타내는 하나의 기준으로 사용할 수 있다. exposure 후 peak가 이 범위를 벗어난다면, 자연 변동성 이상의 변화라고 판단할 수 있다는 것이다.



&#x09;Daphnia의 심박수 자체가 원래 개체 간 variability가 큰 특성을 가진다. 때문에 단순히 평균값이 조금 변했다는 이유만으로 toxicity를 선언하는 것이 아니라, control distribution의 자연적 변동 범위를 충분히 넘어서는 변화를 중요한 effect로 해석해야 한다. 

또한, Cohen's distance를 d라 할때, 0.5 ≤ d < 1수준의 변화는 명확한 significant shift로 판단하지 않고 potential trend, 즉 잠재적인 변화 경향으로 기록하였다. 이는 강한 독성 반응과 초기 또는 중간 수준의 생리적 변화를 구분하여 해석하기 위한 것이다. 결론적으로 N = 100의 control group을 기준으로 Daphnia의 physiological heart-rate range을 **274.9 – 388.1 bpm**으로 제시하였다. 그리고 exposure group에서 나타난 peak가 이 control range 밖에 위치할 경우 significant deviation으로 분류하였다. 



###### **\[3. Results and Discussion]**



&#x09; 3장에서는 앞서 설명한 방법론을 실제 실험에 적용했을 때 무엇이 검증되었고, 각 물질에 대해 어떤 심박수 반응이 나타났는지가 핵심이므로 주요 결과와 그 의미를 중시한다.

특히 결과를 볼 때에는 각 물질의 정확한 bpm이나 농도 자체보다는,

* 개발한 시스템이 실제 심박수를 안정적으로 측정할 수 있었는지
* 기존 독성시험보다 낮은 농도에서 sublethal response를 탐지할 수 있었는지
* mean-based analysis와 distribution-based analysis가 어떤 차이를 보여주는지

를 중심으로 확인하였다.



**3.1–3.4. 주요 실험 결과**

|구분|핵심 결과|의미|
|-|-|-|
|고정 방법 검증|Cotton-based immobilisation + 30분 안정화에서 353.0 ± 57.2 bpm으로, methyl cellulose 및 cover glass 방식보다 심박수와 변동성이 낮게 나타남|측정을 위한 고정 과정 자체에서 발생하는 stress를 감소시켜 보다 physiological한 심박수 측정 가능|
|자동 심박수 측정 검증|Manual counting은 6 Hz, Fourier-based analysis는 5.76 ± 0.09 Hz로 유사하게 측정됨|Fourier 기반 자동 분석이 실제 심박수를 정확도 있게 추정할 수 있음을 확인|
|High-throughput 성능|시간당 최대 150마리의 Daphnia 심박수를 측정 가능|많은 개체의 데이터를 빠르게 확보하여 population-level analysis 가능|
|적정 표본 수|N ≥ 63부터 심박수 분포가 안정화되었으며 이후 실험에서는 N = 100 사용|소수 개체의 평균보다 충분한 표본을 이용한 분포 분석이 필요함을 확인|
|H₂O₂|Control MHR 331.53 bpm → 242.82 bpm|H₂O₂에 의해 심박수가 감소하는 bradycardia를 탐지|
|Caffeine|MHR 417.74 bpm, distribution variability 증가|심박수를 증가시키는 tachycardia 반응을 탐지|
|Potassium dichromate|농도가 증가할수록 MHR 감소|기존 immobilisation threshold보다 낮은 농도에서도 sublethal inhibitory response를 탐지|
|Paraquat|심박수가 증가하며 5.0 ppm에서 bimodal distribution 발생|단순 평균뿐 아니라 분포를 분석함으로써 서로 다른 반응 집단의 존재를 추정 가능.|
|AuNPs|전체 분포와 평균 변화는 크지 않았으나, 높은 농도에서 최대 31.2%의 개체가 500 bpm 이상의 비정상적인 심박수를 나타냄|평균값에 가려질 수 있는 population heterogeneity 및 민감한 일부 개체의 반응을 확인|
|CuONPs|1.5 ppm 이상에서 뚜렷한 심박수 증가, 높은 농도에서는 약 450–600 bpm까지 증가|기존 acute toxicity 기준보다 낮은 농도에서도 초기 physiological disturbance가 탐지 가능함을 확인|



&#x09;**3.5. Strengths, limitations and future perspectives**



**Strengths**

* Stress-minimised immobilisation과 자동화된 high-throughput heart rate analysis를 결합함.
* 시간당 최대150마리의 Daphnia 심박수를 분석할 수 있음.
* 평균 심박수만 비교하지 않고 전체 heart rate distribution을 분석함.
* Gaussian deconvolution을 통해 서로 다른 반응을 보이는 subpopulation 후보를 추정함.
* 평균값만으로는 놓칠 수 있는 미세한 심박수 변화와 population-level heterogeneity를 탐지할 수 있음.
* 기존 immobilisation이나 mortality와 같은 endpoint보다 더 이른 단계의 physiological disruption을 탐지할 가능성을 제시함.



**Limitations**

* Gaussian deconvolution으로 구분된 subpopulation은 현재로서는 통계적으로 분리된 집단임.
* 각 Gaussian component가 실제로 서로 다른 생물학적 집단을 의미하는지는 아직 검증되지 않음.
* 특정 peak가 서로 다른 physiological state나 toxicity mechanism을 나타낸다고 해석할 가능성은 있지만, 현재 분석만으로는 이를 확정할 수 없음.
* molecular 또는 genetic biomarker를 이용한 biological validation이 추가로 필요함.
* Daphnia의 cardiac regulation 자체에 대한 기초 연구가 더 필요함.



**Future perspectives**

* 현재 방법을 standardised protocol로 발전시킬 필요가 있음.
* 다양한 particle type으로 적용 범위를 확대할 필요가 있음.
* 실제 환경에 가까운 exposure condition에서도 검증이 필요함.
* Bayesian mixture modelling이나 machine learning clustering을 적용하여 subpopulation 구분과 해석을 개선할 수 있음.
* 심박수 변화와 실제 toxicological pathway를 연결하는 mechanistic study가 필요함.
* 검증이 진행될 경우 환경위해성 평가 및 규제적 활용 가능성이 더욱 높아질 수 있음.



###### **\[4. Conclusion]**



&#x09;이 연구는 Daphnia magna의 심박수를 stress-minimised immobilisation, high-speed imaging, Fourier 기반 자동 분석과 결합해 시간당 최대 150마리까지 측정할 수 있는 high-throughput monitoring system을 제시했다. 이를 통해 대규모 데이터를 확보할 수 있게 되면서 기존의 mean-based endpoint 대신  distribution-based 와 probabilistic analysis를 통해 population-level heterogeneity를 확인할 수 있도록 하였다.



&#x09;이는 낮은 농도의 화학물질과 나노입자 노출에서도 기존 immobilisation이나 EC50 중심 평가보다 이른 sublethal physiological change를 탐지할 가능성을 보였고, CuONPs와 AuNPs 실험에서는 평균값만으로는 놓칠 수 있는 개체별 반응 차이도 확인했다. 따라서 이 방법으로 측정한 heart rate는 기존 endpoint를 보완할 수 있는 quantifiable, non-lethal physiological endpoint가 될 수 있으며, emerging contaminants에 대한 보다 sensitive하고 non-invasive한 environmental risk assessment 도구로 활용될 가능성이 있다.

