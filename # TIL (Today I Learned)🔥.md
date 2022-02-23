# TIL (Today I Learned)🔥

2022-02-08


## Git 의 영역

 Working directory 

- ↓↓↓↓ git add .

Staging area (Index) // 작업트리와 저장소 사이에있는 가상의 준비영역

- ↓↓↓↓ git commit -m "메세지"

Local repository

- ↓↓↓↓ git push {저장소} {브랜치}

Remote repository (github)



## Git 명령어

```markdown
git init // 저장소 생성
git clone {복사한Url} 
git add {} //원하는 것만 staging area에 올림
git add .  //다올림
git reset  // 스테이지 올라간 파일 취소
git commit -m "메세지"  //  로컬저장소에 저장
git log      //커밋 이력조회 
git branch {이름} // 브랜치 만들기
git branch  // 브랜치 확인
git checkout -t origin/{가져올 branch} 
//작업할 브랜치를 원격저장소에서 추적
git switch {이름} // 브랜치 이동
git merge {합칠 브랜치이름} // 현재 브랜치에 다른 브랜치 병합
git status // 파일 상태 확인
git remote // 저장소명 알려줌
git push {저장소명} {브랜치명} //  원격 저장소에 올림
git push -u {저장소명} {브랜치명} // -u 붙이면 다음에 인자생략가능
```

### git status  


	빨강이면 스테이지 올라가지않은상태  -> add 해야함
		        
		
	초록이면 스테이지 올라감 -> commit 가능


포크 ->클론 -> 브랜치추적 -> 애드커밋푸시 -> PR
