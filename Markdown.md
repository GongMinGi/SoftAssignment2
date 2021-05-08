# 마크다운 사용법

## 1. 제목.
- 제목을 적으려면 단어 적으려는 문장 앞에 #을 붙이고 문자를 입력해야 한다. 또한 #의 개수가 늘어날 수록 크가가 작아지며 최대 6개까지 붙일 수 있다.<br>
ex)1. # 마크 2. ## 마크 3. ### 마크
# 마크
## 마크
### 마크

- 또한 적은 문장 아래에 = 혹은 - 를 입력하여 각각 #, ## 을 사용한 크기의 제목을 만들 수도 있다.       
    
      heading     heading2
      =======     --------
## 2. 줄바꾸기
- 마크다운에서 줄을 바꾸는 방법은 두가지가 있는데 엔터를 두 번 이상 입력하거나 문장 끝에 <> 을 입력하고 안에 br을 입력하면 줄을 바꿀 수 있다.


## 3. 강조
- **굵게**: 마크다운에서 글씨를 굵게 하기 위해서는 2가지 방법을 사용할 수 있는데, 첫째로 **  ** 이 애스터리스크 사이에 문자를 입력하는 방법이있고, __   __ 언더바 사이에 문자를 입력하는 방법이있다. 

      예시:  **예시**,   __예시__

- *이탈릭체* : 이탈릭체를 사용하고 싶을 때는 * * 사이에 문자를 입력하거나 _ _ 사이에 입력하면 됀다. 문자를 굵게 하는 것과 차이점은 각각 쓰이는 * 와 _가 한개라는 것.
  
      예시: *예시*,  _예시_

- ***동시사용*** : 이탈릭체와 굵은 글씨를 동시에 사용하는 것도 가능하다. *** ***, ___ ___ 처럼 밑줄과 에스터리스크를 3개씩 사용하거나 2개 1개 씩 섞어서 사용한다.

       예시: ***예시*** ,  ___예시___, __*예시*__, **_예시_**, 

- 주의사항: 위에 서술된 어떤 강조를 사용할 때에도 문장사이에 오는 단어를 강조할때 예를들어 *이것* 처럼 사용할때 __ 로만 이루어진 방법을 사용해선 안됀다. 밑줄과 에스터리스크가 섞인 표기, 혹은 에스터리스크로만 이루어진 표기를 사용하자

      문장사이에 쓸때는 *이렇게* 사용하자.
## 4.인용구
- 인용구를 사용할 때에는 > 를 문단앞에 붙이자<br>
> 이런식으로 왼쪽에 막대기가 생긴다.<br>
___
>인용구는 중첩되어 사용할 수 도 있는데 이 경우에는 >> 이렇게 2번 사용해주면 된다.
>> 중첩시 이런 모양이 된다.

## 5.리스트.
- 순서대로 목록을 정렬하고 싶을 때는 목록의 앞에 숫자와 점을 추가 해주면 된다. 이 때 숫자는 순서대로 적지 않아도 돼지만, 첫번 째 순서는 1이어야 한다. 예를들어 1, 5, 6, 3 순서로 목록을 입력해도 1,2,3,4, 순서로 출력된다.

- 순서 구분이 없는 목록을 출력하고 싶을 때에는  -, *,+ 등의 기호를 입력하고 글자를 입력하면 현재 문단에 붙어있는 동그란 목록 표시 기호를 쓸 수 있다. 단, 세 개의 기호를 섞어 쓰지 말고 하나로 통일해야 한다. 

    하나의 목록의 이와 같이 새로운 문단을 추가하고 싶을 때는 줄을 한칸 띄운 뒤, tab이나 스페이스 바 4번을 이용하여 이처럼 쓸 수 있다.
    
    >인용구 또한 같은 방식으로 쓸 수 있다


- 코드블럭: 특정한 기능을 하는 기호나 문자들을 코드블럭이라고 하는데, 이것들은 보통 tab이나 스페이스 4번으로 입력할 수 있지만, 리스트 내부에서는 tab을 2번, 스페이스를 8번 입력해야한다. 다음은 예시이다.

        ##      <head>      <html>      *강조*

- 이미지: 이미지를 입력하려면 !를 적은 대괄호 안의 제목을 입력하고 괄호안에 경로를 입력하면 된다.
  <br> ex: ! [해바라기] (.\image\해바라기.jpg)

![해바라기](https://user-images.githubusercontent.com/76468280/117534069-d85caf80-b02a-11eb-9911-693535a7d5a9.jpg)

 - 리스트중첩: tab을 1번 입력하여 리스트 내부에 다른 리스트를 만들 수 도 있다.
   - 이런 형태의 리스트가 만들어진다.

## 6.코드
-  단어나 구를 코드로 표기하고 싶을 경우엔 `` ` ` ``사이에 문자를 입력하면 된다  
-  탈출: 코드로 나타낼 단어 또는 구문에 하나 이상의 백틱(')이 포함되어있다면, 단어 또는 구문을 이중 백틱('')으로 묶으면 탈출 할 수 있습니다.
   -  예시: `` 이것은 `예시 문장` 입니다. ``




## 7. 링크
- 링크를 만들려면 대괄호 안에 제목을 적어넣고 그 뒤에 바로 괄호를 입력하고 그 안에 링크를 넣으면 됀다.
  - ex) [Duck Duck Go] (https://duckduckgo.com).
  - = 내가 좋아하는 검색엔진은 [Duck Duck Go](https://duckduckgo.com)다.

- 제목 넣기 : 링크에 추가로 제목을 넣을 수 있다. 아래 예시 처럼 링크 뒤에 ("") 를 이용해서 제목을 넣을 수 있는데, 이 경우 링크에 마우스를 올리면 입력한 내용이 보여진다.
  - 내가 좋아하는 검색엔진은  [Duck Duck Go] (https://duckduckgo.com "The best search engine for privacy")이다.
  - = 내가 좋아하는 검색엔진은 [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy")이다.

- URL과 이메일 주소: <> 안에 URL과 메일주소를 입력하는 것으로 간단히 링크를 걸 수 있다.
  - < https://www.markdownguide.org > , < fake@example.com >
  - <https://www.markdownguide.org>
  - <fake@example.com>


-  링크 강조: 링크를 강조하기 위해서는 대괄호 전과 소괄호후에 (*) 를 사용하면 되고, 코드로 만들기 위해선 괄호안에 ('')을 추가해야 한다.<br>

        I love supporting the **[EFF](https://eff.org)**.
        This is the *[Markdown Guide](https://www.markdownguide.org)*.
        See the section on [`code`](#code).
    결과는 이렇게 나온다.

    I love supporting the **[EFF](https://eff.org)**.<br>
    This is the *[Markdown Guide](https://www.markdownguide.org)*.<br>
    See the section on [`code`](#code).

- 참조 스타일 링크: 참조 스타일 링크는 URL을 마크다운에서 쉽게 표시하고 읽을 수 있도록 하는 특수한 종류의 링크이며 총 2단계로 구성된다.
  - 1단계
  
    첫번쨰 부분은 두 개의 괄호로 구성되며 첫번째 대괄호는 링크된 것으로 표시되는 텍스트를 둘러싸며, 두번 째 괄호는 문서의 다른곳에 저장된 링크를 가리키는데 사용된다.<br>
    ex) [hobbit-hole][1]<br>
        [hobbit-hole] [1]

    괄호사이에 스페이스바를 넣어도 상관없다.
  - 2단계

    두 번째 부분은 실제 링크가 저장되 있는 장소이며, 이는 문서 어디에든 올 수 있다. 즉 주석처럼 사용할 수 있다는 의미이다. 다음 표기는 모두 같은 의미를 가진다.

        [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
        [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
        [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'
        [1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)
        [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
        [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'
        [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)
  - 예시

        In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
        of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
        eat: it was a [hobbit-hole][1], and that means comfort.

        [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
        이 문장은 다음과 같이 출력된다.


        In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to eat: it was a [hobbit-hole][1], and that means comfort.

    [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"


- 이미지 링크: 이미지 자체에 링크를 걸기 위해 마크다운 언어로 표기한 이미지에 대괄호를 씌운뒤 다음 소괄호 안에 링크를 적는다.

        [![An old rock in the desert](.\image\shiprock.jpg "Shipr ock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

     결과는 이렇게 나온다.

     [![An old rock in the desert](.\image\shiprock.jpg "Shipr ock, New Mexico by Beau Rogers")](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

## 8.문자열 탈출
 - 마크다운 언어에서 서식으로 쓰이는 문자들을 표기하기 위해서 \를 사용한다. <br>다음은 예시이다.
  
        \* Without the backslash, this would be a bullet in an unordered list.
    이는 다음과 같이 출력된다.

        * Without the backslash, this would be a bullet in an unordered list.


    아래 문자들이 \를 통해 탈출할 수 있는 문자들이다.

    |문자|문자명|
    |---|---|
    |\ | 백슬래쉬|
    |` | 그래이브|
    |* | 에스터리스크|
    |_ | 언더바|
    |{}| 중괄호|
    |[]| 대괄호|
    |<>| 앵글브래킷(부등호)|
    |()| 괄호|
    |# | 샵 |
    |+ | 플러스|
    |- | 마이너스|
    |. | 점|
    |! | 느낌표|
    |\|| 파이프|

## 9. HTML
- 많은 마크다운 응용 프로그램에서는 html 태그를 마크다운 언어로 사용하는걸 가능하게 해준다. 이는 마크다운 언어보다 특정 html 태그를 선호하는 경우에 유용하다. 예를 들어 몇몇 사람들은 이미지에 HTML 태그를 사용하는 것이 더 쉽다고 생각한다.<br>다음은 HTML태그를 사용한 이탈릭체와 마크다운 언어를 사용한 굵은 글씨다.

        This **word** is bold. This <em>word</em> is italic

    This **word** is bold. This <em>word</em> is italic.  이렇게 출력됀다.

## 10. 깃허브 링크
<https://github.com/GongMinGi/GFMpractice>