# Introduction to Metaverse 
### Week1 : Introduction to Unity


### 1. Installation and Tutorial
- Visual Studio Community에서 '.NET 데스크톱 개발'과 'Unity를 사용한 게임 개발' Workload 설치
- Unity Hub 및 Unity Editor 설치
- 3D(Built-in Render Pipeline) Project 생성
- Cube Object 생성
  - Rigidbody Component 추가
- MonoBehavior Script(C#) 생성
  - Cube에 Drag and Drop
  - Script에 아래 Code 추가
```CS

using System.Runtime.InteropServices;
using UnityEngine;
public class NewMonoBehaviourScript : MonoBehaviour
{
    public Rigidbody myRigidbody;


    void Start() 
    { 
        myRigidbody.AddForce(0, 500, 0); 
    }
    void Update() 
    { 

    }
}

```
- Unity Editor에서 `Play` Button 클릭하면 움직이는 Cube 확인 가능

### 2. Unity Editor Interface
#### Scene
- Game World를 관리하는 단위
- Scene은 하나의 Game World, 하나의 Map, 하나의 Game Level에 대응
- 현재 활성화 된 Scene 창에 존재하는 Game Object들을 시각적으로 활성화하여 볼 수 있음
#### Hierarchy
- 현재 Scene에 존재하는 모든 Object를 리스트로 보여줌
#### Inspector
- 현재 선택한 Game Object 혹은 Asset에 대한 상세 정보
- 선택된 Game Object에 붙어있는 Component들이 표시됨
  - Object: 게임 세상 속에 존재하는 사물
  - Component: Object에 붙어서 해당 Object가 어떤 동작을 할 수 있는 기능을 부여하는 요소
#### Game
- Game이 시작되었을 때, 플레이어에게 연출되는 화면
#### Project
- 현재 Project에서 사용한 모든 Package와 Asset을 표시
- Game에서 사용된, 또는 사용될 수도 있는 모든 소품들을 보관하는 창고 역할
- Assets
  - Project에 사용된 모든 파일과 폴더
- Packages
  - 외부 모듈
  - Read-only
  - Assets 폴더로 Drag and Drop 해서 편집해야 함

#### Console
- 개발자들에게 유용한 정보를 Text로 표시

#### Play Button
`Ctrl+P`

- ▶️: Play
  - Game이 Run-time 상태가 됨
  - Scene이 활성화되며 Object들이 기능에 따라 동작
  - Play 동작 중에 변경한 사항들은 반영되지 않음음

- ⏸️: Pause
  - Play 중에 누르면 Object가 동작하는 것을 잠시 멈출 수 있음
  - Pause를 누르고 나서 `Play` 버튼을 누르면 시작됨과 동시에 멈춤
  - 이 상태에서 ⏯️`Step` 버튼을 누르면 한 Frame씩 Game이 진행 됨됨
  
#### RigidBody
- Object에 물리 기능을 추가하는 Component
  
#### Corrider
- Object 표면을 감지하기 위한 경계계