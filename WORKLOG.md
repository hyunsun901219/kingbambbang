# 작업 이력 (WORKLOG)

앞으로 진행하는 작업을 날짜순으로 기록합니다. 최신 항목이 위로 오도록 작성합니다.

---

## 2026-08-07 — SX3K Coating D.O.E Report 틀 작성

- JG EV Coating D.O.E Report 양식(구조) 전달받아 SX3K 버전 제작 (디자인은 기존 GlowOne 스타일 유지)
- `docs/SX3K-Coating-DOE-Report.pptx` 생성 (5장 구성)
  1. 목적 / 재원(Coating liquid·Machine — 공급사/Type 미정) / Base Parameter(토출압, Tap/Fuse Nozzle Speed 미정)
  2. DOE results — M/C Head별 중량 측정 사진 그리드 (No × Fuse1/Tap×3/Fuse, M/C 구성은 SX3K 기준으로 수정 예정)
  3. DOE results — Tap/Fuse 중량(g) 데이터 표 (15회 + MIN/MAX/AVR, 값 미기입)
  4. 두께 측정 이미지 — Point.1 [부위명 미정] / Point.2 (커넥터) × PCB Board #1~3
  5. Summary — Coating Area Size, 평균 중량, SPEC 산정 문구 틀 (수치 미정)
- 두께 측정 사진 4종 전달받음 → 측정 부위 4곳으로 확정 (Point 순서는 확인 필요)
  - 센싱탭: 1292 / 1098 / 1105 / 1225 um
  - 퓨즈: 903 / 784 / 843 um
  - 커넥터: 689 / 748 / 986 / 954 um
  - NTC: 154(?) / 159 / 203 um
- 다음 할 일: 실제 SX3K 섹션 자료 수신 후 데이터 기입 (재원, Base Parameter, 측정값, Summary 수치)

## 2026-08-05 — BJ 검사기 설비 셋업 완료 보고서 작성

- 회사 양식(GlowOne, JG EV 검사기 Set-Up 완료 보고서 PPT) 확인 → 동일 구조로 BJ 버전 PPT 제작
- `docs/BJ검사기-Set-Up-완료보고서.pptx` 생성 (4:3, 5장 구성)
  1. 표지 — 제목 / 결재란(작성·검토·실장·부문장·대표) / EV생산기술팀 / 2026-08-05
  2. 설비 셋업 LAY OUT — 도면·사진 자리 비움 (사용자가 직접 삽입 예정)
  3. 내전압&절연저항 검사기 (HIPOT Test Machine) — S/N 미정, 셋업 결과: 만족
  4. EOL (EOL Test Machine) — S/N 미정, 셋업 결과: 만족
  5. BJ EV INLINE UPH 표 — 수치 미정 `[ ]` 상태
- 참고: `docs/BJ검사기-설비셋업-완료보고서.md` (초기 Markdown 초안, 항목 참고용)
- BSA EOL 이슈 시트 5건(No. 6/7/8/12/23) 전달받아 "셋업 이슈 및 대책" 슬라이드(4p) 추가 → 총 6장
  - 상세 기록: `notes/2026-08-05-BSA-EOL-셋업이슈.md`
- 다음 할 일: 설비 S/N, UPH 수치 확정값 기입, 사진 삽입(사용자), 이슈 대책 완료 여부 확인 후 문구 업데이트

## 2026-08-05 — 저장소 초기 설정

- 자동차 생산기술 작업을 정리·보관하기 위한 저장소 구조 생성
- `docs/`, `projects/`, `notes/` 폴더 및 README, WORKLOG 작성
- 이후 세션에서는 이 파일을 먼저 읽고 작업 맥락을 파악할 것
