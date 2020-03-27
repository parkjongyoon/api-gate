ZUUL + RIBBON + EUREKA 테스트 소스
===========================================================

아래 프로젝트를 모두 받고 모두 기동한다.
	api-gate
	eureka-server
	service-a
	service-a2
	service-b

기동 후 아래 주소를 실행하면 고객정보를 가져온다. 그래고 log를 통해서 로드발라스 되는 것을 확인할 수 있다.
	http://localhost:8801/users/getUserInfo

실행 설명
	api-gate를 통해 eureka-server에 등록된 service를 검색한다.
	우선 service-b를 실행시키면 service-b는 feign client를 이용하여 servie-a를 호출하여 username을 가져온다.