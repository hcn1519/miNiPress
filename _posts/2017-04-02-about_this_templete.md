---
layout: post
title:  "miNiPress의 특징"
date:   2017-04-02 13:56:55 +0900
categories: Jekyll
tags: [Jekyll, BlogTheme, miNiPress]
image:
  feature: jekyll.jpg
excerpt: "miNiPress의 기본 구성에 대해 알아봅니다."
---

`miNiPress` 테마는 다음과 같은 구성요소로 이루어져 있습니다.

## 1. 레이아웃

`miNiPress`의 레이아웃은 `poole/lanyon` 테마에 기반하여 제작되었습니다.

[https://github.com/poole/lanyon](https://github.com/poole/lanyon)

다만, `miNiPress`는 lanyon에서 제공하는 여러가지 색상 테마는 제공하고 있지 않으며, 제공되는 테마는 검정색 1개 입니다.

## 2. 폰트

`miNiPress`의 기본 폰트는 `KoPub Dotum Light`으로 한국출판인회의에서 제작한 무료 폰트입니다. 변경을 원하는 경우, `/public/sass/blogTheme.scss.css`에서 원하는 폰트를 import하고 `font-family` 속성을 변경해주세요.

코드 블럭 폰트의 경우, 네이버에서 제공되는 `D2Coding` 폰트를 사용하였습니다. `/public/sass/syntax.scss.css`에서 다른 폰트로 변경하고 적용할 수 있습니다.

## 3. Syntax Highlighting

코드 블럭에 적용되는 Syntax Highlighting의 테마는 기본적으로 `Tomorrow-Night`테마입니다. 해당 테마는 `/public/sass/syntax.scss.css`에서 변경할 수 있습니다. 예시는 아래와 같습니다.

{% highlight swift %}
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
{% endhighlight %}

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

{% highlight html %}
<figure class="animated_gif_frame" data-caption="GIF (2MB)">
  <img class="animated_gif" src="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" data-source="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" width="100%" height="auto">
</figure>
{% endhighlight %}

결과 이미지는 아래와 같습니다.

<figure class="animated_gif_frame" data-caption="GIF (2MB)">
  <img class="animated_gif" src="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif"
  data-source="https://dl.dropboxusercontent.com/s/jrgk963ymu3fhpk/42BEB33A-AAAE-45AB-A4AB-858CD3AA5CEE-848-00000083B5261F0D.gif" width="100%" height="auto">
</figure>


## 5. 태그, 카테고리

각 포스팅별로 원하는 태그와 카테고리를 설정할 수 있습니다. 태그는 전체 글 목록에서 노출되며 태그를 클릭할 경우, 태그별로 정리된 `/tags.html`로 이동하게 됩니다.

<img src="{{ site.baseurl }}/public/assets/tag-image.png">

카테고리는 태그와 유사한 기능을 담당하지만, 따로 노출이 되지는 않으며, 카테고리별로 모아볼 수 있는 기능만 제공합니다.(`/categories/index.html`)

-----
