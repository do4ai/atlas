---
title: "11. hallucination, faithfulness, evaluation"
source_kind: page
---
멀티모달 모델은 답을 잘 쓰는 것만으로 충분하지 않습니다. 이 강의는 hallucination과 faithfulness를 기준으로 VLM 평가 문제를 정리하는 초안입니다.

# 먼저 알아둘 말
- hallucination: 입력에 없는 내용을 그럴듯하게 만들어 내는 오류입니다.
- faithfulness: 출력이 입력 근거를 충실히 반영하는 정도입니다.
- benchmark: 모델을 비교하기 위한 평가 세트입니다.
- calibration: 모델 확신과 실제 정확도의 일치 정도입니다.
- human evaluation: 사람 판단이 포함된 평가 방식입니다.

# 이 강의에서 답할 질문
- 유창한 답과 grounded한 답은 어떻게 다른가?
- 자동 지표만으로 VLM 품질을 충분히 볼 수 있는가?
- hallucination 완화는 왜 구조, 데이터, 평가가 함께 가야 하는가?

# 왜 중요한가
- 멀티모달 제품은 잘못된 근거 제시가 신뢰를 빠르게 무너뜨립니다.
- evaluation 프레임이 잘못되면 모델 개선 방향도 틀어집니다.

# 앞으로 깊게 다룰 핵심 포인트
- object hallucination과 relation hallucination
- answer correctness와 evidence faithfulness 구분
- benchmark leakage와 evaluation gap
- reference-free evaluation의 한계

# 적용 장면
- 의료 이미지나 산업 검사처럼 근거가 중요한 영역에서는 faithfulness가 더 중요합니다.
- 일반 소비자 앱에서도 이미지 설명 오류는 사용자 신뢰를 크게 해칠 수 있습니다.

# 스스로 점검
1. hallucination과 faithfulness를 구분해 설명하라.
2. 자동 지표의 한계를 한 가지 이상 말하라.
3. 왜 평가 설계가 모델 설계만큼 중요한지 설명하라.
