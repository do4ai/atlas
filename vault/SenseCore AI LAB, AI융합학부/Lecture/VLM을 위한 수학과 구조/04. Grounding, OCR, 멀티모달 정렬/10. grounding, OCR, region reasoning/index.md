---
title: "10. grounding, OCR, region reasoning"
source_kind: page
---
VLM이 실제 입력을 근거로 답하고 있는지 보려면 grounding을 먼저 봐야 합니다. 이 강의는 OCR과 region reasoning을 grounding 문제 안에서 읽는 초안입니다.

# 먼저 알아둘 말
- grounding: 답변이 실제 입력 영역에 근거하는 성질입니다.
- OCR: 이미지 속 글자를 읽는 문제입니다.
- region: 이미지 안의 특정 부분이나 객체 영역입니다.
- localization: 필요한 영역을 찾는 문제입니다.
- relation reasoning: 객체 간 관계를 추론하는 문제입니다.

# 이 강의에서 답할 질문
- OCR은 왜 일반 captioning보다 어려운가?
- region reasoning은 어떤 종류의 시각-언어 결합을 요구하는가?
- grounding이 약하면 왜 자연스럽지만 틀린 답이 나오는가?

# 왜 중요한가
- 실제 제품에서는 문서, UI, 차트, 표 같은 장면에서 grounding 실패가 치명적입니다.
- region-level reasoning은 VLM이 진짜로 "보고 있는지"를 드러내는 시험대입니다.

# 앞으로 깊게 다룰 핵심 포인트
- 작은 텍스트와 고해상도 문제
- 공간 위치 표현과 참조 해석
- box-level supervision과 weak grounding
- OCR-heavy benchmark 읽는 법

# 적용 장면
- 화면 스크린샷 이해에서는 버튼 위치와 레이블을 함께 읽어야 합니다.
- 문서 QA에서는 OCR 오류가 곧 reasoning 오류로 이어질 수 있습니다.

# 스스로 점검
1. grounding과 OCR의 관계를 설명하라.
2. region reasoning이 단순 캡션과 다른 이유를 말하라.
3. grounding이 약할 때 생기는 전형적 오류를 설명하라.
