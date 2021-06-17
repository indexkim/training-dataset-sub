# Training_Dataset


## 학습데이터 구축 공정

- 수집 2. 정제 3. 가공 4. 검수 5. 학습의 5단계로 구성되어 있습니다.

1. 수집: 원시데이터 수집(이미지)
2. 정제: 원시데이터의 파일명 변환, 이미지 해상도 조정, 흔들린 사진 폐기, 개인정보 비식별화를 통해 원천데이터 획득
3. 가공: 원천데이터(jpg) + 어노테이션 데이터(Json) = 데이터셋
4. 검수: 데이터셋 검수 후 통과한 데이터셋을 학습 단계로 이관
5. 학습: 검수를 통과한 데이터셋 학습

## 일일 가공 공정 세부 업무

1. 가공 전 입고된 원천데이터 적합성 검증
2. 입고된 원천데이터 DB화, 창고로 이동, 창고의 원천데이터 물량 현행화
3. 작업자 고용 현황, 사업 일정, 공정단계별 종별 잔여 물량 체크 후 작업물 분배. 물량 부족 시 report
4. 분배 내역 DB화
5. 완료된 작업물 확인: 공정 내 Performance management 측면의 검수 - 분배된 작업량을 전부 업로드했는지 체크 - Bot
6. Quality management 측면의 1차 검수 : data analysis 데이터 분석
7. Quality management 측면의 1차 검수 : data ETL - 1차검수를 통과한 데이터셋 추출 > 검수 서버 구조에 맞게 변환 > 데이터 적재(이관) > 이관 목록 생성
8. 검수 결과 분석 및 재작업 대상자 피드백 - Bot

## 일일 업무 외 

1. 요청사항에 맞는 데이터 추출, 전처리, 분석
2. 파일 자동 생성 및 이메일 전송
3. Ground Truth 검증을 위한 viewer 개발
4. 어노테이션 데이터 일괄 변경
