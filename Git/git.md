# git 사용법 

    git init 

    git add .      -.은 전체를 표시 

    git commit -m "first commit"((이름 아무거나)) 깃 타임캡슐 생성

    git remote add origin (git repositories 주소를 입력) 주소와 연결

    git push origin master(branch)  이제 깃허브에 커밋된걸 올린다



### 깃 프로젝트 가져올 경우(신입) 

    cmd 에서
    git clone (git repositories 주소를 입력) (새로 만들 폴더이름)
        
    ->신입 수정 후 
    git add .

    git comit -m "freshM commit"

    git checkout -b freshM  신입을 위한 공간(branch) 새로 생성

    git push origin freshM

### 편집 중간에 커밋이 되었을 경우

    git add . 

    git commit -m "second commit"  일단 작성중인걸 저장하고

    git pull origin master 마스터에 커밋된걸 가져온다 

    ---
    git log  만든 타임캡슐에 정보들을 나열해줌      ((안빠져나가질때 :q로 나가자))

### 과거로 돌아는 법 
 
    git reset (일련번호6자{log로 나온 일련번호}) --hard     ///hard 모든 작업 상태 내 변경 사항을 버림 (다시 미래로 갈 수 없다 )

    미래한발걸치고 과거 가는법  ((일련번호를 돌아갈 시점이 아닌 취소할 시점))

    git revert (일련번호6자)  그 전 단계에 있던걸 새캡슐로 묶어냄 
    --> 그럼 리셋으로 다시 돌아갈 수 있다 

### 다음은 새 브란치 만드는 것 

    git branch my-idea 새로운 브란치 생성

    git checkout my-idea 만들어놓은 다른 브란치로 이동 

### 브란치 내용 통과! 합치기 
master 로 이동해서 
git merge my-another(my-idea에서 파생된)   ?? 그럼 my-idea 에서 변경된 내용도 옮겨지는건가 

rebase
이런 브란치들이 엄청 지저분할때 한줄로 정리  (이건 심화 나중에 배우기)
git rebase my-another


git branch -D my-idea  다쓴 브란치 삭제 


git fetch  깃허브에서의 소식받아오기 
git status  커밋이 올라온게 있나 확인가능


git branch 로컬에 브랜치 조회와 현재 브랜치 확인   
git branch -a 로컬과 원격(깃허브) 모두 조회가능 


--충돌방지
동시에 같은부분 커밋시 후에 커밋시도하면 에러 

원격의 브랜치 지울땐 
git push -d origin 브랜치명 
