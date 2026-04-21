---
title: "4. CLIP, contrastive learning, shared embedding"
source_kind: page
---
VLM의 많은 출발점은 이미지와 텍스트를 같은 표현 공간에 놓는 문제입니다. 이 강의는 CLIP의 contrastive objective를 기준점으로 삼아 shared embedding의 의미를 정리하는 초안입니다.

# 먼저 알아둘 말
- embedding: 입력을 벡터로 옮긴 표현입니다.
- similarity: 두 벡터의 가깝고 먼 정도입니다.
- positive pair: 대응되는 이미지와 텍스트 쌍입니다.
- negative pair: 대응되지 않는 쌍입니다.
- contrastive loss: 정답 쌍은 가깝게, 오답 쌍은 멀게 만드는 손실입니다.

# 이 강의에서 답할 질문
- shared embedding space는 왜 VLM의 중요한 기반인가?
- CLIP의 loss는 무엇을 밀고 당기는가?
- retrieval과 zero-shot transfer가 왜 여기서 가능한가?

# 왜 중요한가
- 생성형 VLM도 많은 경우 contrastive pretraining의 혜택을 간접적으로 받습니다.
- image-text alignment를 이해해야 이후 grounding 문제도 선명해집니다.

# 앞으로 깊게 다룰 핵심 포인트
- cosine similarity와 정규화
- symmetric contrastive objective
- in-batch negative의 역할
- zero-shot classifier를 읽는 관점

# 적용 장면
- 텍스트 쿼리로 이미지 검색을 할 때 shared space가 직접 쓰입니다.
- 사전학습된 CLIP encoder는 다운스트림 VLM의 시각 정렬 기반이 될 수 있습니다.

# 스스로 점검
1. CLIP의 positive와 negative를 설명하라.
2. shared embedding이 retrieval을 가능하게 하는 이유를 말하라.
3. contrastive alignment가 생성 구조와 어떻게 연결될 수 있는지 설명하라.
