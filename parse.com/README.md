Parse.com 초기 설정하기
============================

1.Parse.com 로그인

2.사용할 App으로 이동

3.Settings 선택 후 왼쪽 메뉴의 'Application keys' 선택

 *  Application ID
 *  Client Key
 
 
![Screen shot](https://github.com/ohjongin/control-mobile-value-up-2014/blob/master/parse.com/images/settings-app-key.png?raw=true)


4.Application class 에서 초기화 하기
```java
public class ValueUpApplication extends Application {
	private static final String APPLICATION_ID="Application keys from parse.com";
	private static final String CLIENT_KEY="Client keys from parse.com";
	
	@Override
	public void onCreate() {
		super.onCreate();
		Parse.initialize(this, APPLICATION_ID, CLIENT_KEY);

		ParseACL defaultACL = new ParseACL();
		defaultACL.setPublicReadAccess(true);
		ParseACL.setDefaultACL(defaultACL, true);

	}
}
```

