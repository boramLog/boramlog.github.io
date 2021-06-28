---
typora-root-url: ..\..\..\..\..\workspace\boramlog\assets\images
---

# 깃허브로 블로그 만들기

### 1. 깃허브 가입하고 저장소 만들기

##### 1-1. 깃허브 가입

https://github.com/

깃허브에 들어가서 Sign up을 해줍니다.

![1-1(1)](/assets/images/1-1(1).jpg)

-----------------------------------------------------------------------------------------------------

<img src="1-1(1).jpg" style="zoom:50%;" />

이때 username은 내 블로그 주소에 사용되니 신중히 적어줍니다.



##### 1-2. 저장소 만들기

![1-2(1)](C:\Users\b0109\OneDrive\바탕 화면\깃허브 블로그 개설 관련\1-2(1).jpg)

Create a repository를 눌러 저장소를 만들어줍니다.

![1-2(2)](C:\Users\b0109\OneDrive\바탕 화면\깃허브 블로그 개설 관련\1-2(2).jpg)

저장소 이름은 내 블로그의 주소가 되며 

> *username***.github.io** 

위와 같은 형식으로 설정해주며 대소문자는 상관 없습니다.

username은 꼭 깃허브 가입할 때 적었던 username과 동일하게 적어줍니다.

옆에 있는 Owner와 똑같으면 됩니다.

<img src="C:\Users\b0109\OneDrive\바탕 화면\깃허브 블로그 개설 관련\1-2(3).jpg" alt="1-2(3)" style="zoom:70%;" />

저장소 생성이 완료되었습니다.



##### 1-3. username을 다시 설정하고 싶은 경우

1-2(4)사진

우측 상단의 프로필 아이콘을 눌러줍니다.

Setting을 선택하신 후

1-2(5)사진 1-2(6)사진

Account > Change username을 눌러 변경해주시면 됩니다.

1-2(7) 

username이 변경되었습니다.



##### 1-4. 저장소를 다시 만들고 싶은 경우

1-2(8)

repository의 setting으로 들어갑니다.

Options를 선택한 후 스크롤을 맨 마지막까지 내리면 Danger Zone이 있습니다.

1-2(9)사진

Delete this repository를 선택해줍니다.

1-2(10)사진

나의 저장소 주소명을 적어주시면 삭제가 완료됩니다.



### 2. 루비 설치하기

##### 2-1. 루비 설치하기

사진2-1(1)

https://rubyinstaller.org/downloads/

필자는 루비에서 추천(=>)해주는 DEVKIT을 설치하였습니다.

필자가 사용하려는 https://github.com/mmistakes/minimal-mistakes 테마에서는 루비 버전에 따라 안되는 경우가 있다고하니 참고하시기 바랍니다. [^2-1.ruby]

> [^2-1.ruby]: https://honbabzone.com/jekyll/start-gitHubBlog/

사진2-1(2)~(5)

모든 체크박스를 선택한 후 설치를 진행해주시면 됩니다.

사진2-1(6)

설치를 완료하면 위와 같은 창이 뜹니다.

1을 선택하고 엔터키를 눌러주시면 됩니다.

사진2-1(8)

엔터키를 눌러서 창을 닫아주면 설치가 완료됩니다.



### 3. 깃 설치하기

##### 3-1. 깃 설치하기

사진 6-1(1)

https://git-scm.com/downloads

자신의 OS에 맞게 다운로드를 해줍니다.

아무 변경없이 그냥 next만 눌러주시면 됩니다.

사진 6-1(2)

깃 설치가 완료되었습니다.



##### 3-2. 로컬 폴더와 저장소와 연결하기

로컬 폴더 위치를 정해줍니다.

필자는 C:\workspace\boramlog 로 설정해주었습니다.

이때 주소명에 한글, 공백이 들어가지 않게 주의합니다.

사진 6-2(1)

설치된 Git Bash를 실행시켜줍니다.

먼저 위치를 로컬 폴더 위치로 바꿔 줍니다.

cd .. : 부모 폴더로 돌아가기

cd 하위 폴더명 : 하위 폴더로 들어가기

사진 6-2(2)

```
git config --global user.name "이름"

git config --global user.email "이메일"
```

깃에 사용자이름과 이메일주소를 설정해줍니다. 마우스 오른쪽을 클릭하여 쉽게 붙여넣기 할 수 있습니다.

깃을 커밋할 때마다 이 정보를 사용합니다.

사진 6-2(3)

```
git init
```

깃 저장소를 생성해줍니다.

그러면 로컬 폴더 주소 옆에 (master)가 추가가 됩니다.

사진 6-2(4)

```
git remote add origin https://github.com/boramLog/boramlog.github.io.git

git remote -v
```

git remote add origin 저장소 주소

git remote -v

저장소 주소를 연결 후 확인해줍니다.

사진 6-2(5)

원격지 주소는 깃허브에 들어가셔서 위의 아이콘을 누르시면 복사됩니다.



### 3. 지킬 설치하기

사진3-1(1)

로컬 폴더 위치로 설정해준 폴더에 들어가서 주소창에 cmd를 입력 후 엔터키를 눌러줍니다.

사진 3-1(2)

경로가 로컬 폴더의 경로와 같은지 확인해줍니다.

만약 경로가 다를 경우  로컬 폴더의 경로로 바꿔줍니다.

cd .. : 부모 폴더로 돌아가기

cd 하위 폴더명 : 하위 폴더로 들어가기

사진 3-1(3)

`ruby -v`을 입력하여 루비가 잘 설치되었는지 확인합니다.

사진 3-1(4)

`gem install jekyll bundler`

지킬 번들러를 설치합니다.



### 4. 테마 적용하기

이제 본인이 적용하고 싶은 테마를 찾아서 로컬 폴더에 올려줍니다.

필자는 https://github.com/topics/jekyll-theme?o=desc&s=forks에서 가장 많은 포크와 별을 가지고 있는 [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)를 선택했습니다.

사진 4-1(1)

위의 아이콘을 누르면 쉽게 테마의 주를 복사해 올 수 있습니다.

사진 4-1(2)

`git clone https://github.com/mmistakes/minimal-mistakes.git`

git clone [복사해 올 테마의 주소] 를 사용해 테마를 복사해옵니다.

minimal-mistakes 폴더가 잘 복사가 되었습니다.

사진 4-1(4)

필자는 C:\workspace\boramlog를 로컬 폴더로 정했으므로 전체 파일을 옮겨줍니다. 

minimal-mistakes 폴더 안에 들어가서 전체 선택 후 Ctrl + X로 잘라내신 후 로컬 폴더 안에 Ctrl + V로 붙여넣으시면 됩니다.

위의 방법이 번거롭다면 

사진 4-1(3)

직접 다운로드하셔서 로컬 폴더 위치에 옮겨주셔도 됩니다.

사진 4-1(5)

받은 테마가 로컬 폴더에 잘 위치되어 있다면

```bundle exec jekyll serve```을 사용해 지킬 서버를 실행합니다.

이때 위와 같은 문구가 뜨면 우선 Ctrl + C를 눌러 빠져나옵니다.

사진 4-1(7)

그리고 로컬 폴더에 들어있는 Gemfile을 열어 `gem 'wdm', '>= 0.1.0'`를 추가 후 저장해줍니다.

사진 4-1(8)

```
gem install jekyll bundler

bundle exec jekyll serve
```

위의 명령어를 다시 한 번 실행해줍니다.

http://127.0.0.1:4000/에 접속하여 잘 실행이 되고 있는지 확인합니다.

사진 4-1(6)

테마가 잘 적용된 모습입니다.



### 5. 저장소에 올리기

적용된 테마를 자기의 스타일에 맞춰 설정한 후 저장소에 올려 내 블로그 주소에 적용해 보겠습니다.

minimal-mistakes 테마의 설정은 를 참고해주시길 바랍니다.

사진 5-1(1)

지금 나의 블로그 주소를 들어가면 위와 같이 아무것도 적용되어있지 않은 모습입니다.

사진 5-1(7)

```
$ cd ..
$ cd ..
$ cd workspace
$ cd boramlog // 경로 변경
$ git config --global user.name "이름"
$ git config --global user.email "깃허브 가입 이메일"
$ git init
$ git add . // 깃에 모든 변경사항 반영
$ git commit -m '커밋 메시지' // 변경사항 커밋
$ git remote add origin [깃허브 저장소 주소]
$ git remote -v
$ git push -u origin master
```

`$ git push -u origin master` 명령어 이후 아무 반응이 없는 경우

로컬 폴더에서 cmd 창을 열어 `$ git push -u origin master` 명령어를 입력합니다.

사진 5-1(8)

1 입력 후 엔터키를 누르면 브라우저 창이 뜨는데 초록색 버튼을 눌러줍니다.

사진 5-1(9)(10)

패스워드를 입력하여 자격증명을 완료해줍니다.

