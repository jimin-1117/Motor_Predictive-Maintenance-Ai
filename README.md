# ⚙️ 주파수 해석 + CNN 기반 유도전동기 고장 진단


## 🎯 연구 목표
> **"잡음이 있는 진동 데이터에서도 안정적인 고장 진단"**

- 유도전동기 **진동 센서 데이터** 수집  
- 시간 도메인 데이터 → **FFT 주파수 해석**  
- 잡음(화이트 가우시안 노이즈, Bias) 환경 가정  
- **CNN 분류 모델** 설계 및 평가  


## ⚡ 시스템 아키텍처
- **데이터 전처리**: FFT 변환, DC 성분 제거  
- **주파수 특징 추출**: 진폭 상위 5개 주파수 선택  
- **CNN 모델 입력**: Conv1D 기반 1차원 합성곱 계층  
- **출력 클래스**: Normal, Rotor Fault, Bearing Fault
<img width="299" height="157" alt="image" src="https://github.com/user-attachments/assets/d66c8cf7-e3fc-461e-af4d-292db41273f6" />



## ✨ 주요 기능
✅ FFT 기반 **주파수 해석으로 잡음 영향 최소화**  
✅ **CNN 분류 모델**로 3가지 상태(정상/회전자/베어링) 진단  
✅ **화이트 가우시안 노이즈(WGN) & Bias** 환경 실험  
✅ **잡음 환경에서도 100% 분류 정확도 달성** 


## 🧪 실험 결과
- 데이터셋: 정상/회전자 고장/베어링 고장 (각 100쌍, 총 300)  
- **훈련/테스트 분할**: 210 (train), 90 (test)  
- Epoch = 20, Batch size = 16  

**결과**
- WGN 추가 (분산 0.01~0.1) → **100% 정확도**

<img width="301" height="314" alt="image" src="https://github.com/user-attachments/assets/2425a2ed-0ef8-436e-9b4e-69f35e25fc6d" />

- Bias 추가 (0.05 ~ 1.0) → **100% 정확도**

<img width="299" height="287" alt="image" src="https://github.com/user-attachments/assets/155e7d26-1aa1-4f02-94fd-e99e5a43f1ab" />


## 📄 Publication
김민규, 권효선, 유지민, 이호형, 최진우, 이인수. (2024-11-21). 주파수 해석과 CNN을 이용한 진동 센서에 잡음이 있는 유도전동기 시스템의 고장 진단. Proceedings of KIIT Conference, 제주.
[주파수 해석과 CNN을 이용한 진동 센서에 잡음이 있는 유도전동기 시스템의 고장 진단.pd.pdf](https://github.com/user-attachments/files/22311524/CNN.pd.pdf)


## 🏆 Awards
- **우수논문상 (은상)**, 한국정보기술학회 대학생논문경진대회, 2024
[우수논문상(동상).pdf](https://github.com/user-attachments/files/22311531/default.pdf)
