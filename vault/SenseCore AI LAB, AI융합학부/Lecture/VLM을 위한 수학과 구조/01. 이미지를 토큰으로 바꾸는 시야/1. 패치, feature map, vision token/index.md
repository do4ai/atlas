---
title: "1. 패치, feature map, vision token"
source_kind: page
---
이미지를 VLM이 읽으려면 먼저 시각 정보를 토큰처럼 다룰 수 있어야 합니다. 이 강의는 pixel이 patch로 묶이고, patch가 feature map과 token 시퀀스로 바뀌는 과정을 설명하는 출발점입니다.

# 먼저 알아둘 말
- patch: 이미지를 일정 크기 블록으로 나눈 단위입니다.
- feature map: 인코더가 추출한 중간 시각 표현입니다.
- token sequence: 언어 토큰처럼 순서 있는 벡터 목록입니다.
- spatial resolution: 공간 해상도입니다.
- pooling: 표현을 압축하는 연산입니다.

# 이 강의에서 답할 질문
- 이미지를 왜 토큰처럼 바꾸어야 하는가?
- patch와 feature map은 어떤 관계인가?
- vision token 수가 늘어나면 무엇이 좋아지고 무엇이 어려워지는가?

# 왜 중요한가
- 이미지가 시퀀스로 보이지 않으면 Transformer 계열 결합을 읽기 어렵습니다.
- 해상도와 토큰 수의 trade-off를 이해해야 계산량 문제를 설명할 수 있습니다.

# 앞으로 깊게 다룰 핵심 포인트
- patch embedding과 지역 정보 손실
- feature map에서 token sequence로 바꾸는 방법
- CLS token, pooled token, dense token의 차이
- spatial locality와 global context의 균형

# 적용 장면
- 문서 OCR에서는 작은 글자를 살리기 위해 더 촘촘한 시각 토큰이 필요합니다.
- general captioning에서는 압축된 전역 표현이 더 효율적일 수 있습니다.

# 스스로 점검
1. patch와 feature map의 차이를 설명하라.
2. 시각 토큰 수가 많아질 때 생기는 계산 문제를 말하라.
3. 왜 이미지도 시퀀스로 읽는 관점이 필요한지 설명하라.
