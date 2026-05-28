### 📌 바로가기 목차

* [ERROR 1: colcon 명령어를 찾을 수 없음](#colcon-명령어를-찾을-수-없음)
* [ERROR 2: 특정 패키지만 골라서 빌드하고 싶을 때](#특정-패키지만-골라서-빌드하고-싶을-때)

---

### 📂 에러 사항 분석 및 해결 본문

#### colcon 명령어를 찾을 수 없음
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| *(터미널 캡처 사진)* | **🚨 ERROR 2: colcon 명령 미설치**<br><br>• **문제:** ROS2 빌드 툴인 `colcon`이 컨테이너에 설치되어 있지 않음<br>• **로그:** `bash: colcon: command not found`<br>• **해결:** Dockerfile의 4번 패키지 목록에 **`python3-colcon-common-extensions \`** 추가 후 이미지 재빌드 |

#### 특정 패키지만 골라서 빌드하고 싶을 때
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| *(터미널 빌드 화면 캡처)* | **🚨 ERROR 3: 특정 패키지 선택 빌드 필요**<br><br>• **문제:** 전체 패키지를 다시 빌드하는 데 시간이 너무 오래 걸리거나 특정 패키지만 수정됨<br>• **로그:** *(전체 빌드로 인한 시간 지연 및 병목)*<br>• **해결:** 전체 빌드 대신 아래 명령어로 원하는 패키지만 지정하여 빌드<br>`colcon build --packages-select [패키지명]` |
