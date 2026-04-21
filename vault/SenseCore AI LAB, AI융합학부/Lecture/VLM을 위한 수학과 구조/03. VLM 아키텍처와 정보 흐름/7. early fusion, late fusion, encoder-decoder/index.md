---
title: "7. early fusion, late fusion, encoder-decoder"
source_kind: page
---
VLM 구조를 읽을 때 가장 먼저 볼 것은 "이미지와 텍스트가 언제 만나는가"입니다. 이 강의는 fusion 시점과 encoder-decoder 구조 차이를 정리하는 초안입니다.

# 먼저 알아둘 말
- fusion point: 두 모달이 결합되는 지점입니다.
- encoder-decoder: 인코더가 입력을 읽고 디코더가 출력을 생성하는 구조입니다.
- conditioning: 한 입력이 다른 생성 과정을 조건짓는 방식입니다.
- modality bridge: 서로 다른 모달 사이의 연결 통로입니다.
- latency: 실제 추론 지연 시간입니다.

# 이 강의에서 답할 질문
- early fusion과 late fusion은 어떤 문제에 각각 유리한가?
- encoder-decoder 구조는 어떤 상황에서 자연스러운가?
- fusion 지점이 바뀌면 계산량과 정답성은 어떻게 달라지는가?

# 왜 중요한가
- 구조도는 복잡해 보여도 결국 정보가 결합되는 위치를 찾으면 이해가 쉬워집니다.
- VQA, OCR, retrieval, captioning은 요구하는 결합 강도가 서로 다릅니다.

# 앞으로 깊게 다룰 핵심 포인트
- dense interaction과 sparse conditioning
- seq2seq style multimodal generation
- late fusion의 효율성과 한계
- early fusion의 표현력과 비용

# 적용 장면
- captioning은 비교적 늦은 결합으로도 성립할 수 있습니다.
- 세밀한 region reasoning은 더 이른 시점의 상호작용이 필요할 수 있습니다.

# 스스로 점검
1. fusion point가 중요한 이유를 설명하라.
2. early fusion과 late fusion의 trade-off를 말하라.
3. encoder-decoder 구조가 자연스러운 멀티모달 과제를 예로 들어라.
