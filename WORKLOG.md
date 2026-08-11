# 작업 이력 (WORKLOG)

앞으로 진행하는 작업을 날짜순으로 기록합니다. 최신 항목이 위로 오도록 작성합니다.

---

## 2026-08-11 — BJ CAPA 확대 제안서 (최종 전문가 버전)

### 단계별 버전 진화:
1. **시각 버전** (build_capa_visual.js, pptxgenjs) — 226KB
   - 막대 차트, 공정 흐름도, 색상 박스 다이어그램
   - 사용자 피드백: "디자인이 너무 구리고 딱딱한데 그냥 트렌드 하게 바꿔줘"

2. **모던 버전** (build_capa_modern.js, pptxgenjs) — 트렌드 디자인 시도
   - 다크/라이트 모드, 그래디언트, 큰 타이포그래피(52pt), 이모지, 둥근 모서리
   - 사용자 피드백: "글로우원 정식 템플릿 미포함, 이모지와 그래프가 애들 장난감 같음, 아예 새로 만들자"

3. **전문가 버전** (build_capa_professional.py, python-pptx) — **최종 선택** ✓
   - GlowOne 정식 템플릿(jg_setup.pptx) 기반
   - 10장 구성 (표지 + 9장 내용)
   - `docs/BJ-CAPA-제안서-전문.pptx` 생성 (27MB)

### 최종 전문 제안서 구성 (10장):

**Slide 1 (표지)**: 제목 / 결재 영역 / 팀명 / 날짜

**Slide 2 (Executive Summary)**: 
- 현황: 1차 코팅 300 UPH 병목
- 4가지 전략 요약
- 기대 효과: 모든 공정 2배 이상 증대
- 투자 규모: 총 701,000만원
- ROI: 14개월 회수

**Slide 3 (Current Process Analysis)**:
- 4개 공정 상태 테이블 (SMT 424 UPH, 1차 300, 2차 343, 검사 400)
- 병목 공정 분석: 1차 코팅 12.0s C/T
- 각 공정별 개선 기회점 설명

**Slide 4 (Strategy 1 - SMT Dual Reflow)**:
- 현황 vs 개선안 비교
- 효과: 424→800+ UPH (+88%), 8.5→4.3s C/T (-49%)
- 투자: ~50,000만원
- 회수기간: 8개월

**Slide 5 (Strategy 2 - 1st Coating Dual-Nozzle)**:
- 단일노즐 vs 이중노즐 비교
- 효과: 300→600 UPH (+100%), 12.0→6.0s C/T (-50%), 2→4개 동시 처리
- 투자: ~15,000만원
- ROI: ~6개월

**Slide 6 (Strategy 3 - 2nd Coating Parallel Line)**:
- 설비 구성 표 (Mi-1400×2, Mi-1600TG×1, MC-2000UV×1, Loader/UnLoader)
- 효과: 343→686+ UPH (+104%), 평행 운영으로 간섭 해소
- 투자: ~516,000만원
- 회수기간: 15개월
- 구체적 구현 일정

**Slide 7 (Strategy 4 - Inspection Automation)**:
- 자동화도 개선: 60%→95%
- HIPOT/EOL 채널 최적화
- 엘리베이터 자동화
- 효과: 400→750 UPH (+88%), 9.0→4.8s C/T
- 투자: ~120,000만원
- 회수기간: 18개월

**Slide 8 (Comprehensive CAPA Effects)**:
- 전체 공정 종합 효과 테이블
- 경제 분석: 225,000 ea/년 추가 생산, 2,250,000만원 추가 연 수익
- 총 투자 701,000만원
- 14개월 회수, 85% IRR

**Slide 9 (Implementation Timeline)**:
- 4단계 구현 계획 (분기별)
- Q1: SMT 구축
- Q2: 1차 코팅
- Q3-Q4: 2차 코팅 라인
- 최종: 검사 자동화
- 마일스톤별 구체적 일정

**Slide 10 (Conclusion)**:
- 5가지 핵심 성과
- 경제 효과 요약
- 전략적 중요성
- 즉시 추진 권고

### 설계 원칙:
- GlowOne 정식 템플릿 준수 (10.8" × 7.5" 슬라이드)
- Navy (#17365D) 헤더, Blue (#0070C0) 악센트
- 전문적 테이블 구조 (헤더-명확한 경계선, 체계적 정렬)
- 기술 용어 및 정량적 분석 강조
- 이모지·그래프·장난감 스타일 완전 제거
- 신뢰성과 전문성 우선
- 영업팀·엔지니어링 팀 모두 대상

## 2026-08-07 — BJ Set-Up 보고서: 원본 템플릿 기반 재생성

- 사용자가 JG EV Volt Sensing PCB ASSY 원본 PPT 업로드 (GlowOne 정식 템플릿 포함)
- 원본 파일의 슬라이드 마스터/레이아웃(로고 이미지, 좌측 바, 장식, 푸터)을 그대로 사용해
  `docs/BJ검사기-Set-Up-완료보고서.pptx` 전면 재생성 (6장: 표지/LAYOUT/HIPOT/EOL/개선·이상 리스트/UPH)
- 빌드 방법: 원본 pptx에 add_slide.py로 슬라이드 1장 복제 → python-pptx로 기존 내용 삭제 후 BJ 내용 삽입
  (빌드 스크립트: 세션 스크래치패드 build_bj_from_template.py — 원본 파일은 대외비라 저장소에 미포함)
- 주의: 원본 JG 파일들(통전검사 방법, Volt Sensing 검증)은 대외비로 판단되어 저장소에 커밋하지 않음

## 2026-08-07 — SX3K 코팅 Section 자료: 원본 템플릿 기반 재생성

- `docs/SX3K-코팅Section-자료.pptx`를 GlowOne 원본 템플릿 기반으로 재생성 (5장)
  1. 표지 (EV생산기술팀 / 2026-08-07)
  2. 코팅 라인 구성 — 확정값 기입 (설비 흐름도 + 품목/규격/수량 표)
  3. 재원 및 Base Parameter — 확정값 기입 (JG 동일)
  4. 부위별 코팅 두께 측정 — 사진 자리 (센싱탭/퓨즈/커넥터/NTC × PCB #1~3)
  5. NTC 도포 방식 검토 — Manual 도포 제안 (사진 자리 2곳)
- 수치 미확정으로 Summary 슬라이드는 제외 (데이터 확정 시 추가 예정)
- 빌드 스크립트: build_coating_from_template.py (세션 스크래치패드)

## 2026-08-07 — SX3K 코팅 Section 자료 작성 (구버전, 위 항목으로 대체)

- 처음에 JG EV Coating D.O.E Report 양식을 전달받아 DOE Report로 만들었으나,
  사용자 정정: **DOE 자료가 아니라 코팅 섹션 자료**이며 JG DOE는 동일 코팅 설비 참고용 → 재구성
- `docs/SX3K-코팅Section-자료.pptx` 생성 (4장 구성, GlowOne 스타일)
  1. 재원(Coating liquid/Machine — 공급사·Type 미정) / Base Parameter(토출압, Tap/Fuse Nozzle Speed 미정)
  2. 부위별 코팅 두께 측정 — Point.1 센싱탭 / P.2 퓨즈 / P.3 커넥터 / P.4 NTC × PCB Board #1~3 (사진 자리)
  3. NTC 도포 방식 검토 — 설비 자동 도포 시 좌/우 편차 불량 예시(422/527/119um) → Manual 도포 적용 제안
  4. Summary — 수치 미정 틀
- 두께 측정 사진 4종 전달받음 (측정값 기록)
  - 센싱탭: 1292 / 1098 / 1105 / 1225 um
  - 퓨즈: 903 / 784 / 843 um
  - 커넥터: 689 / 748 / 986 / 954 um
  - NTC(설비 도포 편차 불량 예시): 422 / 527 / 119 um — 별도 단면 154(?)/159/203 um
- 코팅 설비 내역 전달받음 → "1. 코팅 라인 구성" 슬라이드 추가 (총 5장)
  - 코팅기 3대(일반 Mi-1400 ×2, Tilt Mi-1600TG ×1) + UV 경화기(MC-2000UV) 1대, 전/후단 Loader/UnLoader
  - 단가 포함 내역은 `notes/2026-08-07-SX3K-코팅설비-내역.md`에 내부 기록 (PPT에는 품목/규격/수량만)
- 재원·Base Parameter는 JG와 동일 확인 → 확정값 기입 (Shin Kwang Chemicals HB-2U1S-04 / Micro Line Niddle-Valve / 4~9bar, 40~70, 25~35)
- 다음 할 일: 두께 측정 사진 삽입(사용자), 설비 배치 순서 확인, Summary 수치 확정

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
