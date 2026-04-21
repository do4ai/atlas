---
title: "13. video token, temporal modeling, long context"
source_kind: page
---
비디오는 이미지 VLM에 시간축이 추가된 문제입니다. 이 강의는 video token과 temporal modeling, long context를 다루는 초안입니다.

# 먼저 알아둘 말
- frame: 비디오의 한 장면입니다.
- video token: 시간축까지 반영한 시각 토큰입니다.
- temporal modeling: 시간 순서와 변화를 표현하는 방식입니다.
- long context: 매우 긴 입력 시퀀스를 처리하는 문제입니다.
- frame sampling: 모든 프레임 대신 일부를 선택하는 전략입니다.

# 이 강의에서 답할 질문
- 비디오는 왜 이미지보다 훨씬 더 많은 토큰 문제를 만드는가?
- 시간 순서를 무시하면 어떤 종류의 오류가 생기는가?
- frame sampling과 long context 설계는 어떻게 연결되는가?

# 왜 중요한가
- 실제 제품에서는 영상 이해, 화면 녹화 분석, 로봇 관찰 등 시간이 포함된 문제가 많습니다.
- 비디오 VLM은 토큰 폭증과 grounding 악화를 동시에 다뤄야 합니다.

# 앞으로 깊게 다룰 핵심 포인트
- frame-level tokenization
- temporal pooling과 memory token
- event understanding과 causal order
- 긴 비디오에서의 질의응답 전략

# 적용 장면
- 강의 영상 요약은 시간 순서 이해가 중요합니다.
- 화면 녹화 분석은 UI 변화와 사용자 행동의 연속성을 읽어야 합니다.

# 스스로 점검
1. video token이 image token과 다른 점을 설명하라.
2. temporal modeling이 필요한 이유를 말하라.
3. long context가 비디오 VLM에서 왜 핵심인지 설명하라.
