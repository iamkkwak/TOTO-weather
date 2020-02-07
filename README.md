# WEB PROJECT

- **Who?** SSAFY 3기 임베디드 16반 곽은정 & 이현민
- **When?** 2020.02.07 ~
- **What?** 날씨 및 달력 등을 포함한 웹 페이지 제작하기
- **How?** HTML, CSS, JavaScript, Vue.js, MongoDB 등을 이용

<br>

## Index

- [Day 1](#day-1-20200207)

<br>

### Day 1: 2020.02.07

1. git 관련 환경설정 구축

   > 자리가 바뀌었기 때문에 서버 저장소와 로컬 저장소를 연동하기 위해서는 환경설정도 다시 해야했다. `제어판` - `자격 증명 관리자` - `Windows 자격 증명`에서 git 관련 저장된 계정 등을 삭제한다.

   - git user 바꾸기

     ```
     $ git config user.name "$(USERNAME)"
     $ git config user.email "$(USEREMAIL)"
     ```

   - 새로운 ssh-key 받기

     ```
     $ ssh-keygen
     $ cat ~/.ssh/id_rsa.pub
     ```

     이 때, 나오는 항목에서 overwrite 하겠냐는 항목에 엔터를 누르면 키 생성이 안 된다 :cry: 이것 때문에 애를 먹었는데, 반드시 `y`를 치고 넘어갈 것! `$ cat ~/.ssh/id_rsa.pub` 를 통해 나오는 ssh-key를 git에 등록해주면 된다.

   - 서버 저장소와 로컬 저장소를 연동하기

     ```
     $ cd $(USERDIRECTORY)
     $ git init
     $ git clone $(GITURL)
     ```

     `GITURL`에는 내가 연동하고 싶은 저장소의 **HTTP 주소**를 적어주면 된다. 잘 모르고 SSH 주소로 시도하다 안 돼서 멘붕이 왔었다 .... :scream: 

   - 커밋과 푸시하기

     ```
     $ git add $(YOURFILE)
     $ git commit -m "COMMIT MESSAGE"
     $ git push -u origin master
     ```

     그럼 이제 git 로그인 창이 뜰 텐데, 그 때 로그인을 해주면 연동 완료!
     
     

2. 레이아웃 구성하기
