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

**Example 1**

- 👤 User 1 코멘트
    
    Hug is the fastest growing framework for  `microservices` `on Python3` and `as such` clearly deserves placement on this list.
    
    Hug는 파이썬 3을 기반으로 가장 빠르게 성장하는 프레임워크이며, 그러한 이유로 리스트에 포함되어야 합니다.
    
- 👤 User 2 코멘트
    
    There are `duplicate` lines.
    
    중복된 라인이 있습니다.
    
- 👤 User 3 코멘트
    
    `Not sure` if this is the right place but I would go for a Services or Microservices section. Hug seems like it’d fit better under such a heading.
    
    여기가 맞는지 모르겠지만, 저는 Services 또는 Microservices 섹션이 좋은 것 같습니다. Hug는
    이러한 섹션 제목이 적합한 것 같습니다.
    
- **주요 표현 분석**
    - `Microservice` : 1 마이크로서비스(Microservice)는 애플리케이션을 작은 독립적인 서비스로 나누어 구조화 하고 개발하는 아키텍처 스타일
        - ex) 전자상거래 서비스에 마이크로서비스 아키텍처 적용 → UI, 인증 서버, 결제 처리 서버, 데이터 처리 서버, 정적 콘텐츠 저장소 등 다수의 독립적인 서비스로 나누어 설계하고 개발
        - 반대로 모든 서비스를 일체화된 형태로 설계하고 개발하는 것 : `모놀리식(Monolithic)`아키텍처
    - "Program written `in` Python(파이썬으로 작성된 프로그램)"과 같이 프로그래밍 언어로 코드를 작성하는 경우에는 전치사 in을 사용하지만, 본문은 Python3를 기반으로(based on) 작성된 프로그램이라는 맥락에서 전치사 `on` 사용
    - `As such` : 그러한 이유로, 그 자체로(in itself)
    - 코드의 특정 부분을 언급할 때는 주로 라인(Line, 행)과 칼럼(Column, 열)을 활용
    - **I’m이 생략** : 이와 같이 인터넷 상의 캐주얼한 커뮤니케이션에서는 주어 및 형용사와 함께 사용되는 be 동사가 종종 생략

**Example 2**

- 👤 User 1 코멘트
    
    +1 for the Microservices section. This is where I'd ideally want to place it, and 1 as time goes on ****I believe there will be more and more libraries that would ****`aptly` ****fit in this
    category.
    
    Microservices 섹션에 추가하는 것에 찬성합니다. 이 섹션은 제가 이상적으로 (Hug를) 배치하고 싶은
    곳이며, 시간이 지남에 따라 이 카테고리에 적합한 라이브러리가 점점 더 많아질 것입니다.
    
- 👤 User 4 코멘트
    
    Just another framework like Flask.
    
    (Hug는) 그냥 또 하나의 플라스크 같은 프레임워크입니다. 흥
    
- 👤 User 1 코멘트
    
    @User4 3 `With all due respect`**,** do some basic research before making such `blatantly` ****false statements.
    
    @User4 이런 말씀드려서 죄송하지만, 그런 노골적인 거짓 진술을 하기 전에 기본적인 조사를
    하시기 바랍니다. 
    
- **주요 표현 분석**
    - `Aptly` = Properly(적절하게)
    - `With all due respect` : 직역 : 모든 존경심을 담아 / 의역 : 외람되지만, 이런 말씀드려서 죄송하지만
    - `Blatantly` : 노골적으로 / 조금 더 순화된 표현 : `bluntly`(직설적으로)

**Example 3**

- 👤 User 4 코멘트
    
    So why in one sentence is it not flask? Just because it requires a command line tool to run?
    
    😡 그렇다면 한 문장으로 Hug는 왜 플라스크 같은 프레임워크가 아닌가요? 실행하려면 커맨드 라인 도구가 필요하기 때문인가요?
    
- 👤 User 1 코멘트
    
    Here's my short answer: hug does not require a command line tool to run. It 1 `allows` ****your APIs to be `exposed` ****over the command line 3 `as well as` ****over HTTP. Flask is a
    framework for making websites / HTTP applications. Hug is a framework for building
    general APIs / microservices on Python that can be exposed to any interface (HTTP, CLI,
    Locally, asyncio) with automatic documentation and validation built in.
    
    짧게 답변 드리겠습니다. hug를 실행하기 위해 커맨드 라인이 필요하지 않습니다. Hug는 HTTP뿐만 아니라 커맨드 라인을 통해 API를 사용하도록 할 수 있습니다. Flaskb 웹사이트 / HTTP 애플리케이션을 만들기 위한 프레임워크입니다. Hug는 Python을 기반으로 모든 인터페이스(HTTP,
    CLI, Locally, asyncio)에 사용될 수 있는 일반적인 API와 마이크로서비스를 만드는 프레임워크로, 자동화된 문서화 및 검증이 내장되어 있습니다.
    
- **주요 표현 분석**
    - `Expose` : IT 엽계에서는 “사용가능하게 하다(make available)”라는 의미로 사용

### Repository Example 2

> **tensorflow/tensorflow**
> 
> 
> Pull Request #56097 - Add CI/CD for ARM64 using GitHub Actions
> 
- 인기 오픈소스 머신러닝 플랫폼, 텐서플로우의 풀 리퀘스트
- Github Action : 깃허브에서 제공하는 CI/CD 플랫폼
- 일반적으로 풀 리퀘스트 제목은 커밋 메시지처럼 동사 원형을 활용한 **명령적 어조**로 간**결하게** 작성

**Example 1**

- 👤 User 1 코멘트
    - `Added Github workflows` to build, test and upload ARM64 pip wheels for Python versions 3.7, 3.8, 3.9 and 3.10
    - Workflow jobs run on `self-hosted` runners `on` AWS Graviton instances.
        
        워크플로우 작업은 AWS Graviton 인스턴스의 자체 호스팅 러너에서 실행됩니다.
        
    - Cl workflow uploads generated pip wheels to GitHub Actions and is triggered for:
        - PR 4 `on` master branch
        - PR on branch name starting with r2.
    - CD workflow uploads 어쩌구 생략
    - Following 18 tests currently failed and are skipped :
        
        tensorflow/python: nn_grad_test_cpu 
        
        …
        
- **주요 표현 분석**
    - 일반적으로 풀 리퀘스트의 첫 코멘트는 **코드 변경 사항**과 **변경 이유**를 요약함. 위 예시에서는 어떤 변경 사항을 제안하는지 중요 항목을 bullet point로 요약
    - `Self-hosted` runners : 여러 단어를 합쳐 새로운 의미를 만들고 명사를 수식하는 경우, 각 단어를 하이픈(-)으로 붙여쓴다.
        
        > **복합 형용사** : 두 개 이상의 단어가 모여 새로운 의미로 사용되는 형용사
        > 
        
        > **hyphenate** : 하이픈으로 단어를 붙여 쓰는 것
        > 
    - AWS와 같은 클라우드에 업로드된 인스턴스 앞에는 전치사 `on` 사용
        
        > BUT 문장 내 전치사는 문맥에 따라 달라질 수 있음. Add more storage to the AWS EC2와 같은 표현도 있음.
        > 
    - **Pull request와 Commit은 Branch 위에 (on) 있다고 표현함.**
        
        반면, Branch는 Repository 안에(in) 있다고 표현함.
        

<aside>
📌 본문의 Add, Build, Test, Generate, Upload, Run, Trigger(작동시키다), Fail, Skip은 매우 자주 등장하는 IT 주요 동사들!

</aside>

## 2. 오픈소스 커뮤니티 “인싸”로 도약하는 인터넷 영어 표현

### LGTM(Look Good To Me)

- Pull Request 코드 리뷰에서 코드에 별다른 문제가 없을 때 사용

> `LGTM`, Approved this PR.
> 

### TL;DR (Too Long; Didn’t Read)

- 너무 길어서 읽지 않는다
- 주로 기술 블로그나 문서에서 자세한 설명 시작 전 요약된 정보 소개할 때 사용

> `TL;DR` : the new build system will be `implemented` next week.
> 

### SSIA (Subject Says It All)

- 제곧내

> `SSIA`. Let me know what you think.
> 

### TBD (To Be Determined)

- 아직 결정되지 않는 내용이 있어 나중에 결정해야 함.

> Set up environment variables (TBD)
> 
> 
> 환경 변수 설정 (추후 다시 논의)
> 

### RFC (Request For Comment)

- 의견 요청

> (RFC) Integrating the new architecture
> 

### AFAIK (As Far As I Know)

- 내가 아는 한

### TBH (To Be Honest)

- 솔직히

### WIP (Work In Progress)

- 진행 중, 진행 중인 작업

> (WIP) Add T&C
> 

### Noob

- 입문자(Newbie)

> I’m noob here. Please help troubleshoot this Issue.
> 
> 
> 여기 처음 왔습니다. 이슈 해결을 도와주세요.
>


## 5. 퇴근 시간을 앞당기는 검색 노하우 4가지

### 1. 핵심 키워드를 “ ”로 묶기

- 해당 키워드를 반드시 포함하는 웹 문서만 검색 가능

### 2. 특정 웹사이트에서만 검색 결과 가져오기

> 에러 메시지를 검색하고 이슈를 해결할 때 : Stack Overflow에 검색
> 

> React의 소스코드를 살펴볼 때 : React Github Repository 확인
> 
- `“site : 도메인”` 키워드 추가하기
    - ex) 스택오버플로우에서 C++ 메모리 유출 문제 해결 방법 검색
        
        “how to fix memory leaks in C++ `site:stackoverflow.com`”
        
    - `site:github.com`과 같이 www 같은 서브 도메인을 명시하지 않으면 [docs.github.com](http://docs.github.com) / www.github.com과 같은 서브 도메인이 모두 검색됨
- 참고사항
    
    1) 검색어 뒤에 `filetype:확장자`를 추가하면 해당 확장자의 파일 검색 가능
    
    2) 검색 키워드에 `*`는 와일드 카드 역할 (ex. What a * day)
    
    3) `-`,`+` 연산자 : 특정 검색어 빼거나 포함한 검색 결과 (ex. “Git hosting solutions -github +gitlab)
 
### 3. 중요 단어만 포함해서, 단순하게
 
- 핵심 키워드로만 검색
- IT 기술 업계에 특화된 단어나 동사를 핵심 키워드로 사용하면 더 전문적인 결과를 얻을 수 있음
- 예시
    - Gradle의 “Command not found : gradle” 에러 검색 시 `Troubleshoot`(이슈나 버그를 해결하다) 동사를 활용하면 양질의 검색 결과 얻기 가능
    - Troubleshoot command not found : gradle error → 많은 검색 결과 / 공식 gradle 문서의 가이드 참고 가능
    - How can I fix command not found : gradle error? → 상대적으로 적은 검색 결과 / gradlew에 대한 검색 결과가 섞여 나옴
 
### 4. 웹페이지가 사용할만한 키워드로 검색하기

- 검색 엔진은 웹페이지 내 키워드를 분석해 자주 인용되거나 검색 키워드를 알맞게 포함하는 웹 페이지를 보여줌
    
    ⇒ 일상적인 표현보다는 웹페이지가 포함할만한 단어로 키워드 구성해야 함
    
- 영어로 정보를 검색할 때 가장 중요한 것 : **내가 찾고자 하는 정보를 영어로 키워드화**
- 문법적으로 어색한 문장이나 잘못된 철자 검색 → 퀄리티 급하락

## 6. 단어 하나로 생사가 갈리는 소프트웨어 법률 영어

- 모든 오픈소스를 무료로 사용할 수 있는 것은 아님
- 제한된 오픈소스를 허가 없이 사용하거나 저작권 고지를 무시하고 프로젝트를 개발할 경우, 엄청난 배상금을 지불하거나 프로젝트를 중단하게 될 수도 있음
- 불필요한 법적 문제를 마주하지 않으려면 주요 소프트웨어 라이선스의 법적 허용 범위를 명확히 알고 있어야 함

### 영어 법률 문서의 특징

1. Shall과 May
    - Shall : 반드시 지켜야 하는 것(Obiligation)
    - May : 허용되는 것(Permission)
2. 일반적으로 법률 문서는 시작 부분에 문서에서 다루게 될 주요 용어를 정의함
    - 첫 번째 글자를 대문자로 쓰고, 용어가 처음 정의되는 부분을 큰 따옴표로 표시
    - 이후 등장하는 용어는 the Sofeware 처럼 큰 따옴표 없이 첫 글자의 대문자만 유지
    - ex) associated documentation files (the “Software”)
        
        이와 연관된 모든 문서 파일들(이하 “소프트웨어”라 한다)
        
    1. 강조가 필요한 부분, 법적 책임 소재를 명시하는 부분은 대문자로 표시
    2. 문장 사이의 관계나 법률 문서의 성격을 강조하기 위해 hereto(여기에), hereafter(이후로), thereof(앞서 언급된 그것의) 같은 대명사형 부사를 사용
    
### Example : MIT License

| 단어 | 뜻 |
| --- | --- |
| Grant | 권한을 부여하다, 인정하다, 허가하다 |
| Without restriction, Without limitation | 제약 없이 |
| Sublicense | 특허를 양도하다, 재실시하다, 2차 라이선스를 부여하다 |
| Persons | (사람, 법인 등의) 독립체들 |
| Subject to | ~을 조건으로, 조건에 따라 |
| As follows / As stated below | 아래와 같이 |
| Condition | 조건 |
| As is | (어떤 조건, 상태에서든) 있는 그대로 |
| Of any kind | 어떤 종류의 ~도 |
| Including but not limited to | (뒤의 대상을) ~를 포함하지만 국한되지 않고 |
| Liable for | ~에 대한 책임이 있는 |

### 기타 본문 단어 & 표현 정리

- Substantial : (양, 가치, 중요성이) 상당한
- Merchantability : 판매 적격성, 상품성
- Noninfringement : 비침회, 비위반, 준법성
- Tort : 불법 행위

### IT 주요 법률 용어

| 단어 | 뜻 |
| --- | --- |
| Terms and conditions | 이용 약관 |
| Privacy policy | 개인 정보 정책 |
| Copyleft | 공개저작권 |
| Patent | 특허권 |
| Trademark rights | 상표권 |
| Attribution | 인용 표시 |
| Redistribution | 재배포 |
| Disclaimer | 표명 진술, 부인(Denial) |
| Derivative Work | 2차 저작물 |
| Liability | 법적 책임, 부채 |


## 7. 품격 있게 비즈니스 이메일을 작성하는 방법

- 영문 이메일은 이메일을 작성하는 당사자인 “We” 또는 “I”를 주어로 활용하는 경우가 많음
- “With Kind Regards” , “Best Wishes”와 같은 맺음말과 이름으로 이메일을 마무리하는 등 한국식 이메일과 구조적으로 다름

### 이메일 예시

```
To : geekyboy@geekhaus.club

From : contact@geekhaus.club

Subject : Welcome to Geek Haus!

Deer Geekboy,
친애하는 Geekboy님께,

We hope this email finds you well.
이 이메일이 잘 전달되기를 바랍니다.

We are thrilled to inform that your application has approved, and you are now officially a memeber of Geek Haus.
귀하의 지원서가 승인되었으며, 귀하는 이제 공식적으로 긱하우스 멤버가 되었음을 알리게 되어 기쁩니다.

We will be hosting a welcome party for our new club members some thime in the nex few weeks. We will send you another email later this week with details regarding the event.
긱하우스는 앞으로 몇 주 안에 새로운 클럽 회원들을 위한 환영 파티를 개최할 것입니다. 이번 주 후반에 이벤트 세부 정보에 대한 이메일을 보내드리겠습니다.

Welcome to the club, we look forward to see you at the party!
클럽에 오신 것을 환영합니다. 파티에서 뵙기를 바랍니다!

Best Regards,
Geek Haus Team
안부를 전합니다,
긱하우스 팀 드림
```

### 1. 제목

- 주로 간략한 문장 또는 명사구 형태로 작성
- Regarding(~에 대하여)으로 시작하기도 함.

```
Request for Feedback | 피드백 요청
Regarding Technical Support | 기술 지원 관련
```

- 이메일 제목은 일반적으로 a, an, the와 같은 관사 생략

```
Inquiry Regarding Schedule | 스케줄 관련 문의
```

- 상대방의 조치가 필요한 경우에는 ‘Action Required’를, 긴급한 요청은 ‘Urgent’를 제목에 붙이기도 함

```
[Action Required] Email Verification | 조치 필요 : 이메일 인증
Urgent Request for Meeting Confirmation | 긴급 회의 확인 요청
```

### 2. 본문

- **1) 호칭**
    - 격식을 갖춘 경우 : Dear + Mr. / Ms. + 성(Last name)
    - 캐주얼한 상황 : Dear + 이름(First name)
    - 호칭의 첫 글자는 대문자로, 호칭 뒤에는 쉼표로 마무리
    
    ```
    Dear Ms. Watson,
    Dear Jane,
    ```
    
    - 특정 지위나 부서를 호칭으로 사용 가능
    
    ```
    Dear HR Manager,
    Dear Frontent team,
    ```
    
    - 수신인이 특정되지 않은 경우에는 “Whom it may concern(연관될 수 있는 사람”이라는 표현 사용
    
    ```
    Dear whom it may concern,
    To whom it may concern,
    ```
    
    - 어느 정도 관계 형성된 상대방과는 바로 인사와 함께 이메일 시작
    
    ```c
    Hi Michelle,
    Hi all,
    Hello Yelim, // Hello는 Hi보다 조금 더 격식을 갖춘 인사말
    ```
    
- **2) 인사**
    - 간단한 안부 인사 또는 소개로 본론 시작
    
    ```c
    I hope you are doing well. (I hope all is well, I hope you are well)
    잘 지내고 있기를 바랍니다.
    
    How are you?
    
    I hope this email finds you well.
    
    My name is Dojoon, and I am the front-end developer for Geek Haus.
    ```
    
    - 상대방과 친분이 있는 경우, 주말이 끝나거나 휴가에서 복귀하는 경우
    
    ```c
    I hope you enjoyed your weekend.
    
    I hope you had a great vacation.
    ```
    
- **3) 본론**
    - 간결함을 중요시, 서문 없이 본론으로 바로 들어가는 경우가 많음
    
    ```
    I am writing in reference to the meeting agenda.
    회의 안건과 관련해서 이메일을 드립니다.
    
    I am writing the request testing for the latest build.
    최신 빌드에 대한 테스트를 요청하기 위해 이메일을 송부합니다.
    
    I am emailing to inform you that we have found some issues with your pull request.
    풀 리퀘스트에 문제를 발견했음을 알려드리기 위해 이메일을 보내드립니다.
    ```
    
- **요청**
    - 정중한 표현이 필요한 경우 : “Could you please~”, “I’d like to request~”, “I would appreciate it if you could~”
    - 지나치게 격식을 갖출 필요가 없는 상황 : “Can you~”, “Please~”

### 3. 마무리

- **1) 마무리 인사**
    
    ```
    Please feel free to contact me for more information.
    추가적인 정보는 저에게 연락주시기 바랍니다.
    
    I look forward to your response. (I look forward to hearing from you.)
    회신 부탁드립니다.
    
    Thank you for your time.
    시간을 내주셔서 감사합니다.
    
    Don't hesitate to contact me for further assistance.
    추가적인 도움이 필요하시면 주저하지 말고 제게 연락 주세요.
    ```
    
- **2) 맺음말**
    - "With Kind Regards", "Best Regards", "Regards", "Sincerely”
    - 여기서 “Regards”는 인사, 축복, 안부 등의 의미로 s를 붙여 복수 형태로 사용
    - 맺음말 끝에는 쉼표 붙이고 이메일 작성자의 이름 또는 부서명 기재
    
    ```
    Sincerely,
    John
    
    Best Regards,
    DevOps team
    ```
    
    - 이미 친분이 있는 상대방 : "Thanks", "Cheers", "Best”처럼 짧고 캐주얼한 맺음말
    
    ```
    Thanks,
    Steve
    
    Best,
    Geek Haus
    ```
    
    - 영문 이메일로 의견이나 요청 사항을 작성할 때에는 작성자나 작성자가 포함된 조직을 명시하는 것이 일반적
    
    ```
    We appreciate your assistance.
    
    I hope everything is going well.
    
    We will not be able to attend the seminar next week.
    
    I am writing in reference to our schedule for this week's meeting.
    ```
    
- **첨부 파일과 관련된 표현**
    - Attach, Attached, Attachement 등으로 표현
    
    ```
    Please find the attached file.
    
    Please refer to the file attached for more information
    자세한 내용은 첨부된 파일을 참조하시기 바랍니다.
    
    I have attached the file for review.
    ```
    
- **리마인더와 관련된 표현**
    - Gentle reminder, Friendly remindeer와 같은 형태 사용
    
    ```
    This is a gentle reminder that your document review is due this Friday.
    문서 검토 마감이 이번 주 금요일이라는 것을 상기시켜드립니다.
    
    Just a friendly reminder that we will having a meeting at 3PM.
    3시에 회의가 있다는 것을 상기시켜 드립니다.
    
    I am following up to check if you were able to take a look at my suggestion from my previous email.
    이전 이메일의 제안을 살펴보셨는지 확인하기 위해 팔로우업 합니다.
    ```
    
- **희소식을 전달할 때 사용하는 표현**
    - Be (thrilled / excited / happy) to + 동사원형
- **거절과 관련된 표현**
    - Regret to, Sorry to(유감이다)
- **감사 표현**
    - “Thank you for~”, “I appreciate~”
    - 좀 더 격식있는 표현 : “Express my (our) gratitude)”
- **양해를 구하는 표현**
    - Apologize, Sorry
    - “Thank you for your patience” : 기다려주셔서 감사합니다 or (앞으로 불편이나 지연이 있을 수 있으니) 양해를 구한다
