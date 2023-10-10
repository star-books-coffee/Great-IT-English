### 1. Git으로 세련되게 협업하는 5가지 방법

- 전 세계적으로 통용되는 커밋 메시지
관습 : Conventional Commits
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
