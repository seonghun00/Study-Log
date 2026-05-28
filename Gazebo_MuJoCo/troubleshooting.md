### 📌 바로가기 목차

#### 1. [BUILD] 환경 구축 및 패키지 설치
* [ERROR 1: Dockerfile 패키지 설치 오타 및 줄바꿈 에러](#dockerfile-패키지-설치-오타-및-줄바꿈-에러)
* [ERROR 2: colcon 명령어를 찾을 수 없음](#colcon-명령어를-찾을-수-없음)

#### 2. [RUN] 컨테이너 및 소스코드 실행
* [ERROR 1: URDF 파일 경로 불일치](#urdf-파일-경로-불일치)

#### 3. [LINK] GUI 화면 표시 및 로봇 연동
* *(추후 에러 발생 시 추가 예정)*

---

### 1. [BUILD] 환경 구축 및 패키지 설치

#### Dockerfile 패키지 설치 오타 및 줄바꿈 에러
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| <img width="350" alt="image" src="https://github.com/user-attachments/assets/8babbc64-1625-4b32-a71d-89bb1541ddaa" /> | **🚨 ERROR 1: 존재하지 않는 패키지명 입력**<br><br>• **문제:** `terminator` 대신 `terminal`로 오타 입력<br>• **로그:** `E: Unable to locate package terminal`<br>• **해결:** **`terminator`**로 철자 수정<br><br><hr><br>**🚨 ERROR 2: 역슬래시 뒤 공백 누락**<br><br>• **문제:** `tree` 뒤에 공백 없이 `\`를 붙여 아랫줄과 합쳐짐 (`treegit`으로 인식)<br>• **로그:** `... terminal \ttree git ...`<br>• **해결:** 띄어쓰기를 추가해 **`tree \`** 형태로 수정 |

#### colcon 명령어를 찾을 수 없음
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| *(터미널 캡처 사진)* | **🚨 ERROR 3: colcon 명령 미설치**<br><br>• **문제:** ROS2 빌드 툴인 `colcon`이 컨테이너에 설치되어 있지 않음<br>• **로그:** `bash: colcon: command not found`<br>• **해결:** 터미널에 아래 명령어를 실행하여 설치<br>`pip install -U colcon-common-extensions` |

---

### 2. [RUN] 컨테이너 및 소스코드 실행

#### urdf 파일 경로 불일치
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| <img width="719" height="205" alt="image" src="https://github.com/user-attachments/assets/6b4e2c0e-d5bd-48c5-9b84-f3ec29e55905" /> | **🚨 ERROR 1: URDF 경로 오류**<br><br>• **문제:** 실제 위치(`mujoco_ws`)와 코드 내 경로(`ros2_ws`)가 다름<br>• **로그:** `No such file or directory`<br>• **해결:** 코드를 **`mujoco_ws`**로 수정 |

---

### 3. [LINK] GUI 화면 표시 및 로봇 연동
*(추후 에러 발생 시 추가 예정)*
