---
title: "14. multimodal RAG, tool use, agent loop"
source_kind: page
---
멀티모달 시스템은 모델 하나만으로 끝나지 않고 검색과 도구 호출, 반복적 계획까지 확장됩니다. 이 강의는 multimodal RAG와 tool use, agent loop를 다루는 초안입니다.

# 먼저 알아둘 말
- RAG: 외부 지식을 검색해 응답에 결합하는 방식입니다.
- multimodal query: 이미지와 텍스트가 함께 들어가는 질의입니다.
- tool use: 외부 API나 도구를 호출해 문제를 푸는 방식입니다.
- agent loop: 관찰, 계획, 실행, 반영을 반복하는 구조입니다.
- memory: 이전 단계 정보를 저장하고 재활용하는 장치입니다.

# 이 강의에서 답할 질문
- VLM만으로 부족할 때 왜 검색과 도구가 필요한가?
- multimodal RAG는 text-only RAG와 무엇이 다른가?
- agent loop가 붙으면 오류 양상은 어떻게 달라지는가?

# 왜 중요한가
- 실제 업무형 시스템은 정답 생성보다 외부 지식 연결과 실행 능력이 더 중요할 수 있습니다.
- 시각 입력을 포함한 검색과 계획은 일반 LLM 시스템보다 복잡합니다.

# 앞으로 깊게 다룰 핵심 포인트
- 이미지-텍스트 공동 검색 인덱스
- visual evidence를 가진 retrieval
- 도구 호출 실패와 recovery
- planning과 grounding의 결합

# 적용 장면
- 매뉴얼 이미지와 텍스트 문서를 함께 검색하는 지원 assistant가 여기에 해당합니다.
- 화면을 보고 필요한 도구를 호출하는 UI agent도 같은 범주에 들어갑니다.

# 스스로 점검
1. multimodal RAG가 필요한 상황을 예로 들어라.
2. tool use가 붙으면 모델 문제가 왜 시스템 문제로 확장되는지 설명하라.
3. agent loop에서 grounding이 더 중요해지는 이유를 말하라.
