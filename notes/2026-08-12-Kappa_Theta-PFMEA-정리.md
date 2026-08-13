# KAPPA/THETA PFMEA 정리 (Process FMEA)

> 원본: `Kappa_Theta_PFMEA_250304_Rev3.xlsx` (사용자 업로드, 2026-08-12 정리)
> 이 문서는 원본 엑셀의 `Process(K)` 시트(공정 FMEA 본문)를 재구성한 것입니다.

## 1. 개요

| 항목 | 내용 |
|------|------|
| 모델명 | KAPPA/THETA |
| 작성사 (Company) | ㈜글로우원 |
| 고객사 (Customer) | ㈜인지컨트롤스 |
| PFMEA 시작일 | 2023-11-10 |
| 최종 개정일 | 2025-03-04 (Rev.3) |
| Cross-Functional Team | 생산기술 / 품질 / 개발 / 생산관리 |

## 2. 개정 이력

| No. | 개정일 | Ver | 내용 | 작성자 |
|-----|--------|-----|------|--------|
| 1 | 23.11.10 | 0 | Kappa&Theta PFMEA 신규 작성 | 신태양 |
| 2 | 24.03.11 | 1 | 각 공정 관리계획서-FMEA Validation 완료 | 박한열 |
| 3 | 25.03.04 | 2 | Coating 공정 외관검사 추가 | 장현순 |

## 3. 전체 공정 흐름 (31개 공정)

| 공정번호 | Item | Step (설비/공정) | 비고 |
|---------|------|------------------|------|
| 00 | 자재관리 | 자재관리 | 자재 불출 검증 |
| 10 | 수입검사 | 수입검사 | 수입 검사 (치수/외관) |
| 50 | PCB 투입 | VACUUM LOADER | PCB 투입 (Vacuum Loader) |
| 60 | 바코드 마킹 | LASER MARKING | 바코드 마킹 (Laser) |
| 70 | 제품 반전 | 반전기 | 제품 반전 |
| 80 | 바코드 마킹 | INK MARKING | 바코드 마킹 (Ink) |
| 90 | 솔더 도포 | SCREEN PRINTER | 솔더 도포 (Screen Printer) |
| 100 | 솔더 검사 | SPI | 솔더 검사 (SPI) |
| 110 | 부품 실장 | MOUNTER | 부품 실장 (Mounter, SMT) |
| 120 | 솔더 용융 | REFLOW | 솔더 용융 (Reflow) |
| 130 | 부품 검사 | AOI | 부품 검사 (AOI) |
| 150 | PCB 적재 | UNLOADER | PCB 적재 (Unloader) |
| 180 | Module 공정 | ICT | Module 공정 - ICT |
| 190 | Module 공정 | Coating | Module 공정 - Coating (1차) |
| 200 | Module 공정 | Router | Module 공정 - Router |
| 210 | Module 공정 | 케이스 공급 | Module 공정 - 케이스 공급 |
| 220 | Module 공정 | Grease 도포 | Module 공정 - Grease 도포 |
| 230 | Module 공정 | Gear 삽입 | Module 공정 - Gear 삽입 |
| 240 | Module 공정 | GND PIN 삽입 | Module 공정 - GND PIN 삽입 |
| 250 | Module 공정 | PCB 체결 | Module 공정 - PCB 체결 |
| 270 | Module 공정 | 열융착 | Module 공정 - 열융착 |
| 260 | Module 공정 | FLUX 도포 | Module 공정 - FLUX 도포 |
| 280 | Module 공정 | Soldering | Module 공정 - Soldering (Robot) |
| 300 | Module 공정 | Soldering Vison | Module 공정 - Soldering Vision |
| 310 | Module 공정 | Coating | Module 공정 - Coating (2차) |
| 320 | Module 공정 | 다운로드+EOL | Module 공정 - 다운로드+EOL |
| 340 | Module 공정 | 외관검사+포장 | Module 공정 - 외관검사+포장 |
| 350 | GP-12 | GP-12 | GP-12 |
| 360 | 출하검사 | 출하검사 | 출하검사 |
| 380 | 완제품창고 | 포장/완제품창고 | 완제품창고 (포장) |
| 390 | 출하관리 | 출하관리 | 출하관리 |

## 4. 공정별 상세 고장모드 분석 (Failure Mode Analysis)

컬럼 약어: **FE**=고장영향 / **S**=심각도 / **FM**=고장형태 / **FC**=고장원인 / **PC**=예방관리 / **O**=발생도 / **DC**=검출관리 / **D**=검출도 / **AP**=Action Priority / **RPN**=Risk Priority Number(S×O×D)

### 공정 00 — 자재관리 / 자재관리

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| 자재불출 F/P | 자재 오불출 시 제품 사용 불가 | 10 | 자재 오 불출 | 작업자 라벨 오 부착 | 자재 불출 시, 업체라벨 및 당사 라벨 정보 매칭 안될 경우, MES Interlock | 3 | MES Interlock | 1 | L | 30 |

### 공정 10 — 수입검사 / 수입검사

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Measuring device | 제품 조립 시 형합성 불량 | 7 | 치수불량 | 계측기 오류 | 계측기 MSA 실시 | 1 | MSA 점검 check | 4 | L | 28 |
| Operator |  | 7 |  | 검사 기준 상이 | 작업자 MSA | 1 | 검사자 인증 | 4 | L | 28 |

### 공정 50 — PCB 투입 / VACUUM LOADER

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Operator | PCB 역투입 시 Barcode 인쇄 NG | 3 | 인식 불량 | PCB 적재 방법 오류 | 투입 전 인쇄 방향 확인 | 2 | 육안검사 | 4 | L | 24 |

### 공정 60 — 바코드 마킹 / LASER MARKING

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Laser Marking Machine | 제품 이력 관리 불가 | 5 | 인식 불량 | 레이저 헤드 불량 | 작업 전 시현,  설비 알람 발생 | 2 | 일상 점검, Barcode Scanner | 2 | L | 20 |
| Laser Marking Machine |  | 5 |  | 마킹 누락 | 작업 전 시현,  설비 알람 발생 | 2 | 일상 점검, Barcode Scanner | 2 | L | 20 |

### 공정 70 — 제품 반전 / 반전기

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| 반전기 Machine | 마킹 작업 불가 | 3 | 인식 불량 | 반전기 동작 방법 미흡 | 반전 모델 진행 시 AUTO 설정 | 2 | 일상 점검 | 4 | L | 24 |

### 공정 80 — 바코드 마킹 / INK MARKING

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Ink Marking Machine | 제품 이력 관리 불가 | 5 | 인식 불량 | 노즐 막힘, 잉크량 부족 | 작업 전 시현,  설비 알람 발생 | 2 | 일상 점검, Barcode Scanner | 2 | L | 20 |
| Ink Marking Machine |  | 5 |  | 마킹 누락 | 작업 전 시현,  설비 알람 발생 | 2 | 일상 점검, Barcode Scanner | 2 | L | 20 |

### 공정 90 — 솔더 도포 / SCREEN PRINTER

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Screen Print Machine | Soldering Open/Short로 인한 미/오작동 | 7 | 과납 | Squeegee 인쇄조건 설정 미흡 | 인쇄조건 설정(압력/속도) | 3 | 일상 점검 | 2 | L | 42 |
| Mask |  | 8 | 소납/미납 | Metal Mask 세정 미흡 (개구부 막힘 등) | 세척주기 설정 | 3 | 일상 점검 | 2 | L | 48 |
| Solder |  | 8 |  | Solder Paste 장기 사용 | 개봉 후 사용시간 기준 설정 | 3 | Solder 용기에 개봉 라벨 부착, MES interlock | 2 | L | 48 |
| Solder |  | 8 |  | Solder 점도 불량 | 자동교반기 사용 | 3 | Solder viscocity inspection | 2 | L | 48 |

### 공정 100 — 솔더 검사 / SPI

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| SPI Machine | 수율 하락 | 1 | 과검출 | 검사 기준 상이 | 작업표준 설정 | 4 | 일상점검 | 6 | L | 24 |
| SPI Machine | Soldering Open/Short로 인한 미/오작동 | 8 | 미검출 | 설비 측정 오류 | PCB fiducial 인식 | 2 | 전수 검사 | 2 | L | 32 |
| SPI Machine |  | 8 |  | 검사 기준 상이 | Solder Volume 기준 설정 (70~170%) | 3 | 전수 검사 | 2 | L | 48 |
| SPI Machine |  | 4 |  | 설비 이상 발생 | Error / PROOFING 실시 | 2 | 기준미달 상황 발생시(Error 알람 확인) | 3 | L | 24 |

### 공정 110 — 부품 실장 / MOUNTER

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Mounter Machine | 특성 불량으로 인한 미/오작동 | 8 | 오삽 | 장비 설정 미흡 | 오삽방지시스템 | 2 | AOI/ICT 검사 | 2 | L | 32 |
| Mounter Machine | 특성 불량으로 인한 미/오작동 | 9 | 역삽 | 장비 설정 미흡 | 초품 생산 시 역삽 확인 | 3 | AOI/ICT 검사 | 2 | L | 54 |
| Mounter Machine | 특성 불량으로 인한 미/오작동 | 9 | 미삽 | 장비 설정 미흡 | 초품 생산 시 미삽 확인 | 2 | AOI/ICT 검사 | 2 | L | 36 |
| Mounter Machine | 인접 부품 및 패턴간 Short로 인한 미/오작동 | 6 | 치우침(틀어짐) | 좌표셋팅 작업 미흡 | 초품 생산 시 실장 좌표 확인 | 3 | AOI/ICT 검사 | 2 | L | 36 |

### 공정 120 — 솔더 용융 / REFLOW

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Reflow Machine | 외관불량 | 6 | 부품변형 | 온도 PROFILE 설정 미흡 | Reflow 온도Profile 기준 설정  -Preheat (150 ~180℃)    : 60 ~120sec - Melting Zone (220℃ 이상)   : 30 ~ 90sec - Peak temperature   : 230℃ ~ 255℃ | 2 | 온도 Profile 측정 | 4 | L | 48 |
| Reflow Machine | Soldering Open으로 인한 미/오작동 | 8 | 냉납 | 온도 PROFILE 설정 미흡 |  | 2 | 온도 Profile 측정 | 4 | L | 64 |

### 공정 130 — 부품 검사 / AOI

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| AOI Machine | 수율 하락 | 1 | 과검출 | 장비 설정 미흡 | 부품실장 기준서에 의한 스펙관리, Master SPL(OK/NG)점검 | 5 | 전수 검사 | 4 | L | 20 |
| AOI Machine | 제품 미/오작동 | 5 | 납볼 | Solder 품질 관리 미흡 | SPI 전수 검사, AOI 납볼 검출 알고리즘 설정 | 3 | AOI 전수검사 | 2 | L | 30 |
| AOI Machine |  | 7 | 미검출 | 설비 측정 오류 | 부품실장 기준서에 의한 스펙관리, Master SPL(OK/NG)점검 | 2 | 전수 검사 | 4 | L | 56 |
| Operator |  | 7 |  | 불량 확인절차 미준수 (불량 혼입) | 불량 적재(격리) 구역 설정 | 2 | 자동 검사 후 판정 알람 | 2 | L | 28 |

### 공정 150 — PCB 적재 / UNLOADER

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Unloader Machine | 제품 파손 | 8 | 부품 파손 | PUSHER 동작 이상 | PUSHER 위치 및 동작 확인 | 3 | 일상 점검 | 4 | L | 96 |

### 공정 180 — Module 공정 / ICT

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| ICT Machine | 기능 미/오동작 | 7 | 미검출 | SPEC 설정 오류 | 작업표준 설정 및 Data Matrix 검증 | 1 | Master SPL(OK/NG)점검 | 4 | L | 28 |
| ICT Machine |  | 8 | Test Pin PCB 단층 파괴 | Test Pin Type 미검토 및 반복성 Test 미진행 | Test Pin Type 선정 적합성 검토 반복성 Test 진행 | 3 | DOE반복성 Test 단층파괴 검증. Pin 사용 횟수 MES 인터락 | 2 | L | 48 |
| ICT Machine | 수율 하락 | 7 | Test Pin 가성불량 | 가성불량 발생으로 인한, De-Bugging 진행중 Spec 오설정 | Test Pin 수명관리 진행. 마스터샘플 운영관리. | 3 |  | 2 | L | 42 |
| ICT Machine | 제품 파손 | 7 | 캐리어 역투입 | 캐리어 지그 투입 작업 미숙 | 캐리어에 SMD 정방향 화살표 표기 ICT Fixture 역투입 방지 | 2 | Fixture 역투입 안착 불가 Pin 설치 | 1 | L | 14 |

### 공정 190 — Module 공정 / Coating

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Coating Machine | 제품 미/오작동 | 6 | Coating 두께관리 | 장비 설정 미흡 | 도막두께 측정/일 | 3 | 도막두께 측정 시트 | 2 | L | 36 |
| Coating Machine |  | 6 |  |  | 디스펜서 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 24 |
| Coating Machine |  | 6 | Coating 기포 관리 | 장비 설정 미흡 | 코팅액 탱크 관리 설정 | 3 | 설비 일상점검 관리 | 3 | L | 54 |
| Coating Machine |  | 7 | Nozzle 막힘 | 일상 점검 관리 미흡 | 세척액 관리 | 3 | 설비 일상 점검 관리 | 2 | L | 42 |
| Coating Machine |  | 7 | Coation 영역 관리 | 설비 설정 미흡 | 외관 검사 진행 | 3 | 외관 검사 기준서 | 2 | L | 42 |

### 공정 200 — Module 공정 / Router

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Router Machine | 제품 파손 | 7 | 부품 파손 | JIG 제작 오류 | 안착 JIG 제작 관리 검토 | 2 | 실물 형합성 검토 | 3 | L | 42 |
| Router Machine | 조립불가 | 4 | Burr 발생 | Router Bit 관리 미흡 | Bit 교체 관리주기 설정 | 2 | Bit 교체 알람 및 비상정지 Burr Spec Cpk 관리 | 6 | L | 48 |

### 공정 210 — Module 공정 / 케이스 공급

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| CASE | 제품 파손 | 7 | 케이스 파손 | 설비 설정 미흡 | 설비 PICK UP 관리 검토 | 3 | 실물 형합성 검토 | 2 | L | 42 |
| CASE | 제품 파손 | 2 | 케이스 파손 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 3 | 설비 일상점검 관리 | 2 | L | 12 |

### 공정 220 — Module 공정 / Grease 도포

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Grease Machine | 제품 미/오작동 | 7 | grease 도포 범위 | 설비 설정 미흡 | grease 도포 비전검사 실시 | 3 | Grease 도포 영역 버전검사실시 | 2 | L | 42 |
| Grease Machine |  | 7 | 미검출 | 설비 설정 미흡 | 설비 설정 및 Data Matrix 검증 | 3 | Master SPL(OK/NG)점검 | 2 | L | 42 |
| Grease Machine |  | 2 | grease 미도포 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 3 | 설비 일상점검 관리 | 2 | L | 12 |
| Grease Machine |  | 4 | grease 도포 중량 | 설비 설정 미흡 | 그리스 도포 중량 측정 | 2 | 그리스 도포 무게 일상 점검 | 4 | L | 32 |
| Grease Machine |  | 4 |  |  | 디스펜서 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 16 |

### 공정 230 — Module 공정 / Gear 삽입

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Gear | 제품 미/오작동 | 8 | 미체결 발생 | 설비 관리 미흡 | 작업표준 설정 | 3 | 기어 인식 센서 확인 | 1 | L | 24 |
| Gear |  | 1 |  | 설비 관리 미흡 | 진공 압력 일일 점검관리 | 2 | 설비 일상점검 관리 | 1 | L | 2 |
| Gear |  | 1 |  | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 4 |
| Gear |  | 2 | 낙하품 혼입 | 낙하품 관리 미흡 | 낙하품 관리 설정 실시 | 2 | 낙하품 관리 표준 설정 | 1 | L | 4 |

### 공정 240 — Module 공정 / GND PIN 삽입

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| GND PIN | 제품 미/오작동 | 7 | 미체결 | 설비 설정 미흡 | 설비 F'proof 설정 | 3 | GND Pin 유/무 F'proof | 1 | L | 21 |
| GND PIN |  | 1 |  | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 4 |
| GND PIN |  | 1 | 이물 불량 | GND PIN 투입 BOWL 청결 미흡 | GND PIN 투입 BOWL 청소 실시 | 1 | GND PIN 투입 BOWL 주기적청소 실시 | 1 | L | 1 |

### 공정 250 — Module 공정 / PCB 체결

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| PCB 체결 | 제품 미/오작동 | 5 | 제품 파손 | PCB 트레이 관리 미흡 | PCB 트레이 관리 실시 | 3 | 파손, 휨 발생 TRAY 폐기 | 3 | L | 45 |
| PCB 체결 |  | 1 | 미체결 발생 | 설비 설정 미흡 | 진공 압력 일일 점검관리 | 3 | 설비 일상점검 관리 | 2 | L | 6 |
| PCB 체결 |  | 1 |  |  | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 4 |

### 공정 270 — Module 공정 / 열융착

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| 열융착 Machine | 조립 불가 | 7 | 탈거력 이탈 | 온도 설정 미흡 | 작업 온도 표준 설정 실시 | 3 | 탈거력 측정 | 2 | L | 42 |
| 열융착 Machine |  | 7 |  | SPEC 설정 미흡 | 작업표준 설정 및 Data Matrix 검증 | 3 | Master SPL(OK/NG)점검 | 2 | L | 42 |
| 열융착 Machine | 제품 파손 | 8 | 제품 파손 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 32 |
| 열융착 Machine | 조립 불가 | 7 | 상대물 미조립 | 설비 설정 미흡 | 설비 설정 관리 | 3 | 융착부 전수 검사 | 2 | L | 42 |

### 공정 260 — Module 공정 / FLUX 도포

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| FLUX Machine | 기능 미/오작동 | 2 | Nozzle 막힘 | 설비 관리 미흡 | 노즐 교체 | 2 | 노즐교체/일 | 2 | L | 8 |
| FLUX Machine |  | 2 | 미도포 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 8 |
| FLUX Machine |  | 3 |  |  | 도포 유무 확인 센서 확인 | 2 | 미도포시 설비 알람발생 | 1 | L | 6 |

### 공정 280 — Module 공정 / Soldering

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Robot Soldering Machine | 기능 미/오작동 | 7 | 미납/소납 | 인두팁 교체주기 관리 미흡 | 50,000회 교체 | 3 | 인두팁 사용 횟수 설비 인터락 | 2 | L | 42 |
| Robot Soldering Machine |  | 7 |  | 인두팁 청결 관리 미흡 | 자동 세척 실시 | 2 | 인두팁 자동 세척 설정 | 2 | L | 28 |
| Robot Soldering Machine |  | 7 |  | 인두팁 온도체크 관리 미흡 | 인두팁 온도 체크 실시 | 3 | 온도 측정기로 온도 측정 | 2 | L | 42 |
| Robot Soldering Machine |  | 5 |  | 설비 관리 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 20 |
| Robot Soldering Machine |  | 5 | 납볼 | 마스킹 청결 관리 미흡 | 마스킹 세척 실시 | 2 | 주기적 마스킹 세척 | 2 | L | 20 |

### 공정 300 — Module 공정 / Soldering Vison

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Vison Machine | 기능 미/오작동 | 2 | 미검출 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 8 |
| Vison Machine |  | 7 | 미납/소납 | 설비 설정 미흡 | 작업표준 설정 및 Data Matrix 검증 | 3 | Master SPL(OK/NG)점검 | 2 | L | 42 |

### 공정 310 — Module 공정 / Coating

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Coating Machine | 제품 미/오작동 | 6 | Coating 두께관리 | 장비 설정 미흡 | 도막두께 측정/일 | 3 | 도막두께 측정 시트 | 2 | L | 36 |
| Coating Machine |  | 6 |  |  | 디스펜서 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 24 |
| Coating Machine |  | 6 | Coating 기포 관리 | 장비 설정 미흡 | 코팅액 탱크 관리 설정 | 3 | 설비 일상점검 관리 | 3 | L | 54 |
| Coating Machine |  | 7 | Nozzle 막힘 | 일상 점검 관리 미흡 | 세척액 관리 | 3 | 설비 일상 점검 관리 | 2 | L | 42 |

### 공정 320 — Module 공정 / 다운로드+EOL

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| EOL Machine | 기능 미/오동작 | 7 | 미검출 | SPEC 설정 오류 | 작업표준 설정 및 Data Matrix 검증 | 1 | Master SPL(OK/NG)점검 | 4 | L | 28 |
| EOL Machine |  | 7 | Test Pin 가성불량 | Test Pin 관리 미흡 | Test Pin 수명 관리 진행. | 3 | MES Interlock Pin Count : 50,000 회 | 1 | L | 21 |
| EOL Machine |  | 7 | 제품 파손 | 설비 설정 미흡 | 컨베이어 속도 관리 설정 | 2 | 설비 일상점검 관리 | 2 | L | 28 |
| EOL Machine |  | 7 | 상대물 미조립 | 커넥터 터미널 검사 미흡 | 외관 검사 진행 | 2 | 외관 검사 진행 | 4 | L | 56 |

### 공정 340 — Module 공정 / 외관검사+포장

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Operator | 수율 하락 | 7 | 제품 파손 | 작업자 취급 부주의 | 작업표준 설정 | 3 | 육안검사 | 4 | L | 84 |
| Operator | 고객 VOC | 8 | 혼입 포장 | 작업자 취급 부주의 | 작업표준 설정 | 3 | MES Interlock | 1 | L | 24 |

### 공정 350 — GP-12 / GP-12

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Operator | 제품 조립 시 형합성 및 작동 불량 | 7 | 외관풀량 | 작업자 취급 부주의 | 작업표준 설정 | 3 | 육안검사 | 4 | L | 84 |

### 공정 360 — 출하검사 / 출하검사

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| Measuring device | 제품 조립 시 형합성 및 작동 불량 | 7 | 치수불량 | 계측기 오류 | 계측기 MSA 실시 | 1 | MSA 점검 check | 4 | L | 28 |
| Operator |  | 7 |  | 검사 기준 상이 | 작업자 MSA | 1 | 검사자 인증 | 4 | L | 28 |

### 공정 380 — 완제품창고 / 포장/완제품창고

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| 완제품 포장 | 불량제품 Lot 구성 불가 | 8 | 혼입포장 | 작업자 부주의 | MES 포장 설정한 제품과 상이한 제품과 불량 등록된 제품 Scan시 Box 구성 안됨 | 2 | MES Interlock | 1 | L | 16 |

### 공정 390 — 출하관리 / 출하관리

| WorkElement | FE(고장영향) | S | FM(고장형태) | FC(고장원인) | PC(예방관리) | O | DC(검출관리) | D | AP | RPN |
|---|---|---|---|---|---|---|---|---|---|---|
| 완제품 출하 | 선입선출 미준수 | 3 | 선입선출 미준수 | 작업자 부주의 | 먼저 포장된 Box 순서로 출하요청 가능 | 2 | MES Interlock | 1 | L | 6 |

## 5. 리스크 우선 검토 항목 (RPN 상위)

> 본 PFMEA의 AP(Action Priority) 등급은 AIAG-VDA 기준(S·O·D 조합 매트릭스)에 따라 전체 항목이 **L(낮음)**으로 산출되어 있습니다.
> 다만 RPN(S×O×D) 수치가 상대적으로 높은 항목은 관리 상태를 주기적으로 재확인할 가치가 있어 별도로 정리합니다.

| 공정 | Item/Step | FM(고장형태) | S | O | D | RPN | AP |
|------|-----------|-------------|---|---|---|-----|-----|
| 150 | PCB 적재/UNLOADER | 부품 파손 | 8 | 3 | 4 | 96 | L |
| 340 | Module 공정/외관검사+포장 | 제품 파손 | 7 | 3 | 4 | 84 | L |
| 350 | GP-12/GP-12 | 외관풀량 | 7 | 3 | 4 | 84 | L |
| 120 | 솔더 용융/REFLOW | 냉납 | 8 | 2 | 4 | 64 | L |
| 130 | 부품 검사/AOI | 미검출 | 7 | 2 | 4 | 56 | L |
| 320 | Module 공정/다운로드+EOL | 상대물 미조립 | 7 | 2 | 4 | 56 | L |
| 110 | 부품 실장/MOUNTER | 역삽 | 9 | 3 | 2 | 54 | L |
| 190 | Module 공정/Coating | Coating 기포 관리 | 6 | 3 | 3 | 54 | L |
| 310 | Module 공정/Coating | Coating 기포 관리 | 6 | 3 | 3 | 54 | L |

## 6. 요약 통계

- 총 공정 수: 31개
- 총 고장모드 항목 수: 85건
- RPN 50 이상 항목: 9건
- AP 등급 분포: 전체 L(낮음) — 별도 조치 우선순위 상승 항목 없음 (Rev.3 기준)

---

*본 문서는 원본 xlsx의 구조·수치를 그대로 재구성한 정리본이며, 원본 파일의 서식/코멘트/조건부서식 등은 포함하지 않습니다. 상세 수정이력 및 관리계획서 연동 내용은 원본 파일을 참조하세요.*