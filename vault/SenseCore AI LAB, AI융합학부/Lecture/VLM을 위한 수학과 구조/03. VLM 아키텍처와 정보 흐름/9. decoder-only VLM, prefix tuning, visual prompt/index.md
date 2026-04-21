---
title: "9. decoder-only VLM, prefix tuning, visual prompt"
source_kind: page
---
최근 VLM은 거대한 language model을 최대한 유지하면서 시각 정보를 앞단에 붙이는 방향도 많이 택합니다. 이 강의는 decoder-only VLM과 visual prompt 계열을 읽는 초안입니다.

# 먼저 알아둘 말
- decoder-only: 다음 토큰 예측 중심의 생성형 언어모델 구조입니다.
- prefix tuning: 입력 앞부분에 학습 가능한 프리픽스를 붙이는 방식입니다.
- visual prompt: 시각 정보를 프롬프트 형태로 주입하는 접근입니다.
- frozen LM: 언어모델 본체를 고정한 상태입니다.
- parameter efficiency: 적은 추가 파라미터로 적응하는 성질입니다.

# 이 강의에서 답할 질문
- 왜 LM을 크게 바꾸지 않고 시각 정보를 붙이려 하는가?
- visual prompt는 실제로 무엇을 대체하거나 보완하는가?
- decoder-only VLM은 어떤 장점과 한계를 갖는가?

# 왜 중요한가
- 대형 LM 생태계에서는 재사용성과 학습 비용이 매우 중요합니다.
- prompt-like injection은 실용적인 시스템에서 자주 등장하는 설계입니다.

# 앞으로 깊게 다룰 핵심 포인트
- prefix token과 visual token의 차이
- LM freezing 전략
- instruction following과 visual prompt의 관계
- 경량 적응과 full fine-tuning 비교

# 적용 장면
- 빠르게 멀티모달 assistant를 붙여야 할 때 decoder-only 접목 방식이 실용적일 수 있습니다.
- 반대로 세밀한 grounding이 중요하면 prompt만으로는 부족할 수 있습니다.

# 스스로 점검
1. decoder-only VLM이 실용적인 이유를 설명하라.
2. visual prompt와 connector의 차이를 말하라.
3. LM을 고정하는 전략의 장단점을 설명하라.
