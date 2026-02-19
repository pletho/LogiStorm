# CAPA MVP Light (블럭 텍스트 → 시뮬 → CAPA)

이 프로젝트는 쭌님이 말한 방식 그대로,
- **블럭을 텍스트(JSON)로 정의**
- **시간축 기반(틱) 시뮬레이터로 토큰 흐름 실행**
- **CAPA(THP/병목/큐/붕괴지표) 산출**
을 목표로 하는 라이트 MVP입니다.

## 설치
```bash
npm i
```

## 실행
```bash
npm run run
# 또는
node --loader ts-node/esm src/index.ts --scenario scenarios/adcross_chuncheon_mvp.json
```

## 결과 예시(콘솔)
- THP(시간당 완료 처리량)
- 병목 후보(큐/활용률 기반)
- 최대 큐 길이 / 큐 초과(붕괴) 경고
- 블럭별 요약 통계

## 시나리오 파일
`scenarios/*.json` 형식입니다. 핵심은:
- nodes(블럭 목록)
- edges(연결)
- source(투입률) 및 station/labeler 등의 serviceTime, capacity, queueLimit

> UI(HTML 블럭 카드 + 색상 변경)는 이 엔진 이벤트(BLOCK_ENTER/EXIT/JAM)를 구독해서 붙이면 됩니다.
# LogiStorm
