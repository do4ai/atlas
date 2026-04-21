---
title: "3. projector, adapter, connector"
source_kind: page
---
vision encoder가 좋은 표현을 만들었다고 바로 language model에 연결되지는 않습니다. 이 강의는 두 표현 공간을 이어 주는 projector, adapter, connector의 역할을 정리하는 초안입니다.

# 먼저 알아둘 말
- hidden dimension: 모델 내부 표현 차원입니다.
- projector: 차원을 맞추는 선형 또는 비선형 변환기입니다.
- adapter: 추가 학습 가능한 경량 모듈입니다.
- connector: 시각 표현과 언어 표현 사이의 일반적인 다리입니다.
- bottleneck: 정보량이 줄어드는 구간입니다.

# 이 강의에서 답할 질문
- 단순 선형층으로 충분한 경우와 아닌 경우는 언제인가?
- connector는 정보 압축과 정렬 중 무엇을 담당하는가?
- 왜 connector 설계가 작은 차이로도 전체 VLM 품질을 바꾸는가?

# 왜 중요한가
- 실제 VLM은 vision encoder와 language model을 단순 연결하는 것보다 connector 설계에서 많은 차이가 납니다.
- connector는 계산량, 토큰 수, 정보 손실을 동시에 좌우합니다.

# 앞으로 깊게 다룰 핵심 포인트
- linear projector와 MLP projector 비교
- token compression과 resampling
- frozen backbone 위에서 adapter를 학습하는 전략
- connector를 어디 층에 붙일지 결정하는 문제

# 적용 장면
- 작은 모델에서는 얇은 projector가 효율적일 수 있습니다.
- 복잡한 시각 질의응답에서는 richer connector가 더 나은 grounding을 만들 수 있습니다.

# 스스로 점검
1. projector와 adapter의 역할 차이를 설명하라.
2. connector가 병목이 되면 어떤 현상이 생기는가?
3. 왜 connector는 단순 연결층 이상으로 다뤄져야 하는지 말하라.
