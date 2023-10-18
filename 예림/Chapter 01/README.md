# Chapter 1_Communication 

## 1. Git으로 세련되게 협업하는 5가지 방법

- 국내에 한정된 프로젝트라면 한글로 써도 되지만 career를 위해 글로벌 오픈소스 프로젝트에 핵심 기여자(Core Contributer)로 참여하거나 해외 개발자와 협업하려면 커밋 메시지는 영어로 작성되어야 함.

### 커밋 메시지의 구성

- Subject(Title), Body, Footer로 구분됨.

```jsx
//---- Subject or Title  ----//
fix : prevent racing of requests <- Subject or Title

//---- Body  ----//
Introduce a request id and a reference to lates request. Dismiss incoming resposes other than from latest request. 

//---- Footer  ----//
Reviewed-by : Z
Refs : #123
```

### Conventional Commits의 구조

```jsx
<type>[optional scope]: <description>
[optional body]
[optional footer(s)]
```
- 소문자로 작성
- Conventional Commits를 적용하지 않는 경우 일반적으로 앞부분은 대문자를 사용하고 type 생략

### Commit Types

- `feat` : 코드에 새로운 기능(Feature) 추가
- `fix` : 버그 수정
- `BREAKING CHANGE` : 이전 버전과 호환되지 않는 변경 내역으로 !으로 표시할 수 있음.(예 : feat!:)
- `docs` : 개발 문서 변경
- `style` : 들여쓰기, 따옴표, 세미콜론 등 코드 형식 및 스타일 변경
- `ci` : CI/CD 관련 코드 변경
- `test` : 테스트 관련 코드 변경
- `build` : 빌드 시스템 관련 코드 변경
- `perf` :성능 개선 관련 코드 변경
- `chore` : 기타 코드 변경

**예시는 다음과  같다.**

```jsx
fix : remove deprecated features [수정 : 권장되지 않는 기능 삭제]
feat : add parameters to getImage [기능 : getImage에 매개변수 추가]
docs(readme): update build instructions [문서(readme) : 빌드 지침 업데이트]
chore : update npm dependencies to latest version (기타 : npm 의존성 최신 버전으로 업데이트]

// 참고 : 선택적으로 "(readme)"와 같이 변경내역이 적용되는 범위(Scope)와 맥락(Context)를 표시합니다.
```

### 영문 커밋 메시지 작성 시 유의 사항

1. **동사 원형으로 시작하기**
    - “Add dark mode”, “Fix racing condition”, “Update README”와 같이 명령적 어조의 동사 원형으로 시작하는 것이 일반적
    - Body나 Footer는 명령문으로 작성하지 않아도 됨.
    
    ```jsx
    Enable logging temporarily
    Fix bugs with setUser
    ```
    
    - 상황에 따라 과겨형 또는 3인칭 단수 현재형(예 : Adds)를 사용하는 경우도 있음.
    
2. 모두 소문자로 또는 첫 글자만 대문자로
3. a, an, the와 같은 관사(Article) 최소화
    
    ```jsx
    X : Fix a typo in the header
    O : Fix typo in header
    ```
    
4. 마침표(.)와 같은 구두점 생략
5. 변경한 이유, 상세 설명은 본문(Body)에
    - 커밋 메시지 타이틀 50자 제한

### Git 주요 실무 영어

- Squash the last 3 commits : 최근 3개의 커밋을 합치다
- Revert a pull request : 풀 리퀘스트를 되돌리다 (이전 상태로 되돌리가)
- Rebase onto another branch : 다른 브랜치로 리베이스(base를 재설정하여 커밋 재적용)하다

## 2. 외국인이 들어도 감탄할 코드 설명법

### Declare (a variable / function / class) : (변수 / 함수 / 클래스)를 선언하다

- Declare a pure function
    
    > 순수 함수 : 동일한 인자에 대해 항상 동일한 값 반환
    > 
- Declare a dictionary in Python

### Assign a value to a variable : 변수에 값을 할당하다

- Assign 5 to an integer variable
- Assign “Hi” to string variable

### Name a class : 클래스의 이름을 짓다

- Name a variable
- Rename a global constant

### Pass an argument to a function : 함수에 인자를 전달하다

- Pass arguments to a recursive function
    
    재귀 함수에 인자들을 전달하다
    
- By default, JavaScript functions do not perform type checking on the passed argument

### Return the result of execution : 실행 결과를 반환하다

- Function return
    
    함수 반환 (Return이 명사로 사용)
    

### Call a function : 함수를 호출하다

- Function call
    
    함수 호출
    
- Asynchronous call
    
    비동기 호출
### Inherit data from a parent object : 부모 객체로부터 데이터를 상속 받다

- A child class inherited from its parent class
    
    부모 클래스로부터 상속 받은 자식 클래스
    

### Execute(Run) a loop body : 반복문의 내용을 수행하다

- Execute a block of code for a certain number of times

### Iterate over (through) an array : 배열을 돌면서 반복하다

### Jump out of a loop : 반복문에서 빠져나오다

### Jump over an iteration : 반복을 한 번 건너뛰다

- You can jump over one iteratioin with the continue statement.

### Fetch data through the API : API로 데이터를 가져오다

- Retrieve data from the REST API
    
    REST API로 데이터를 검색하다
    
- Get data through Graphql queries
    
    Graphql 쿼리로 데이터를 가져오다
    

### Send data to the API server : API 서버로 데이터를 보내다

- Send a request to an API endpoint
- Post data to a backend server
    
    백엔드 서버로 데이터를 보내다

## 3. 인생은 실전, 개발 현장 속에서 배우는 실전 영어

- 오픈소스 프로젝트의 실제 풀 리퀘스트를 바탕으로 기술 토론 현장의 주요 영어 표현과 단어를 분석해보자.

### Repository Example 1

```
vinta/awesome-python
Pull Request #607 - Add hug to REST frameworks list
```

#### Example 1
- 본 오픈 소스 리포지토리는 파이썬 개발과 관련해 추천자료들을 큐레이션함.
- 본 풀 리퀘스트는 Hug라는 프레임워크를 추가하려는 사람과 Hug를 추가하는 것에 회의적인 사람간의 논쟁⚡️을 포함하고 있음.
- 생생한 기술 현장 토론으로 들어가보시죠.
1. Hug is the fastest growing framework for  `microservices` `on Python3` and `as such` clearly deserves placement on this list.
    
    Hug는 파이썬 3을 기반으로 가장 빠르게 성장하는 프레임워크이며, 그러한 이유로 리스트에 포함되어야 합니다.
2. There are `duplicate` lines.
    
    중복된 라인이 있습니다.
    
3. Not sure if this is the right place but I would go for a Services or Microservices section. Hug seems like it’d fit better under such a heading.
    
    여기가 맞는지 모르겠지만, 저는 Services 또는 Microservices 섹션이 좋은 것 같습니다. Hug는
    이러한 섹션 제목이 적합한 것 같습니다.


**주요 표현 분석**

- `Microservice` : 1 마이크로서비스(Microservice)는 애플리케이션을 작은 독립적인 서비스로 나누어 구조화 하고 개발하는 아키텍처 스타일
    - ex) 전자상거래 서비스에 마이크로서비스 아키텍처 적용 → UI, 인증 서버, 결제 처리 서버, 데이터 처리 서버, 정적 콘텐츠 저장소 등 다수의 독립적인 서비스로 나누어 설계하고 개발
    - 반대로 모든 서비스를 일체화된 형태로 설계하고 개발하는 것 : `모놀리식(Monolithic)`아키텍처
- "Program written `in` Python(파이썬으로 작성된 프로그램)"과 같이 프로그래밍 언어로 코드를 작성하는 경우에는 전치사 in을 사용하지만, 본문은 Python3를 기반으로(based on) 작성된 프로그램이라는 맥락에서 전치사 `on` 사용
- `As such` : 그러한 이유로, 그 자체로(in itself)
- 코드의 특정 부분을 언급할 때는 주로 라인(Line, 행)과 칼럼(Column, 열)을 활용
- **I’m이 생략** : 이와 같이 인터넷 상의 캐주얼한 커뮤니케이션에서는 주어 및 형용사와 함께 사용되는 be 동사가 종종 생략

#### Example 2

1. +1 for the Microservices section. This is where I'd ideally want to place it, and 1 as time goes on ****I believe there will be more and more libraries that would ****`aptly` ****fit in this
category.
    
    Microservices 섹션에 추가하는 것에 찬성합니다. 이 섹션은 제가 이상적으로 (Hug를) 배치하고 싶은
    곳이며, 시간이 지남에 따라 이 카테고리에 적합한 라이브러리가 점점 더 많아질 것입니다.
    
2. Just another framework like Flask.
    
    (Hug는) 그냥 또 하나의 플라스크 같은 프레임워크입니다. 흥
    
3. @User4 3 `With all due respect`**,** do some basic research before making such `blatantly` ****false statements.
    
    @User4 이런 말씀드려서 죄송하지만, 그런 노골적인 거짓 진술을 하기 전에 기본적인 조사를
    하시기 바랍니다. 
    

**주요 표현 분석**

- `Aptly` = Properly(적절하게)
- `With all due respect` : 직역 : 모든 존경심을 담아 / 의역 : 외람되지만, 이런 말씀드려서 죄송하지만
- `Blatantly` : 노골적으로 / 조금 더 순화된 표현 : `bluntly`(직설적으로)

#### Example 3

1. So why in one sentence is it not flask? Just because it requires a command line tool to run?
    
    😡 그렇다면 한 문장으로 Hug는 왜 플라스크 같은 프레임워크가 아닌가요? 실행하려면 커맨드 라인 도구가 필요하기 때문인가요?
