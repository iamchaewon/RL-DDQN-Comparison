# RL-DDQN-Comparison

Deep Reinforcement Learning with Double Q-learning 논문을 LunarLander-v3환경 기반으로 재현
이 프로젝트는 **Double DQN(2016)** 논문의 결과를 재연하고, 타겟 업데이트 주기($C_{freq}$)에 따른 학습 안정성을 분석합니다.

## 실행 가이드

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OEy7TRUwChWN3KrT9TuGxqpCCDHsRSyN#scrollTo=CH2-KiZAOvFo)

**단계:**
1. 코랩 상단 배지를 클릭하여 노트북을 엽니다.
2. `런타임` -> `런타임 유형 변경` -> **T4 GPU** 선택.
3. `1. 환경 설정`과 `2. 데이터 로드` 셀을 차례로 실행하면 즉시 최종 비교 그래프를 생성합니다.

**결과 즉시 확인**
이미 학습된 데이터 파일(all_experiment_results_2.npy)을 깃허브에서 자동으로 로드하여 약 10초 내에 최종 신뢰구간 그래프를 생성합니다.
노트북의 Load Data 셀 내 CLEAN_START = False 설정을 유지한 채 실행합니다.

**전체 학습 재현**
모든 하이퍼파라미터 설정과 3개 Seed 실험을 처음부터 다시 실행하여 성능을 검증합니다. (약 2~3시간 소요)
노트북의 Load Data 셀에서 **CLEAN_START = True**로 변경한 후 실행하여 기존 데이터를 초기화합니다.
환경 설정 및 알고리즘 정의 셀부터 순차적으로 실행하여 총 12가지의 실험(4개 비교군 x 3개 Seed)을 진행합니다.


## 실험 요약
- **DDQN의 우위:** 과대평가 편향을 제거하여 DQN보다 안정적인 수렴과 높은 점수를 기록함.
- **$C$ 최적화:** LunarLander-v3 환경에서는 $C=1000$일 때 최적의 균형을 보임.


## 종속성 안내
Windows 로컬 환경에서 실행하려면 C++ 컴파일러(Build Tools) 설치가 필수적입니다. 코랩 사용을 권장합니다.
