---
title: "5. hard negative, temperature, retrieval"
source_kind: page
---
contrastive learning은 단순히 loss 식 하나로 끝나지 않습니다. 이 강의는 hard negative와 temperature가 retrieval 품질을 어떻게 바꾸는지 다루는 초안입니다.

# 먼저 알아둘 말
- hard negative: 정답과 헷갈리기 쉬운 오답 예시입니다.
- temperature: similarity 분포를 날카롭게 하거나 완만하게 하는 계수입니다.
- recall: 정답을 얼마나 잘 찾아오는지 보는 지표입니다.
- precision: 찾은 항목 중 정답 비율입니다.
- ranking: 후보들을 순서대로 정렬하는 문제입니다.

# 이 강의에서 답할 질문
- negative가 쉽기만 하면 왜 학습이 약해지는가?
- temperature를 잘못 잡으면 어떤 문제가 생기는가?
- retrieval 평가는 왜 contrastive 학습의 실제 품질과 이어지는가?

# 왜 중요한가
- 실제 멀티모달 정렬 성능은 데이터 구성과 loss tuning에 크게 좌우됩니다.
- hard negative를 이해하면 단순 정확도보다 더 현실적인 구분 능력을 볼 수 있습니다.

# 앞으로 깊게 다룰 핵심 포인트
- batch size와 negative 다양성
- false negative 문제
- temperature와 gradient scale
- retrieval benchmark를 읽는 법

# 적용 장면
- 매우 비슷한 상품 사진을 구분해야 하는 검색 시스템에서 hard negative가 중요합니다.
- 문서 이미지 검색에서는 OCR 노이즈 때문에 ranking 품질이 더 민감해집니다.

# 스스로 점검
1. hard negative가 필요한 이유를 설명하라.
2. temperature가 너무 크거나 작을 때 어떤 현상이 생기는지 말하라.
3. retrieval 지표와 학습 objective의 관계를 설명하라.
