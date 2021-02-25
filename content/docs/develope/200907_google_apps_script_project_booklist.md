---
title: "Booklist using spreadsheet(+Google Apps Script), 구글 스크립트로 작성한 북리스트 자동 관리 프로그램"
date: 2020-09-07T01:32:38+09:00
tags:
# bookFlatSection: false
# bookToc: true
# bookHidden: false
# bookCollapseSection: false
# bookComments: true
---

https://dheonj.github.io/docs/develope/200812/

여기에서 대충 얘기한 독서리스트 얘기 이어서.. 

<br/>

구글 스프레드시트로 만든 독서 리스트 관리 프로그램 lite 버전.

다음 링크에서 구경할 수 있음. 이사람은 이런책을 리스트에 담가놨구나.

https://docs.google.com/spreadsheets/d/1bHBjwDHrYAHdpVS6u-1Lsywp4F4aL87wh8mhYNGNBlw/edit?usp=sharing

본인 드라이브에 복사하면 사용 가능하다.

  <br/>

![200907_1](/image/200907_1.png)

![200907_2](/image/200907_2.png)

<br/>

읽을 책, 읽은 책 이렇게 두 개의 시트로 구성되어있고, 몇가지 자동 기능이 있음 

- 각각의 리스트 맨 위 빈칸에 제목을 입력하면 자동으로 아래 리스트에 추가됨. 

- 체크박스를 클릭하면 읽은책 리스트로 옮겨지거나 리스트에서 삭제할 수도 있음.

- (std 버전 한정) 독후감을 쓸 수 있도록 자동으로 docs 파일을 생성하고 오픈함 

<br/>

lite 랑 standard를 나눈 이유는,, 

기본 구글 스프레드시트 trigger에는 드라이브에 파일을 편집할 수 있는 권한이 없기 때문이다.

권한 설정은 좀 귀찮음.. 이것도 자동화하면 좋은데. 방법은 있겠지만 뭐.

 <br/>

여튼

작년 가을쯤 기능만 대충 만들어서 쓰고있다가 

함수 구조가 너무 엉켜있어서 그것좀 풀어내고 (전공자들에게는 아직도 복잡하겠지만)

인터페이스좀 개선하고 그랬다 ㅇㅇ

이제 앞으로는 업데이트 없이 거의 이걸로 쭉 쓸듯

<br/>

사용방법:

https://docs.google.com/spreadsheets/d/1bHBjwDHrYAHdpVS6u-1Lsywp4F4aL87wh8mhYNGNBlw/edit?usp=sharing

을 본인 구글 드라이브에 복사 후 복사본 사용

<br/>

전에는 구글 캘린더랑 스프레드시트랑 연동해서 스케줄 관리도 했었는데

또 뭘 할 수 있으려나