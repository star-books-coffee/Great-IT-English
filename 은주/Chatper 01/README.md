### 1. Git으로 세련되게 협업하는 5가지 방법

- 전 세계적으로 통용되는 커밋 메시지 관습 : Conventional Commits
- 커밋 메시지는 Subject (Title), Body, Footer로 구분됨
- Conventional Commits의 구조
    > <type[optional scope]:<description> <br>
    [optional body] <br>
    [optional footer(s)]
    > 
    - docs(readme): update build instructions ［문서(readme) 빌드 지침 업데이트］
    
    → 선택적으로 (readme) 와 같이 **변경 내역이 적용되는 범위와 맥락을 표시**
    
- 커밋 메시지에 Conventional Commits를 적용하지 않는 경우, 일반적으로 앞부분만 대문자를 사용하고 type을 생략
- 영문 커밋 메시지 작성법
    1. 명령적 어조의 `동사 원형` 으로 시작하라
        - Fix : 수정하다
        - Bump : 버전을 올리다
        - Wrap : 감싸다, 그룹화하다
    2. 모두 소문자로 또는 첫 글자만 대문자로
    3. 관사 최소화
    4. 마침표(.)와 같은 구두점(Punctuation Mark) 생략
    5. 변경한 이유, 상세 설명은 본문（Body）에
- 주요 실무 영어
    - Squash the last 3 commits ; 최근 3개의 커밋을 합치다
 
### 2. 외국인이 들어도 감탄할 코드 설명법

- `Declare` a (variable / function / class): (변수 / 함수 / 클래스)를 선언하다
- `Assign` a value to a variable : 변수에 값을 할당하다
    - 변수에 초기값 할당 (Assign) 하는 초기하는 `Initialize`
- `Name` a class : 클래스의 이름을 짓다
- `Pass` an argument to a function : 함수에 인자를 전달하다
- `Call` a function : 함수를 호출하다
    - 다른 대상이 함수를 "불러오는" 경우에는 invoke를, 직접 함수를 "호줄하는" 경우에는 call을 사용합니다
    - **함수를 "불러오는" 경우 (Invoke)**
        - **Event Handler**: 웹 페이지에서 버튼을 클릭하면 이벤트 핸들러가 함수를 "불러옵니다"
            
            ```jsx
            button.addEventListener('click', myFunction); // 이벤트 핸들러가 myFunction을 "불러옴" (invoke).
            ```
            
        - **Promise**: 프로미스를 사용하여 비동기 작업을 수행할 때, **`.then()`**을 통해 성공 또는 실패 콜백 함수를 "불러옵니다"
            
            ```jsx
            javascriptCopy code
            fetchData()
              .then(successCallback) // 성공 시 successCallback 함수를 "불러옴" (invoke).
              .catch(errorCallback); // 실패 시 errorCallback 함수를 "불러옴" (invoke).
            
            ```
            
    - **함수를 "호출하는" 경우 (Call)**
        - **직접 함수 호출**: 함수를 직접 호출할 때, 함수를 "호출" (call)
            
            ```jsx
            function add(a, b) {
              return a + b;
            }
            
            const result = add(3, 5); // 함수 add를 "호출" (call) 함.
            ```
       
        - **재귀 함수 호출**: 함수 내에서 자신을 호출할 때, 자기 자신을 "호출"


            ```jsx
            function factorial(n) {
              if (n <= 1) {
                return 1;
              }
              return n * factorial(n - 1); // 자신을 "호출" (call) 함.
            }
            
            const result = factorial(5);
            ```
- `Execute (Run)` a loop body : 반복문의 내용을 수행하다
- `Iterate over` (through) an array :
배열을 돌면서 반복하다