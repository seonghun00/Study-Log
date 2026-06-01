### 📌 바로가기 목차

* [ERROR 1: colcon 명령어를 찾을 수 없음](#colcon-명령어를-찾을-수-없음)
* [ERROR 2: 특정 패키지만 골라서 빌드하고 싶을 때](#특정-패키지만-골라서-빌드하고-싶을-때)

---

### 📂 에러 사항 분석 및 해결 본문

#### colcon 명령어를 찾을 수 없음
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| <img width="408" height="31" alt="colcon_command_not_found" src="https://github.com/user-attachments/assets/153680ad-106b-4867-9703-b9fc53f42812" /> | **🚨 ERROR 1: colcon 명령 미설치**<br><br>• **문제:** ROS2 빌드 툴인 `colcon`이 컨테이너에 설치되어 있지 않음<br>• **로그:** `bash: colcon: command not found`<br>• **해결:** 터미널에 아래 명령어를 실행하여 설치<br>`pip install -U colcon-common-extensions` |

#### 특정 패키지만 골라서 빌드하고 싶을 때
| 에러 화면 (Error Image) | 에러 사항 분석 및 해결 방법 (Description & Solution) |
| :---: | :--- |
| *(터미널 빌드 화면 캡처)* | **🚨 ERROR 2: 특정 패키지 선택 빌드 필요**<br><br>• **문제:** 전체 패키지 빌드 중 특정 패키지에서 에러가 발생하면 원인 파악이 어렵고 컴파일 시간이 오래 걸림<br>• **로그:** `Failed   <<< [package_name]` 및 전체 빌드 중단 메시지 발생<br>• **해결:** 전체 빌드 대신 아래 명령어로 코드가 수정되거나 변경된 특정 패키지만 골라 빌드하여 효율적으로 해결<br>`colcon build --packages-select [패키지명]` |
