# 비주얼노벨 스타일 대화 시스템

일반적인 SCG 및 표정 변화를 지원하는 Unity 비주얼노벨 대화 시스템입니다.

![Demo](https://github.com/user-attachments/assets/da79c4ed-9d6a-47b3-809e-e70bf87b5d93)

<br>
<br>

## 📦 설치 방법

### 방법 1. Dialogue Box 디렉터리 복사

1. 이 레포지터리의 `Dialogue Box` 디렉터리를 다운로드합니다.
2. 다운로드한 디렉터리를 사용할 프로젝트의 Assets/ 하위에 복사합니다.

<br>

### 방법 2. unitypackage 다운로드
1. 이 레포지터리의 `Dialogue Box.unitypackage`를 다운로드합니다.
2. Unity 상단 메뉴의 `Assets` > `Import Package` > `Custom Package...`를 통해 임포트합니다.

<br>
<br>

## 🚀 사용 방법
1. **`Demo` > `Scenes` > `Demo` 씬을 열어 기능을 확인할 수 있습니다.**
2. **`Demo` > `Runtime` > `Data` > `Dialogue Settings`를 통해 쉽게 설정할 수 있습니다.**
3. **다양한 데이터 로드 방식을 지원하며, 기본적으로 `.csv` 파서를 내장하고 있습니다.**
    - Unity 상단 메뉴의 `Tools` > `Dialogue Box`를 참조해주세요.
4. **`.csv` 파일 및 경로를 수정하고 싶은 경우에는 다음 경로의 파일을 확인해주세요.**
    - 캐릭터: `Runtime` > `Import` > `Character` > `CSV` > `CharacterImportMenu.cs`
    - 대화 및 대사: `Runtime` > `Import` > `Dialogue` > `CSV` > `DialogueImportMenu.cs`
5. **기본적으로 SCG는 SO를 통하여 직접 대입하도록 구성되어 있습니다.**
    - 추가적으로 `Resource` 또는 `Addressables`를 통해 이를 확장시킬 수 있습니다. 

<br>

하나의 대화는 여러 개의 노드로 구성됩니다.   
노드의 종류에는 `LINE`, `CHOICE`, `JUMP`, `END`가 있습니다.

- `LINE`: 일반적인 대화 구성 노드 타입
- `CHOICE`: 분기점 구성 노드 타입
- `JUMP`: 특정 노드로의 이동 타입
- `END`: 대화 종료 노드 타입

<br>
<br>

## ⚙ 설정 옵션
1. **타이핑 효과 설정**
    - 타이핑 효과 사용 여부(Enable typing effect)
    - 1초에 출력할 문자의 수(Typing seconds per character)
    - 타이핑 스킵 허용 여부(Typing Skip Allowed)
    - 주의)) 타이핑 효과를 사용하지 않으면 하위 설정들은 무시됩니다.
2. **입력 시스템 설정**
    - 키보드 입력을 이용한 대화 진행 여부(Allow keyboard input)
    - 대화 진행 키 설정[관용적으로 `Space`를 자주 사용합니다.](Advance Action Reference)
    - 선택지 이동 키 설정[관용적으로 `uparrow`, `downarrow`를 자주 사용합니다.](Selection Action Reference)
3. **대화 자동 진행 설정**
    - 대화 자동 진행 여부(Enable Auto Advance)
    - 자동 진행까지 대기하는 시간(Auto Advance Delay)

<br>
<br>

## 📝 참고 사항
- 기본 폰트는 `exqt.ttf`를 사용하고 있습니다.
- CSV 형식은 `Demo` > `CSV` 경로의 `.csv` 파일과 같은 형식을 사용해야만 합니다.
- CSV가 아닌 방식을 통해 데이터를 로드할 경우, `IDialogueRawSource` 또는 `ICharacterRawSource`를 구현해야 합니다.
- 본 패키지는 개인 개발 목적으로 제작되었으며, 자유롭게 사용 가능합니다.
