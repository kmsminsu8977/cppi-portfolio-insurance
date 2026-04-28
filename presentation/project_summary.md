# 발표 초안

## 1. 문제 정의

초기 보호수준을 유지하면서 상승장 참여도를 높이려면 multiplier가 어떤 역할을 하는가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/strategy_returns.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

고정 floor와 multiplier를 사용해 위험자산 노출이 어떻게 동적으로 변하는지 계산한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
