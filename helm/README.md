# 기본 명령어 

1. 레포 추가 
~~~ bash 
helm repo add stable https://charts.helm.sh/stable
helm repo add test-repo https://charts.bitnami.com/bitnami
~~~

2. 레포 리스트 보기 
~~~ bash
helm repo list 
~~~

3. 레포에서 검색
~~~bash
helm search repo nginx
~~~

4. repo 최신 버전으로 업데이트
~~~bash
helm repo update
~~~

5. helm에서 파일 다운로드  -압축되어 있음
~~~bash
helm fetch  [repo_name]/[설치이름] --version [Version]
helm fetch test-repo/nginx --version 18.1.2 
옵션 :
--untar : 압축 바로 풀기
~~~

6. 문법 확인 
~~~bash
helm lint . 
~~~

7. helm 내용 찍어보기
~~~bash
helm template .
~~~

8. 배포하기
~~~bash
7. 번에서 나온 결과 값을 yaml 파일로 저장후 실행하면 실패  -> name에 Release로 인한 문구로 실패
helm install  이름 .
helm upgrade --install  이름  .  #kubectl apply 와 같은  변경내용만 실행
~~~

9. 만든 helm 내용 패키지로 만들기
~~~bash
helm package [name]
~~~

10. 테스트 결과보기
~~~bash
helm test [name]
~~~

11. 차트 내용보기
~~~bash
helm show chart .
helm show all .
~~~

12. 상태보기
~~~bash
helm status  [name]
~~~

13. 설치 삭제
~~~bash
helm uninstall [namne] .
~~~




