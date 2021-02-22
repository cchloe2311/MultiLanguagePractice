# MultiLanguagePractice
안드로이드 다국어 지원 앱 연습용 레포지토리!

+) 단어는 어떻게 하는지 알겠어, 근데 통화는??
```
double number = 1000000000.0;
String COUNTRY = "US";
String LANGUAGE = "en";
String str = NumberFormat.getCurrencyInstance(new Locale(LANGUAGE, COUNTRY)).format(number);

//str = $1,000,000,000.00
```

https://developer.android.com/reference/java/util/Currency
