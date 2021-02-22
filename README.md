# MultiLanguagePractice
안드로이드 다국어 지원 앱 연습용 레포지토리!

간단한 다국어 지원 앱을 만들어봤다.

## 목표
en, ko 각각에 해당하는 유튜브 프리미엄 가격을 출력하는 앱 만들기

## 구현
### value-ko 폴더 추가
res>value 폴더에 value-ko를 추가한다. 여기서 ko는 언어코드를 의미한다. 기본 value는 영어로 설정된다. 각 폴더 내 string.xml 파일 내 다국어로 표현하고 싶은 문자열을 정의해둔다. (화면 orientation에 대한 xml 구성과 같은 방식이다!)
### xml에서 사용하기
xml에 고정해 나오는 텍스트는 다음과 같이 xml에서 바로 넣으면 된다.
```
    <TextView
        android:id="@+id/tv_title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/youtube_price_text"
```
### kotlin 코드에서 사용하기
유튜브 프리미엄 가격을 R.string.youtube_price로 정의하고 그 값을 kotlin 코드내에서 가져와 설정하는 방법이다.
```
        val formatter: NumberFormat = DecimalFormat("#,###")
        val myNumber = getString(R.string.youtube_price).toInt()
        tv_price.text = formatter.format(myNumber)
```

이렇게 코드를 작성하면 안드로이드는 현재 기기에 설정된 언어를 가져와 맞는 언어로 화면을 구성한다.

기기의 언어 설정을 바꾸고 네이버지도에 접근 시 언어가 바뀌던 것에 대한 궁금증이 해소되었다~ 🔥
