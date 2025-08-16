### 사용한 데이터 셋

원본 데이터: wildfire_2019_2023_combine.csv

전처리 과정
(1) 무관 및 내생성 있는 컬럼 제거
(2) LFDAU_GRNDS_DSTNC 컬럼: 0값 결측치로 변환 + missing labeling
(3) 범주형 데이터 레이블 인코딩
(4) HR_UNIT_WSPD_INFO 컬럼: 풍속 평균으로 레이블 인코딩
(5) 파생변수 생성
- 시각 관련 컬럼: datetime 변환 (파생변수 생성을 위해)
- golden_time_under_50min / arrival_time_diff / is_night / month_rcpt / dispatch_time_diff
- 시각 관련 컬럼 삭제

추가 전처리
(6) LOG 변환 + 변환한 원래 변수 삭제
FIRE_SUPESN_HR",        # 타겟 변수
"DSPT_REQ_HR",          # 출동 요청 시간
"FRSTN_GRNDS_DSTNC",    # 산림지역 거리
"CNTR_GRNDS_DSTNC",     # 중심지역 거리
"LFDAU_GRNDS_DSTNC",    # 인접지역 거리
"arrival_time_diff",     # 도착 시간 차이
"dispatch_time_diff"     # 출동 시간 차이

