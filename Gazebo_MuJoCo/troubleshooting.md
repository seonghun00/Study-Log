## 바로가기 목차
* [에러 1: terminal (패키지 오타)](#dockerfile-패키지-설치-오타-및-줄바꿈-에러)
* [에러 2: tree\ (줄바꿈 공백 누락)](#에러-2-역슬래시-뒤-공백-누락)
* [에러 3: gazebo11 (저장소 누락)](#에러-3-gazebo11-패키지-인식-불가)

### Dockerfile 패키지 설치 오타 및 줄바꿈 에러
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| <img width="350" alt="image" src="https://github.com/user-attachments/assets/8babbc64-1625-4b32-a71d-89bb1541ddaa" /> | **🚨 에러 1: 존재하지 않는 패키지명 입력**<br><br>• **문제 현상:** `terminator` 대신 `terminal`로 오타 입력<br>• **에러 로그:** `E: Unable to locate package terminal`<br>• **해결 방법:** **`terminator`**로 철자 수정<br><br><hr><br>**🚨 에러 2: 역슬래시 뒤 공백 누락**<br><br>• **문제 현상:** `tree` 뒤에 공백 없이 `\`를 붙여 아랫줄과 합쳐짐 (`treegit`으로 인식)<br>• **에러 로그:** `... terminal \ttree git ...`<br>• **해결 방법:** 띄어쓰기를 추가해 **`tree \`** 형태로 수정 |

---

### Gazebo Classic 공식 저장소 누락 에러 (예시)
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| <img width="350" alt="image" src="[새로운 에러 사진 주소]" /> | **🚨 에러 3: gazebo11 패키지 인식 불가**<br><br>• **문제 현상:** Ubuntu 22.04 순정 환경에서 Gazebo Classic 설치 경로를 찾지 못함<br>• **에러 로그:** `E: Unable to locate package gazebo11`<br>• **해결 방법:** Dockerfile에 OSRF 공식 가제보 저장소를 등록하는 코드 추가 |
