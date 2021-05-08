## URL: https://github.com/GongMinGi/SoftAssignment2.git

## 1.로컬 저장소 생성
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
