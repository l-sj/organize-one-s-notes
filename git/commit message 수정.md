[출처](http://celdee.tistory.com/808)

# git commit --amend
바로 이전의 커밋 메세지만 수정.


| 명령어 | - |
| :--------- | :--------- |
| git commit --amend | 바로 이전의 커밋 <br>메세지만 수정.<br>메세지 수정화면으로 넘어가면,<br> `i` 키를 눌러야 편집 가능.<br> 수정 끝내고 나서 `esc`키 누른 후, `:wq` 입력(수정내용 저장후 수정화면에서 나간다는 명령어)<br> 수정내용 저장안하고 나갈려면 `:q` 명령어 입력 |


# N 번째 커밋내용 수정
N개의 커밋 메세지를 불러와서 선택적으로 수정할 수 있음.


| 명령어 | - |
| :--------- | :--------- |
| git rebase -i HEAD~N |  rebase 명령을 사용하여 수정하고자 하는 커밋을 선택.<br> head에서부터 몇 번째 커밋인지에 따라 N에 적절한 숫자를 입력 |

예) 바로 이전 커밋부터 3번째 까지 커밋내용을 불러와서 2번째 커밋 내용을 수정하고 저장.

1. git log 명령을 사용하여 어느 커밋을 수정할지 확인.<br>
> `git log`

2. 3번째 까지의 커밋내용을 불러온다.<br>
> `git rebase -i HEAD~3`

3. 텍스트 에디터에 해당 커밋 목록이 다음 형식으로 출력된다.<br>
```
pick d02a9caw1 commit message 1
pick ca00982bc commit message 2
pick c1892ab2e commit message 3
```
| 예) 첫번째 커밋 | 컬럼 설명 |
| :--------- | :--------- |
| pick | 첫 컬럼은 커밋을 어떻게 처리할지 나타내는 명령.  |
| d02a9caw1 |  두번째는 커밋의 해시. |
| message 1 |  마지막 컬럼은 커밋 메세지. |


4. 수정하고자 하는 커밋의 pick 명령을 reword 명령으로 수정.<br>
> `i` 키를 눌러야 편집 가능.
```
pick d02a9caw1 commit message 1
reword ca00982bc commit message 2. 커밋내용 수정
pick c1892ab2e commit message 3
```

5. 커밋 목록을 저장한 뒤 텍스트 에디터를 종료.<br>
> `esc`키 누른 후, `:wq` 입력

