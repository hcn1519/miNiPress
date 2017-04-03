# Github miNiPress

Site Demo: [https://hcn1519.github.io](https://hcn1519.github.io)

<figure class="animated_gif_frame" data-caption="GIF (2MB)">
  <img class="animated_gif" src="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" data-source="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" width="100%" height="auto">
</figure>


**Github 블로그** 는 github에서 호스팅을 지원해주는 블로그 플랫폼으로 누구나 **Github** 계정이 있다면 시작할 수 있는  jekyll이라는 *static framework* 에 기반한 블로그입니다. **Github** 블로그의 가장 큰 장점은 `html`, `css`, `git` 을 조금만 알고 있다면 모든 기능 및 디자인을 마음대로 ㄴ내 마음대로 설정할 수 있다는 점입니다. 무엇보다도 **무료** 입니다! 지금 바로 시작해보세요!

-----

# Getting Started

## Using github-pages

<img src="https://rawgit.com/hcn1519/miNiPress/master/public/assets/github-Pages.png">

[https://pages.github.com](https://pages.github.com)

위의 링크를 타고 가시면, Github Pages를 시작하는 방법에 대해 나와있습니다. 다만 템플릿을 사용하기 위해서는 순서가 다소 다를 수 있으니 다음 과정을 따라주세요.

### 1. Fork Repository

사용하기를 원하는 템플릿을 내 `Repository`로 `fork` 해옵니다. 여기서 `fork`란 포크로 다른 사람의 `Repository`를 내 `Repository`로 찍어오는 것을 의미합니다. 아래 링크로 가서 `miNiPress` 템플릿을 `fork`해주면, 해당 `Repository`가 자신의 `Repository`로 복사되는 것을 확인할 수 있습니다.

[https://github.com/hcn1519/miNiPress](https://github.com/hcn1519/miNiPress)

<img src="https://rawgit.com/hcn1519/miNiPress/master/public/assets/fork.png">

### 2. Rename Repository

해당 `Repository`가 블로그를 위해 사용된다는 것을 github이 알 수 있도록 `Repository`의 이름을 변경해줍니다. `Settings`탭에 들어가면, 이름을 변경할 수 있는데, 이 때 이름은 항상 `"username".github.io`의 형태이어야 합니다.(ex - `hcn1519.github.io`)

<img src="https://rawgit.com/hcn1519/miNiPress/master/public/assets/rename.png">

### 3. All done!

<img src="https://rawgit.com/hcn1519/miNiPress/master/public/assets/youDone.png">

여러분의 URL(`"username".github.io`)로 이동하면, 블로그가 만들어진 것을 확인할 수 있습니다.

-----

## 첫 포스트 작성하기

### 방법 1. github 사이트에서 바로 작성하기

여러분의 `Repository`에서 바로 첫 포스트를 작성할 수 있습니다. `/_posts`로 이동 후 `test.md` 혹은 `test.html`을 생성합니다. 그리고 해당 파일에 헤더로(파일의 최상단에) 다음과 같은 필요한 포스트 정보를 작성합니다.

```ruby
layout: post
title:  "Welcome to Jekyll miNi Press!"
date:   2017-03-29 13:56:55 +0900
categories: jekyll
tags: [jekyll, blogTheme]
excerpt: "Welcome to MiniPress"
```

그리고 바로 아래에 포스트 내용을 작성하면 됩니다.

### 방법 2. 로컬에서 포스트 작성하기

이 방법은 컴퓨터에 `git`이 설치되어 있어야 합니다. 먼저 `git`을 설치하고, 다음 과정을 진행해 주세요.

프로젝트를 다운 받고, 해당 프로젝트의 `/_posts`로 이동 후 `test.md` 혹은 `test.html`을 생성합니다. 그리고 해당 파일에 헤더로(파일의 최상단에) 다음과 같은 필요한 포스트 정보를 작성합니다.

```ruby
layout: post
title:  "Welcome to Jekyll miNi Press!"
date:   2017-03-29 13:56:55 +0900
categories: jekyll
tags: [jekyll, blogTheme]
excerpt: "Welcome to MiniPress"
```
그리고 포스트 내용을 작성합니다. 이후, 다운 받은 프로젝트를 github으로 푸쉬하는 작업이 필요합니다. 터미널에서 다운 받은 프로젝트로 이동 후, 다음 명령어를 순서대로 입력하면, 내 글이 서버에 올라가게 됩니다.

```Bash shell scripts
$ git init
$ git add -A
$ git commit -m "Adding Test Post"
// username과 repo이름 설정이 필요합니다.
$ git remote add origin remote "https://github.com/'github username'/'repo 이름'.git"
$ git push -u origin master
```

-----

## Local Posting with Jekyll

Jekyll을 설치하게 되면, 작성한 포스팅을 실제 블로그에 올리기 전에 내 컴퓨터에서 확인할 수 있습니다.

```Bash shell scripts
$ gem install jekyll
```

Jekyll이 설치되면, 터미널에서 설치된 블로그의 루트 경로로 이동합니다. 그리고 해당 경로에서 다음 명령어를 치게되면, 블로그가 local에서 실행됩니다.

```Bash shell scripts
$ bundle exec jekyll serve
```

그리고 웹브라우저에서 `localhost:4000`으로 접속하면, 내 블로그의 내용들을 확인할 수 있습니다.

-----

# miNiPress 구성요소

## 1. 레이아웃

**miNiPress** 의 레이아웃은 `poole/lanyon` 테마에 기반하여 제작되었습니다.

[https://github.com/poole/lanyon](https://github.com/poole/lanyon)

다만, **miNiPress** 는 lanyon에서 제공하는 여러가지 색상 테마는 제공하고 있지 않으며, 제공되는 테마는 검정색 1개 입니다.

## 2. 폰트

`miNiPress`의 기본 폰트는 `KoPub Dotum Light`으로 한국출판인회의에서 제작한 무료 폰트입니다. 변경을 원하는 경우, `/public/sass/blogTheme.scss.css`에서 원하는 폰트를 import하고 `font-family` 속성을 변경해주세요.

코드 블럭 폰트의 경우, 네이버에서 제공되는 `D2Coding` 폰트를 사용하였습니다. `/public/sass/syntax.scss.css`에서 다른 폰트로 변경하고 적용할 수 있습니다.

## 3. Syntax Highlighting

코드 블럭에 적용되는 Syntax Highlighting의 테마는 기본적으로 `Tomorrow-Night`테마입니다. 해당 테마는 `/public/sass/syntax.scss.css`에서 변경할 수 있습니다. 예시는 아래와 같습니다.

```swift
# Swift 예시
import XCTest
class ProjectNameUITests: XCTestCase {
  override func setUp() {
     super.setUp()
     continueAfterFailure = false
     let app = XCUIApplication()
     setupSnapshot(app)
     app.launch()
 }
 override func tearDown() {
     super.tearDown()
 }
 func testSnapshot() {
 }
}
```

## 4. 이미지

이미지의 경우 크게 2가지 방식을 통해 보여줄 수 있습니다.

### (1) 블로그 프로젝트에 이미지를 추가하고 구현하기

원하는 위치에 이미지를 프로젝트에 넣어두고, 이미지 태그의 `src` 경로를 올바르게 설정해줍니다.
{% highlight html %}
<img src="{{ site.baseurl }}/public/assets/github-Pages.png">
{% endhighlight %}

결과 이미지는 다음과 같습니다.
<img src="{{ site.baseurl }}/public/assets/github-Pages.png">

### (2) 외부 클라우드에 이미지 저장 후, 링크로 가져오기

여기서는 dropbox에 대한 예시를 넣어두었습니다.

{% highlight ruby %}
# 링크 공유하면 나오는 URL
https://www.dropbox.com/s/cspxnwj2ziqlfpg/getting_started.png?dl=0
# www를 dl로 변경하고, png 이하 ?dl=0 제거
https://dl.dropbox.com/s/cspxnwj2ziqlfpg/getting_started.png
{% endhighlight %}

결과 적용 후 URL과 이미지
{% highlight html %}
<img src="https://dl.dropbox.com/s/cspxnwj2ziqlfpg/getting_started.png">
{% endhighlight %}

<img src="https://dl.dropbox.com/s/cspxnwj2ziqlfpg/getting_started.png">

### (3) GIF extension

GIF로 움직이는 이미지의 경우 아래 코드의 `src`와 `data-source` 부분을 경로에 맞게 설정해주면 됩니다. 여기서는 맥의 앱스토어에 있는 `Jeff`라는 툴을 이용하여 GIF를 만들었습니다.


```html
<figure class="animated_gif_frame" data-caption="GIF (2MB)">
  <img class="animated_gif" src="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" data-source="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" width="100%" height="auto">
</figure>```

결과 이미지는 아래와 같습니다.

<figure class="animated_gif_frame" data-caption="GIF (2MB)">
  <img class="animated_gif" src="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif"
  data-source="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" width="100%" height="auto">
</figure>

## 5. 태그, 카테고리

각 포스팅별로 원하는 태그와 카테고리를 설정할 수 있습니다. 태그는 전체 글 목록에서 노출되며 태그를 클릭할 경우, 태그별로 정리된 `/tags.html`로 이동하게 됩니다.

<img src="{{ site.baseurl }}/public/assets/tag-image.png">

카테고리는 태그와 유사한 기능을 담당하지만, 따로 노출이 되지는 않으며, 카테고리별로 모아볼 수 있는 기능만 제공합니다.(`/categories/index.html`)
