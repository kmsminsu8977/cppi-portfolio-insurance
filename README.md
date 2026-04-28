# CPPI Portfolio Insurance

CPPI 포트폴리오 보험 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 초기 보호수준을 유지하면서 상승장 참여도를 높이려면 multiplier가 어떤 역할을 하는가?

## 작업 기준 문서

- `AGENTS.md`: 저장소 작업 기준과 품질 기준
- `SOURCE.md`: KAIST-DFMBA 참고 경로와 프로젝트별 컨텐츠 재구성 기준

## 저장소 구조

```text
cppi-portfolio-insurance/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- cushion은 portfolio value와 고정 floor의 차이로 정의한다.
- 위험자산 비중은 multiplier x cushion/value로 계산하고 0~100%로 제한한다.
- 시장 경로는 floor와 cushion 변화가 보이도록 구성한 합성 수익률이다.

## 주요 파일

- `src/cppi_baseline.py`: 고정 floor와 multiplier를 사용해 위험자산 노출이 어떻게 동적으로 변하는지 계산한다.
- `data/sample/strategy_returns.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
