---
title: "15. diffusion, image generation, unified multimodal model"
source_kind: page
---
멀티모달의 끝은 입력 이해만이 아니라 생성과 통합입니다. 이 강의는 diffusion, 이미지 생성, unified multimodal model을 이어 보는 초안입니다.

# 먼저 알아둘 말
- diffusion: 점진적으로 노이즈를 제거하며 샘플을 생성하는 모델 계열입니다.
- conditional generation: 조건 입력에 맞춰 출력을 생성하는 방식입니다.
- decoder: 잠재 표현에서 실제 출력을 만드는 모듈입니다.
- unified model: 여러 모달과 작업을 하나의 모델로 다루려는 접근입니다.
- modality token: 어떤 모달인지 구분해 주는 토큰 또는 표식입니다.

# 이 강의에서 답할 질문
- 이해형 VLM과 생성형 멀티모달 모델은 어디서 만나는가?
- diffusion은 언어모델 기반 생성과 어떤 점이 다른가?
- unified multimodal model은 왜 매력적이면서도 어려운가?

# 왜 중요한가
- 멀티모달 연구는 검색과 이해에서 끝나지 않고 생성과 행동으로 이어집니다.
- 하나의 모델이 보고, 읽고, 쓰고, 그리는 방향은 실무적으로도 의미가 큽니다.

# 앞으로 깊게 다룰 핵심 포인트
- text-to-image와 image-conditioned generation
- latent space와 token space의 차이
- autoregressive multimodal generation과 diffusion 비교
- unified tokenization의 난점

# 적용 장면
- 사용자가 이미지를 주고 편집 지시를 내리는 생성 시스템이 대표 예입니다.
- 문서, 이미지, 텍스트를 함께 이해하고 다시 생성하는 assistant도 같은 흐름입니다.

# 스스로 점검
1. 이해형 VLM과 생성형 멀티모달 모델의 연결점을 설명하라.
2. diffusion과 autoregressive generation의 차이를 말하라.
3. unified multimodal model이 어려운 이유를 설명하라.
