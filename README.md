VS code

markdown 왜 배울까 ? - github에 프로젝트 올릴 때, [readme.md](http://readme.md) 파일에 활용

- ctrl + b = 사이드바
- ctrl + ` (물결키) = 터미널
- touch ~~ = new file
- ctrl + , = setting
- 코드블럭 ``` - 코드블럭 설정에 따라 색이 달라서 가독성의 차이를 보임. ex 파이썬 , c, 자바 등
- 기준은 gpt같은 것이 아니라, 공식문서 및 가이드문서 ~ markdownguide.org

- interface = 리모컨과 같은 것
- GUI graphic user interface
- CLI command line interface (텍스트 같은 거)

- window os의 interface
- GUI = window shell
- CLI = power shell, cmd(명령프롬프트)

- Linux os의 interface
- GUI = GNOME
- CLI = bash
- bash의 장점 = 편함 ~ tab 누르면 자동완성 가능

- git을 다룰 때 interface
- GUI = “github desktop”, “소스트리”
- CLI : git bash (엄청 많이 쓸 예정)

- GUI 장점 : 보기 편함, 친숙함 / 복잡한 분석(그래프 같은 거) 보기 좋다
- CLI 장점 : 빠름(commit 명령어 빠름) / 미래에도 계속 쓸 예정(변함없다)
- 결론은 둘 다 써야하지만 대부분은 CLI를 쓸 예정

- IDE(통합개발환경)
- VS code는 IDE가 아님 text editor임
- text editor : 익스텐션을 추가해서 마치 IDE처럼 사용
- 파이썬의 IDE는 파이참, 쥬피터노트북
- C의 IDE는 visual studio
- Java의 IDE는 intelliJ

- minimal gnu for windows : 윈도우환경에서 리눅스에 쓰이는 툴들을 쓸 수 있게 가볍게 만든 프로젝트
- 리눅스는 항상 home 디렉토리 = “~”
- cd ~ : 홈 디렉토리
- cd - : 뒤로가기
- cd.. : 상위 디렉토리

- touch 파일생성
- mkdir : 폴더(디렉토리) 생성
- start : 파일열기
- rm : 삭제

- 절대경로 : ~/desktop/practice
- 상대경로 : ./practice2       ../practice/practice3

- working directory → staging area = git add
- staging area → repository = git commit
- git → github 업로드 시 push, 다운로드 시 pull
- 변경사항이 아무 것도 없으면 add 해도 반응 x
- ctrl + c = 취소하기
- git status는 staging area, git log는 repository

===============================================

리눅스는 항상 HOME 디렉토리 : ~
cd ~ : 홈 디렉토리
cd - : 뒤로가기
cd .. : 상위 디렉토리

touch : 파일 생성
mkdir : 폴더(디렉토리) 생성
start : 파일 열기
rm : 삭제
cp : 복사

절대 경로 : ~/Desktop/practice
상대 경로 : ./practice2
../practice/practice3

===============================================

git : 분산 버전 관리 시스템

git init : git 시작
rm -rf .git : git 삭제(git 종료)

git config --global [user.name](http://user.name/) "이름"
git config --global user.email "이메일"

git push 이후 자리 옮겼을 때 제어판의 windows 자격 증명
-> 일반 자격 증명 에서 github 삭제하기

git add . : staging area 에 올리기
git status : staging area 작업 파일 확인

git commit -m "메시지명" : repository에 올리기
git log : repository 작업 파일 확인(커밋 되어 있는지 확인)

================================================

markdown 왜 배울까?
: github에 프로젝트 올릴때 [README.md](http://readme.md/) 파일에 활용

================================================

vscode 단축키

ctrl + b : 사이드바
ctrl + ` : 터미널 열기/닫기
ctrl + , : setting 열기
ctrl + s : 저장ㅊ

## **01/16**

git remote : git과 github 연결 ~~ git remote add origin url

gir remote -v

붙여넣기 : shift + insert

clone과 pull의 차이

새로운 환경에서 처음 다운로드 받으려함 ⇒ clone ~ git clone url

push나 clone을 진행한 후에 다운로드 하려함⇒ pull 

vs에서 git ignore하면 git에 나타나지 않음

push까지 한 후, vs code 같은 곳에서의 변경사항이 있지 않으면 add 자체가 안됨.

remote를 다른 url에 하고 다른 작업은 가능하다.

만약 같은 repository에 다른 딕셔너리를 추가하고 싶으면 창을 닫고 새로운 git bash를 열어야함.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/134d674b-f64a-43c0-8d47-7c17d9f371b1/10eeedd9-8474-4b7b-8220-7f4e1920b1b7/image.png)

amend는 수정 ~~ git commit 완료 후 git commit —amend입력

그럼 vim이 뜸 맨 위에서 멘트 수정하고 

esc → :wq = 저장 후 종료 ~~ 잘 안되면 wq! 해보삼

esc → :q! = 저장 안하고 종료

느낌표는 약간 강제의 의미를 가지고 있음

commit을 새로 하지 않고 전체 수정하기

git add → git commit —amend 

위와 차이는 commit이 되었나 안되었나 차이

git revert : 특정 commit을 없었던 일로 만들기 

git log —oneline 해시값 확인

git revert — 해시값 하면 댐

git reset : 특정 commit으로 되돌려버리기 ~ 모르고 revert한 것 복구 가능

git reset —hard 해시값

git reflog : 이전 과거 commit 기록을 모두 볼 수 있다.

git add 취소하기 (staging area에서의 작업을 working directory로 옮기는 것)

1. commit이 없는 경우 : git rm —cached 파일명
2. 이전에 했던 commit이 있는 경우 :  git restore —staged 파일명
