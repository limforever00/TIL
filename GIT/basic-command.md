# Basic Command 

## 설정

- 커밋을 남기기 위해 사용자 정보를 입력하는 명령어
- 초기에 한번 작성
- 변경되었을 경우 다시 입력하면 덮어쓰기 됨

```
git congig --golbal user.email 
git config --global user.name
```

## 명령어

git init -> 현재 폴더를 repository지정 (관리를 시작)
이후
ls - a
.git 확인 가능

rm -rf .git reposiroty 해제

git log --oneline 히스토리 목록과 코드 확인

git checkout (코드) 해당 시점으로 이동

git checkout master 다시 돌아오기

- commit 목록에 추가하기 위해 파일을 추가해주는 커맨드
```
git add (파일명)
git add . | git add * : 수정된 파일 전체 add
```

원격 저장소 확인
$ git remote -v

원격 저장소 추가
$ git remote add origin 링크

$ git remote -v
origin  https://github.com/limforever00/test_project.git (fetch)
origin  https://github.com/limforever00/test_project.git (push)

origin : 원격 저장소명

$ git push -u origin master 
master branch를 원격저장소에 추가(브랜치별로 추가)

git 홈페이지에서 파일 만든후  ->
pull을 사용해서 업데이트
$git pull origin master


git에서 내컴퓨터로 con
git remote add origin https://github.com/limforever00/limforever00.github.io

다음은 브랜치에서 master 브랜치로 변경사항을 병합하는 일반적인 절차입니다:

현재 작업 중인 브랜치에서 변경사항을 커밋합니다:

git add .
git commit -m "변경 사항 설명"
master 브랜치로 이동합니다:

git checkout master
master 브랜치를 업데이트합니다:

bash
Copy code
git pull origin master
이제 다른 브랜치에서 작업한 변경 사항을 master 브랜치로 병합합니다:

bash
Copy code
git merge 브랜치_이름
여기서 브랜치_이름은 다른 브랜치의 이름입니다.

병합이 완료되고 충돌이 없다면, 변경 사항을 원격 저장소로 푸시합니다:

bash
Copy code
git push origin master
이제 변경 사항이 master 브랜치로 푸시되었고, 원격 저장소와 로컬 저장소의 master 브랜치는 동일한 상태가 됩니다. 
이런 방식으로 변경사항을 병합하고 푸시하면 협업 과정에서 코드 충돌을 방지하고 정확한 변경사항을 원격 저장소로 업로드할 수 있습니다.

------------------------------------------------------------
다른 사람이 올린 branch 가져와서 master에 적용하기까지 단계별 정리

1. 원격 브랜치 목록 확인
git fetch origin 위 명령어로 원격저장소 origin의 브랜치 정보를 가져옴

2. git branch -r
가져온 branch 목록 확인

3. 다른 사람이 푸시한 원격 브랜치를 로컬로 체크아웃
git checkout -b 로컬_브랜치_이름 origin/<원격 브랜치 이름>

여기서 작업후 이상이 없음을 확인하면 master branch로 merge작업 진행

4. 이상없음 확인후 add && commit 진행

5. master로 이동
   git checkout master

6. master 브랜치 업데이트
   git pull origin master

7. 다른 브랜치에서 작업한 사항을 mater로 병합
   git merge 브랜치명

8. 병합 완료후 정상작동 확인하고 원격저장소로 push
   git push origin master
