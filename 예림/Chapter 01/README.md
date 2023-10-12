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
