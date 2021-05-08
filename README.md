## URL: https://github.com/GongMinGi/SoftAssignment2.git

## 기본 환경 설정
- git을 설치한 이후 명령프롬포트를 이용해 기초적인 환경을 설정한다.

![1 git config 기본설정](https://user-images.githubusercontent.com/76468280/117536357-92f1af80-b035-11eb-8232-3c8e11a4aa41.PNG)

- git config 를 사용하여 설정내용을 확인하고 변경할 수 있다.
- 가장 먼저 해야할 것을 사용자 설정으로 깃이 commit 할 때 사용할 사용자의 이름과 메일의 주소이다. --global로 설정하는 건 한번 이면 되며,
만약 프로젝트마다 다른 이름과 주소를 사용하고 싶다면 --global 옵션을 빼고 명령을 실행하면 된다.
- git config --list를 사용하면 설정한 모든것을 한 번에 볼 수 있다.

## 로컬 저장소 생성
- 로컬 저장소를 생성하는 방법에는 2가지가 있다. 첫째로 git init 을 통해 새로 로컬 저장소를 만드는 방법과, git clone <url> 을 통해 github의 데이터를 불러오는 방식이다.


![2 로컬저장소 위치, init](https://user-images.githubusercontent.com/76468280/117526901-06c69480-b003-11eb-89a4-16dddf0765ed.PNG)

![3 clone 생성](https://user-images.githubusercontent.com/76468280/117526924-1e058200-b003-11eb-92dc-44c547ceacbd.PNG)

- 데이터를 불러온다고 말했지만, clone 명령어도 init 명령어도 새로운 저장소 를 만드는 명령어이기 때문에 git init을 사용하고 거기에 git clone을 사용하면 서로다른 2개의 저장소가 만들어진다.
결과는 아래 그림과 같다.

![4 같은 폴더 init clone 동시진행](https://user-images.githubusercontent.com/76468280/117526950-36759c80-b003-11eb-9c77-9f3973eea6d8.PNG)


- 현재 우리는 미리 만들어놓은 원격저장소(깃허브)의 데이터를 수정해야 하므로 git init으로 완전히 새로운 로컬저장소를 만들기보단, git clone을 이용하여
원격저장소를 복사하여 작업할 것이다.

## commit 과 push
- 원격저장소의 내용을 변경하기 위해서는 먼저 로컬 저장소의 데이터를 변경한후, 변경한 파일을 ,add, commit한 후 원격저장소로 push해주어야한다. 아래 사진을 보자

![image](https://user-images.githubusercontent.com/76468280/117527168-f4e5f100-b004-11eb-8d79-5ae0073e3bb4.png)

- 워킹 디렉토리의 모든 파일은 크게 Tracked(관리대상임)와 Untracked(관리대상이 아님)로 나눈다.Tracked 파일은 또 Unmodified(수정하지 않음)와 Modified(수정함) 그리고 Staged(커밋으로 저장소에 기록할) 상태 중 하나이다. 간단히 말하자면 Git이 알고 있는 파일이라는 것이다.
- 마지막 커밋 이후 아직 아무것도 수정하지 않은 상태에서 어떤 파일을 수정하면 Git은 그 파일을 Modified 상태로 인식한다. 실제로 커밋을 하기 위해서는 이 수정한 파일을 Staged 상태로 만들고, Staged 상태의 파일을 커밋한다. 이런 라이프사이클을 계속 반복한다. 아래 예시를 보자.

![5 파일추가_status](https://user-images.githubusercontent.com/76468280/117527614-565b8f00-b008-11eb-98cb-b8f13848b1eb.PNG)

- 로컬저장소에 빈 마크다운 파일을 추가 하고 git status를 통해 상태를 확인해 보면 파일이 untracked 상태라는 것을 알 수 있다. 여기서 git add를 이용해 파일을 추가해보자

![7 add_and_commit](https://user-images.githubusercontent.com/76468280/117527653-9d498480-b008-11eb-80bf-b460853044d7.PNG)

- 다시 git status를 이용해 확인해보면 무사히 파일이 staged 영역에 올라간 것을 볼 수 있다. 여기서 git commit을 이용해 로컬 저장소에 저장, git push를 이용해 원격저장소에 전송해 주면 끝이다.

![8 push](https://user-images.githubusercontent.com/76468280/117527713-ffa28500-b008-11eb-9cf4-427e132fb0d3.PNG)

-지금까지의 활동으로 add는 git이 관리하는 파일을 추가하는 역할, commit은 변경된내용을 저장하는역할, status는 관리중인파일을 상태를 표시해주는 역할, push는 로컬 저장소에 저장된 내용을
원격 저장소에 덮어쓰는 역할을 하는 명령어라는 것을 알 수 있다.

## pull
- 이제 지금까지 원격저장소에서 작성한 README파일을 로컬저장소로 가져올 것이다. 
- 그러기위해서 git pull 명령어를 사용한다.

![9 pull](https://user-images.githubusercontent.com/76468280/117531049-7cd6f580-b01b-11eb-9bb3-e5f3cadad0d3.PNG)

- 이 명령어를 사용하면 원격저장소에 있는 데이터를 로컬 저장소에 똑같이 복사할 수 있다.


## branch, merge, log
- 현재 문서의 상태는 그대로 보존시키고, 따로 작업을 한후 합치고싶다. 그럴 때는 새로운 git branch <name> 을 통해 새로운 브랜치를 만들어 작업하면 됀다.

![10 branch 작성, checkout](https://user-images.githubusercontent.com/76468280/117531181-451c7d80-b01c-11eb-86e5-fa5fc61f6e6c.PNG)

- git branch를 통해 현재 존재하는 브랜치와 현재 작업중인 브랜치를 확인할 수 있고, 위와 같이 git branch support 를 통해 support 라는 이름의 새로운 브랜치를 생성할 수도 있다.
- 새로운 branch를 생성한 후 git checkout 을 이용하면 작업중인 브랜치를 변경하는 것이 가능하다.
- 이제 support 브랜치에서 Markdown 문서를 좀더 작성해 보자.

![11  support 에서 작성, commit push](https://user-images.githubusercontent.com/76468280/117531248-a2b0ca00-b01c-11eb-93e6-615fc78b292e.png)

- 위에서 한 것처럼 똑같이 문서를 수정하고 commit 해주면됀다.
- commit 이후 git log 명령어를 사용하면 commit의 결과를 좀더 가시적으로 볼 수 있다.

![12  log](https://user-images.githubusercontent.com/76468280/117531273-b3f9d680-b01c-11eb-830c-4eccb4378f75.PNG)

- 보다시피 log 명령어는 우리가 지금까지 해온 commit을 보여주는 명령어이다.
- 잘보면 HEAD, 즉 우리가 작업하는 브랜치가 Support를 가리키고 있고, 방금 진행한 커밋이 다른 branch인 main에는 전혀 영향을 끼치지 않는 것을 볼 수 있다.
- 그럼 이제, 작업한 내용은 main branch에 합칠 차례다.

![13 merge](https://user-images.githubusercontent.com/76468280/117531540-d9d3ab00-b01d-11eb-9111-2fd213a47ea9.PNG)

- support branch를 main에 합치기 위해선 우선 checkout 을 이용해 작업브랜치를 main으로 바꾸고 그다음 merge 명령어를 이용해 병합하면된다.

![14  merge 후 log](https://user-images.githubusercontent.com/76468280/117531569-0687c280-b01e-11eb-8991-873c24513369.PNG)

- 이후 log 명령어를 사용하면 main 과 support 두개가 똑같은 commit을 가리키는 것을 볼 수 있다.

## reset
- 이후 몇 번의 commit 이후 심각한 버그가 발생해 그 이전 시점으로 문서를 돌리고 싶다.
- 실수로 일어난 커밋을 수정하거나, 지우고 싶을 때 reset 명령어를 사용할 수 있다. 

![15  reset 전](https://user-images.githubusercontent.com/76468280/117535690-e95cef00-b031-11eb-9507-41da60dfb7ad.PNG)
![16  reset --hard 후](https://user-images.githubusercontent.com/76468280/117535711-0396cd00-b032-11eb-913a-497105193321.PNG)

- 위와 같이 reset --hard 에 특정commit의 해시값을 입력하면 그 다음에 발생한 커밋부터 전부 지워지게 된다. 특히 --hard 명령어를 사용해 지운 commit은 복구할 수 없기 때문에 
주의가 필요하다.

## rebase
- commit 도중 commit 메세지를 잘못 입력하여 이 메세지를 고쳐야한다.
- rebase 명령어를 이용하면 이전에 진행한 커밋을 수정하는 것이 가능하다.

![17 rebase 전](https://user-images.githubusercontent.com/76468280/117535849-a7807880-b032-11eb-89b7-9a97c7aee8ca.PNG)

- 위 그림에서는 Markdown3 이 2개 존재하고 하나는 "까지 붙어 있다. 이를 수정하기 위해 git rebase -i HEAD~3 을 이용하자. HEAD~3은 HEAD로부터 3개의 commit을 수정하겠다는 소리다.

![18 rebase옵션](https://user-images.githubusercontent.com/76468280/117535880-e6163300-b032-11eb-88bb-5834334c994c.PNG)

- 명령어를 입력하면 위와 같은 화면이 뜬다. Commands 아래는 사용할 수 있는 명령어의 개수와 설명이다. 이 중 우리가 원하는것은 commit 메세지를 수정하는 reword다.
이를 pick을 대신해 입력해주면 됀다.

![19 rebase 수정](https://user-images.githubusercontent.com/76468280/117535917-2aa1ce80-b033-11eb-9505-2d521ac3ab73.PNG)

- 그리하여 이런 화면이 떳다면, 맨 위쪽에 쓰고 싶은 메세지를 쓴 뒤 wq!명령어로 저장후 나오면 그대로 commit에 적용된다. 아래는 적용된 모습이다.

![20  rebase 후](https://user-images.githubusercontent.com/76468280/117535941-51f89b80-b033-11eb-98d3-bb3245b7a79d.PNG)

- rebase의 다른 옵션으로 drop이 있는데, 이는 commit 하나를 삭제하여 없었던 것처럼 만드는 명령으로, reset --hard와 달리 1개의 commit을 지정하여 제거할 수 있다.

## remote
- clone으로 불러온 로컬저장소가 원격저장소를 가리키는 이름은 origin으로 설정된다. 이를 원격저장소의 이름과 똑같이 바꾸고 싶다.
- remote 명령어는 원격저장소를 관리하기 위한 명령어이다.

![21  remote rename](https://user-images.githubusercontent.com/76468280/117536052-efec6600-b033-11eb-8c92-fb6da0a31b93.PNG)

- git remote를 입력하면 현재 로컬저장소에 등록된 원격저장소의 목록이 출력된다. 
- git remote show <name> 을 입력하면 입력한 원격저장소에 대한 구체적인 설명이 출력된다.
- 그리고 git remote rename <원래이름> <바꿀이름> 을 입력하면 가리키는 원격저장소의 이름을 바꿀 수 있다. 

## tag
- 문서를 작성한 이후 그 문서에 버전을 붙이고 싶다.
- tag를 이용하면 프로젝트의 버전을 관리할 수 잇다.
- Git의 태그는 Lightweight 태그와 Annotated 태그로 두 종류가 있다.
- Lightweight 태그는 브랜치와 비슷한데 브랜치처럼 가리키는 지점을 최신 커밋으로 이동시키지 않는다. 단순히 특정 커밋에 대한 포인터일 뿐이다.
- Annotated 태그는 Git 데이터베이스에 태그를 만든 사람의 이름, 이메일과 태그를 만든 날짜, 그리고 태그 메시지도 저장한다
- 일반적으로 Annotated 태그를 만들어 이 모든 정보를 사용할 수 있도록 하는 것이 좋다. 하지만 임시로 생성하는 태그거나 이러한 정보를 유지할 필요가 없는 경우에는 Lightweight 태그를 사용할 수도 있다

![22   tag 1 0](https://user-images.githubusercontent.com/76468280/117536249-f29b8b00-b034-11eb-9320-b8191c50595a.PNG)

- git tag 명령어는 현재 존재하는 tag를 보여주는 명령어이다.
- git tag -a <version> -m "<message>" 를 이용해 annotated 태그를 만들수 있다. 또한, git show <version> 명령어는 지정한 태그의 세부적인 내용을 보여주는 명령어이다.


## 표

  |명령어|존재여부|링크|
  |---|---|---|
  |add | O |[링크](#commit-과-push)|
  |branch | O |[링크](#branch-merge-log)|
  |checkout | O |[링크](#branch-merge-log)|
  |clone | O |[링크](#로컬-저장소-생성)|
  |commit | O |[링크](#commit-과-push)|
  |config | O |[링크](#기본-환경-설정)|
  |init | O |[링크](#로컬-저장소-생성)|
  |log | O |[링크](#branch-merge-log)|
  |merge | O |[링크](#branch-merge-log)|
  |pull | O |[링크](#pull)|
  |push | O |[링크](#commit-과-push)|
  |rebase | O |[링크](#rebase)|
  |remote | O |[링크](#remote)|
  |reset --hard| O |[링크](#reset)|
  |status | O |[링크](#commit-과-push)|
  |tag | O |[링크](#tag)|
