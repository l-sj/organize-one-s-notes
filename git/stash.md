[출처](http://www.popit.kr/git-stash/)

# git stash
임시저장
`스테이지`에 올라가지 않은 수정, 삭제된 파일들을 **임시저장**. 추가된 파일은 관리 대상 아님.

_**[] 대괄호**는 구분짓기 위한것으로 의미없음. 명령어 입력시 입력하지 않음._


| 명령어 | - | - |
| :--------- | :--------- | :--------- |
| git stash list | 목록보기(LIST) | stash에 저장된 목록 확인. stash@{숫자} 형식으로 보여지며, 가장 최근에 stash된것이 0번. 0번이 최신이고 1,2 .. 순서로 밀려서 저장. |
| git stash save [메시지] | 저장하기 (SAVE) | stash에 메시지를 지정할때는 save를 명시함. |
| git stash | 저장하기 | save 옵션이 생략된 축약형 |
| git stash pop [stash@{숫자}]| 불러오고 삭제하기(POP) | apply와 drop을 한번에 수행. 지정된 stash@{숫자}를 불러오고 삭제. |
| git stash pop |  | stash@{숫자}를 지정하지 않으면 가장 최신의( stash@{0} )를 삭제. |
| git stash apply [stash@{숫자}] | 불러오기(APPLY) | 지정된 stash를 불러온다. stash@{숫자}를 지정하지 않으면 가장 최신의( stash@{0} ) 을 불러옴 |
| git stash drop [stash@{숫자}] | 삭제하기(DROP) | 지정된 stash를 삭제. stash@{숫자}를 지정하지 않으면 가장 최신의( stash@{0} )를 삭제. |
| git stash show [stash@{숫자}] | 내용 보기(SHOW) | stash 된 내용을 확인. stash@{숫자}를 지정하지 않으면 가장 최신의( stash@{0} )를 보여준다.|
| git stash git stash branch <새로만들브랜치이름> [stash@{숫자}] | 브랜치로 만들기(BRANCH) | stash 된 내용으로 새로운 브랜치를 만든다. pop과 마찬가지로 stash 된 내용은 삭제된다. |
