---
title: "6. multimodal pretraining objective와 data mixture"
source_kind: page
---
대규모 VLM은 아키텍처만으로 정해지지 않습니다. 이 강의는 어떤 objective를 섞고 어떤 데이터를 혼합하느냐가 왜 핵심인지 설명하는 초안입니다.

# 먼저 알아둘 말
- pretraining objective: 사전학습에서 최적화하는 목표입니다.
- caption pair: 이미지와 설명 문장 쌍입니다.
- interleaved data: 이미지와 텍스트가 교차 배치된 데이터입니다.
- mixture ratio: 여러 데이터 원천을 어떤 비율로 섞는지입니다.
- curriculum: 학습 순서를 설계하는 방식입니다.

# 이 강의에서 답할 질문
- captioning, contrastive, matching objective는 어떻게 다르게 기여하는가?
- 데이터 혼합 비율이 성능과 안정성에 왜 영향을 주는가?
- 웹 데이터와 고품질 curated data는 어떤 장단점을 가지는가?

# 왜 중요한가
- 같은 모델 구조도 어떤 데이터와 loss로 길들였는지에 따라 완전히 다른 성격이 나옵니다.
- VLM은 시각-언어 정합성뿐 아니라 응답 품질까지 요구하므로 objective 설계가 더 민감합니다.

# 앞으로 깊게 다룰 핵심 포인트
- image-text matching과 next-token prediction의 결합
- noisy web-scale data 활용 전략
- OCR-heavy data와 instruction data의 역할
- mixture scheduling과 catastrophic forgetting

# 적용 장면
- 문서 이해용 VLM은 일반 웹 캡션 데이터만으로는 성능이 부족할 수 있습니다.
- 대화형 멀티모달 assistant는 instruction-style data가 별도로 필요합니다.

# 스스로 점검
1. 여러 pretraining objective를 섞는 이유를 설명하라.
2. 데이터 mixture가 모델 성격을 바꾸는 예를 들어라.
3. 왜 VLM 학습에서는 curated data가 특히 중요할 수 있는지 말하라.
