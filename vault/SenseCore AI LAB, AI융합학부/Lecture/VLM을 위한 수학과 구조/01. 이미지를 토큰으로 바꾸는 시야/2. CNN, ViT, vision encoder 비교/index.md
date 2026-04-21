---
title: "2. CNN, ViT, vision encoder 비교"
source_kind: page
---
VLM의 시각 입력은 어떤 vision encoder를 쓰느냐에 따라 성질이 달라집니다. 이 강의는 CNN과 ViT가 시각 정보를 요약하는 방식의 차이를 비교하는 초안입니다.

# 먼저 알아둘 말
- receptive field: 한 표현이 참조하는 입력 범위입니다.
- convolution: 지역 가중치 공유 연산입니다.
- self-attention: 토큰 간 관계를 직접 계산하는 연산입니다.
- inductive bias: 모델이 기본적으로 갖는 구조적 선호입니다.
- backbone: 상위 모델의 기반 인코더입니다.

# 이 강의에서 답할 질문
- CNN과 ViT는 무엇을 다르게 잘하는가?
- vision encoder 선택이 downstream VLM 품질에 어떤 영향을 주는가?
- local bias와 global relation은 어떻게 균형을 잡는가?

# 왜 중요한가
- 같은 connector를 써도 vision encoder가 다르면 전체 VLM의 정보 품질이 달라집니다.
- OCR, region reasoning, dense grounding에서는 시각 인코더 선택이 더 민감합니다.

# 앞으로 깊게 다룰 핵심 포인트
- CNN의 locality bias
- ViT의 patch token interaction
- pretrained vision backbone 재사용 전략
- 고해상도 입력에서의 계산량과 성능

# 적용 장면
- 일반 이미지 이해는 강한 pretrained ViT backbone이 유리할 수 있습니다.
- 세밀한 시각 구조를 다루는 작업은 convolutional prior가 여전히 의미가 있습니다.

# 스스로 점검
1. CNN과 ViT의 inductive bias 차이를 설명하라.
2. vision encoder 선택이 OCR 성능에 영향을 주는 이유를 말하라.
3. backbone 품질이 connector 설계와 왜 함께 논의되어야 하는지 설명하라.
