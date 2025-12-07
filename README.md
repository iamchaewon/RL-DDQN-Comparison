# RL-DDQN-Comparison

Deep Reinforcement Learning with Double Q-learning 논문을 LunarLander-v3환경 기반으로 재현
이 프로젝트는 **Double DQN(2016)** 논문의 결과를 재연하고, 타겟 업데이트 주기($C_{freq}$)에 따른 학습 안정성을 분석합니다.

## 빠른 실행 (Quick Start)
긴 학습 시간(약 2시간) 없이 저장된 결과로 그래프를 즉시 보려면 아래 버튼을 클릭하세요.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/iamchaewon/RL-DDQN-Comparison/blob/main/notebooks/LunarLander_DDQN_Final.ipynb)

**단계:**
1. 코랩 상단 배지를 클릭하여 노트북을 엽니다.
2. `런타임` -> `런타임 유형 변경` -> **T4 GPU** 선택.
3. `1. 환경 설정`과 `2. 데이터 로드` 셀을 차례로 실행하면 즉시 최종 비교 그래프를 생성합니다.

## 실험 요약
- **DDQN의 우위:** 과대평가 편향을 제거하여 DQN보다 안정적인 수렴과 높은 점수를 기록함.
- **$C$ 최적화:** LunarLander-v3 환경에서는 $C=1000$일 때 최적의 균형을 보임.


## 종속성 안내
Windows 로컬 환경에서 실행하려면 C++ 컴파일러(Build Tools) 설치가 필수적입니다. 코랩 사용을 권장합니다.
