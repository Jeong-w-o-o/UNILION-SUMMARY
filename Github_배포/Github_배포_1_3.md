# Github 사용법 및 협업 
## Github & 배포 3강

1. 자주 쓰는 명령어

git 저장소 초기화 -> 비어있는 local 저장소 생성
```phyton
git init
```
폴더에 변경된 모든 파일 staging area에 올리기
```phyton
git add .
```
유사시 돌아갈 수 있는 저장소의 체크 포인트 생성
```phyton
git commit -m "설명"
```
원격 저장소에 연결
```phyton
git remote add origin 원격저장소 주소
```
새로운 브랜치 생성 (브랜치: 용도에 따라 저장소 나누는 것)
```phyton
git branch 브랜치명
```
해당 브랜치로 이동
```phyton
git chechout 브랜치명
```
원격 저장소의 특정 브랜치에 프로젝트 저장
```phyton
git push origin 브랜치
```
원격 저장소의 특정 브랜치에서 변경사항 pull
```phyton
git pull origin 브랜치
```
원격 저장소에 있는 파일 전체 복사
```phyton
git clone 원격저장소 주소
```
git 저장소의 상태 확인
```phyton
git status
```
2. Github 이용한 협업

  2.1 협업자일 경우

  (1) repository 생성
  
  (2) Manage access에서 팀원 추가
  
  (3) 초기 프로젝트 push : 코드 있는 파일에서 git init -> 원격 저장소 연결 git remote add origin 레퍼지토리 url -> commit 전에 항상 add . -> commit -> push origin 
  
  (4) 팀원들의 로컬에 프로젝트 pull : 각자 로컬에 프로젝트 pull -> pull or clone 사용 
  
  (5) 팀원 각자의 브랜치를 생성하여 작업 : git branch 브랜치명 -> git checkout 브랜치명 (브랜치로 이동) -> 코드 생성 & 수정 -> git add . -> commit -> push 브랜치명 (origin 아님)
  
  (6) 브랜치에 작업한 내용 push : git push
  
  (7) Master와 merge하기 전 pull request : "고쳤는데 봐 주세요" pull request에서 브랜치끼리의 차이 볼 수 있음
  
  (8) Pull request 확인 후 Maste와 merge
  
  2.2 협업자 아닐 경우
  
  (1) 작업하고 싶은 레퍼지토리 fork : 오른쪽 위 fork 버튼
  
  (2) 자신의 로컬에서 작업 : url 복사해서 url 저장할 폴더 생성 -> git clone url -> ls 통해 확인 -> 내용 수정 후 저장 -> git add . -> git commit -m "~~"
  
  (3) 변경사항을 자신의 브랜치에 push : git checkout -b 브랜치명 (브랜치 생성 후 바로 체크아웃) -> git push origin 브랜치명
  
  (4) 원본 레퍼지토리 소유자에게 변경사항 request : 앞선 pull request와 동일
  
  (5) 소유자가 pull request 승인 후 merge하면 자동으로 협업자로 추가됨
  
  
