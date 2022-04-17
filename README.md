복싱 사이트

## 실습 진행 중 겪은 어려움
### 1. push 에러 - Sourcetree에서 GitHub 계정 연결 문제 
  * 현상
    *  Boxiting-cat에서 파일 수정 후에 add, commit, push를 시도했는데 push가 되지 않았다. 
  * 원인 추측
    * 소스트리와 깃헙을 연동할 때 유저 네임과 패스워드를 써야 했는데, 이 때 실수로 깃헙 로그인 패스워드를 써 버린 것이 문제인 듯 하다.
    * personal access token을 적용하기 전에 비밀번호를 통한 로그인을 시도했을 경우 저장되어있는 비밀번호로 인해 로그인이 안될 수 있다고 한다. 
  * 해결 시도
    * 소스트리에서 설정 > 저장소 설정을 편집하여, URL경로에서 http://와 github 사이에 토큰@을 입력해주었다.
    * url을 https://personalaccesstoken@github.com/~ 으로 편집하자 push가 가능해졌다. 
    
    
    
  * 참고 - 문제파악과 해결을 위해 다음의 자료를 참고했다.
    * [- Make Me - : 네이버 블로그](https://blog.naver.com/greatperson21/222481333164)
    * [Sourcetree에서 github 계정 연결 문제 해결하기 - Alice_wiki](https://aliceleeme.github.io/develop/Sourcetree-login-error-on-mac/)

### 2. Sourcetree에서 두번째 로컬 저장소 추가할 때 발생하는 에러
  * 현상
    * push가 불가능하던 문제를 해결한 뒤 실습이 원활하게 진행될 줄 알았는데, boxiting-oct를 소스트리에 추가하고자 했을 때 (캡쳐 이미지)와 같은 오류창이 떴다.
    * 로컬저장소에 -cat 폴더를 추가하는 것 까지는 가능하다. 하지만 -oct폴더를 추가하려고 하면 오류창이 뜬다.
    * 일단 오류창이 뜨면 ‘다시열기'를 눌러보아도 소스트리 창이 팝업조차 되지 않는다. 
  * 원인 추측
    * 앞서 GitHub계정 연결에서 잘못된 패스워드를 입력한것이 원인일까?
    * push에러를 해결하기 위해 url을 편집한 것이 원인일까?  
  
  * 해결 시도
    1. 키체인 액세스에서 GitHub Credentials와 GitHub.comAccessKeyfor[계정명]을 삭제 후 PC 재부팅하기 
    2. 소스트리 완전 삭제(응용프로그램에서 소스트리 삭제, 파인더에서 ~/Library/Application Support/SourceTree 삭제, ~/Library/Preferences/com.torusknot.SourceTreeNotMAS.plist 삭제)한 뒤 재부팅하고 소스트리를 재설치하기
    3. 소스트리의 Boxiting-cat폴더에서 설정> 원격 저장소 정보> URL경로를 편집하여, 푸시 오류를 해결하기 위해서 추가했던 토큰@을 삭제
    
  * 현재 상황
    * 해결법 1~3을 여러번 시도해본 뒤에도 문제가 해결되지 않아 질문글을 올렸다.  
   
