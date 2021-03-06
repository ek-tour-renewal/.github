# ek-tour-renewal project
[EK 하나버스관광 홈페이지 리뉴얼 프로젝트] <br>
오래되고 유지보수 어려운 기술로 기존 제작 되었던 관광버스 예약 견적을 요청하고 이를 처리할 수 있는 서버 재구축 <br>
불필요한 기존 기능들 (게시판, 공지사항 등)을 제외하고 기존 기능들을 보완/강화 (견적요청시 알람-이메일 기능) 하여 홈페이지를 리뉴얼 함 <br>

기존 서비스의 문제점
- ASP, MSSql의 윈도우 기반 통합 서버 (프론트, 백 분리가 되어있지 않음)
- 확장성과 유지보수성이 낮은 기능 실현의 최우선 목적의 코드 설계
- 구식 호스팅 서비스를 통한 잦은 서버 장애 발생 및 과도한 유지비용 발생

[old version (now servicing)](http://www.ekhanabus.com/) <br>
[renewal version (now developing)](http:/52.79.242.242)

# ek-tour-client
## 기술스택
```react```, ```Material UI```

## 기능


# ek-tour-server
## 기술스택
```Spring boot```, ```Thymeleaf```, ```Spring Data JPA```, ```MySQL```, ```AWS RDS```, ```AWS EC2```

## 기능
### 1. 리액트 클라이언트 REST API 형식으로 데이터 제공
- 견적요청 생성 및 저장
- 견적요청 저장시 지정된 이메일로 알림 이메일 발송
- 견적요청 삭제 (데이터는 남아있고, 안 보이도록 처리)
- 견적요청 조회 (상세조회, 목록 조회(페이징))

### 2. 관리자 페이지 (SSR)
- 관리자 로그인 (세션 기반)
- 홈페이지 회사 정보 수정 및 관리자 정보 수정(관리자 비밀번호 변경, 로고 변경, 회사 정보 변경)
- 견적요청 관리 (삭제 처리)
- 견적요청 엑셀 형식 변환 및 저장
- 견적요청 검색 (날짜, 요청자, 연락처, 키워드)
- 예외, 오류 페이지 처리 (4xx, 500)
