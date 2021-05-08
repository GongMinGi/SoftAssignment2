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


