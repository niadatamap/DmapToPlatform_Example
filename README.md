## 빅데이터 개방‧유통을 위한 메타데이터 구조 및 데이터 연계 규격 예시

## 개요 
- 메타데이터 조회 API 예제 

## 파일설명
1. DCAT예제샘플.xml
  - 빅데이터 플랫폼에서 통합데이터지도로 전송하기 위해 변환하는 RDF형태의 XML 예제 파일

2. 메타데이터조회샘플.json
  - 통합데이터지도에서 메타데이터 리스트정보를 수집하기 API 형태의 list.json 파일

3. 메타데이터상세조회샘플.json
  - 통합데이터지도에서 메타데이터 상세정보를 수집하기 API 형태의 detail.json 파일

4. 통합데이터지도_메타데이터연계_API_v1.3.xlsx
  - 빅데이터 플랫폼에서 통합데이터 지도로 연계를 위한 API 상세 명세서

## 검색을 위한 통합데이터 지도에서 빅데이터 플랫폼으로 연계를 위한 테스트 절차
- 방화벽상 데이터 요청 아이피 등록(NIA 담당자)

- 사전 빅데이터 플랫폼 ID 등록 요청(NIA 담당자)

- API 요청 테스트(통합데이터 지도 운영 담당자)
  - 메타데이터 목록 조회 (platformId 값을 입력시 해당 플랫폼의 메타데이터가 제외된 조회)
  
      $ curl -X GET \
        http://115.85.181.22:8080/api/resources/list?title=고속&platformIds=1
        
  - 메타데이터 상세내용 조회 (id 속성값 기준으로 상세내용 조회)
    
      $ curl -X GET \
        http://115.85.181.22:8080/api/resources/5388/detail
    
