---
title: "8. cross-attention, Q-Former, resampler"
source_kind: page
---
이미지 토큰이 너무 많고 language model은 그대로 두고 싶을 때, 중간 연결기는 핵심 부품이 됩니다. 이 강의는 cross-attention과 Q-Former, resampler 계열을 비교하는 초안입니다.

# 먼저 알아둘 말
- query token: 필요한 정보를 끌어오기 위해 쓰는 질의 벡터입니다.
- key/value: attention에서 참조되는 표현입니다.
- resampler: 많은 시각 토큰을 더 작은 집합으로 압축하는 모듈입니다.
- bottleneck token: 정보 압축을 담당하는 제한된 토큰 집합입니다.
- latent query: 직접 학습되는 질의 토큰입니다.

# 이 강의에서 답할 질문
- 왜 모든 vision token을 그대로 LM에 넣지 않는가?
- Q-Former는 어떤 방식으로 정보를 압축하는가?
- cross-attention 기반 연결기가 선형 projector보다 강한 이유는 무엇인가?

# 왜 중요한가
- connector는 계산량 문제와 정보 품질 문제를 동시에 다룹니다.
- modern VLM 설계 차이의 상당 부분이 이 중간 연결기에 있습니다.

# 앞으로 깊게 다룰 핵심 포인트
- learnable query token의 의미
- Perceiver-style resampling
- token compression과 grounding의 관계
- fixed bottleneck이 만드는 한계

# 적용 장면
- 고해상도 이미지나 긴 비디오에서는 resampler가 사실상 필수에 가깝습니다.
- region grounding이 중요하면 압축 과정에서 무엇을 잃는지 더 민감하게 봐야 합니다.

# 스스로 점검
1. Q-Former의 목적을 설명하라.
2. resampler가 필요한 이유를 말하라.
3. cross-attention connector가 richer interaction을 만드는 이유를 설명하라.
