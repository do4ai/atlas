---
title: "12. instruction tuning, RLHF, multimodal alignment"
source_kind: page
---
텍스트-only LLM에서 쓰이던 정렬 기법은 멀티모달에서도 다시 등장하지만 그대로 복사되지는 않습니다. 이 강의는 instruction tuning과 RLHF를 멀티모달 환경에서 다시 읽는 초안입니다.

# 먼저 알아둘 말
- instruction tuning: 지시를 따르도록 모델을 추가 학습시키는 과정입니다.
- preference data: 더 나은 응답을 고르게 한 비교 데이터입니다.
- reward model: 응답 선호를 점수로 근사하는 모델입니다.
- multimodal alignment: 시각 근거와 사용자 선호를 함께 반영하는 정렬입니다.
- safety policy: 응답 제한과 안전 기준입니다.

# 이 강의에서 답할 질문
- 텍스트-only alignment와 멀티모달 alignment는 무엇이 다른가?
- preference 판단에 시각 근거가 들어오면 무엇이 어려워지는가?
- instruction tuning이 grounding 문제를 얼마나 해결할 수 있는가?

# 왜 중요한가
- 멀티모달 assistant는 말투만 좋은 것이 아니라 입력을 제대로 보고 안전하게 답해야 합니다.
- alignment는 응답 스타일, 안전성, 시각 근거성까지 함께 다루게 됩니다.

# 앞으로 깊게 다룰 핵심 포인트
- multimodal SFT 데이터 구성
- visual evidence가 있는 preference comparison
- reward hacking과 fake grounding
- alignment와 capability의 긴장 관계

# 적용 장면
- 화면 도우미나 문서 assistant는 정답뿐 아니라 근거를 제시하는 훈련이 필요합니다.
- 안전 민감 장면에서는 이미지 해석 오류와 정책 위반이 함께 검토되어야 합니다.

# 스스로 점검
1. 멀티모달 alignment가 텍스트-only alignment보다 어려운 이유를 말하라.
2. instruction tuning만으로 해결되지 않는 문제를 설명하라.
3. preference data에 시각 근거가 포함될 때 생기는 난점을 설명하라.
