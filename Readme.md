# SAE(SIC Assembly Editor for MacOS)
이것은 sic.zip에서 제공된 SICEditor.exe를 MacOS 용으로 만든 것입니다.
**Windows 용으로도 개발**하고 있습니다.

Assembly나 Simulate 기능 등 SICEditor.exe에서 이제 지원하지 않는 기능도
다시 살려서 개발하였습니다.

설치 방법과 사용 방법은 아래 목차부터 봐주시기 바랍니다.
각 목차 제목을 클릭하시면 하이퍼링크로 연결됩니다.

# 목차
1. [설치 방법](#1-설치-방법)  
   1.1. [폴더 배열 방법](#11-폴더-배열-방법)  

2. [사용 방법](#2-사용-방법)  
   2.1. [Main Window](#21-Main-Window)  
      2.1.1. [Source Tab](#211-Source-Tab)  
      2.1.2. [Object Tab](#212-Object-Tab)  
      2.1.3. [Listing Tab](#213-Listing-Tab)  
      2.1.4. [Working Tab](#214-Working-Tab)  
      2.1.5. [상단 버튼](#215-상단-버튼)  
         - [Refresh](#Refresh)  
         - [Save](#Save)  
         - [Assemble](#Assemble)  
         - [Simulate](#Simulate)  
         - [Close](#Close)  

   2.2. [Simulate Window](#22-Simulate-Window)  
      2.2.1. [저장 경로](#221-저장-경로)  
      2.2.2. [DOSBox 상태](#222-DOSBox-상태)  
      2.2.3. [명령어 매크로](#223-명령어-매크로)  
      2.2.4. [스크린샷](#224-스크린샷)  
      2.2.5. [상단 버튼](#225-상단-버튼)  
         - [Refresh](#Refresh)  
         - [Save](#Save)  
         - [Init](#Init)  

   2.3. [권한 설정](#23-권한-설정)  
      2.3.1. [access files](#231-access-files)  
      2.3.2. [Screen Recording](#232-Screen-Recording)  
      2.3.3. [Accessibility Access](#233-Accessibility-Access)

# 1. 설치 방법

## 1.1. 폴더 배열 방법
이 레포지토리 전체를 ZIP file로 다운로드하여 주십시오.  
지금은 folder로 보이는데, 압축을 풀면 'SIC Assembly Editor.app'이 나올 겁니다.  
이 .app file을 수업에서 제공받은 sic.zip을 푼 장소에 위치시켜 주십시오.  
그리고 '~/Applications' 위치에 'DOSBox.app'을 위치시켜 주십시오.

# 2. 사용 방법

우선 이 프로그램을 실행하시면 권한 설정을 하라는 창이 뜹니다.  
이는 [2.3.1. access files](#231-access-files)를 참고하여 주시기 바랍니다.

## 2.1. Main Window
앱을 실행했을 때 띄워지는 창을 Main Window라고 하겠습니다.
이하는 본 Main Window에 대한 각 기능 설명입니다.

### 2.1.1. Source Tab
![SourceTab](https://github.com/user-attachments/assets/011d714b-9326-4608-8e83-e5a2c895dc56)
Source Tab에서는 SRCFILE을 조회하고 편집할 수 있습니다.

각 칸을 움직이는 방법은 아래와 같습니다.  
Tab을 누를 시 오른쪽 칸으로 이동(맨 오른쪽 칸이면 아랫줄로, 맨 오른쪽이고 맨 아랫칸이면 한 줄 생성)  
Shift+Tab을 누를 시 왼쪽 칸으로 이동(맨 왼쪽 칸이면 윗줄로)  
Enter을 누를 시 아랫 칸으로 이동(맨 아랫칸이면 한 줄 생성)  
Shift+Enter을 누를 시 윗칸으로 이동(맨 윗칸이면 움직이지 않음)  

**칸을 편집하신 후, 꼭 다른 칸으로 이동하셔야 저장이 됩니다.**  
예를 들어 (0, 0) 칸을 수정한 다음,  
(0, 0)에서 키보드 커서가 깜빡일 때 Save 버튼을 누르면...  
(0, 0)칸의 수정 사항은 ${\bf{\color{red}SRCFILE에\ 저장되지\ 않}}$습니다.

마지막으로, **오타 검출 기능**을 넣어두었습니다.  
만일 SIC/EX의 operation이 아닌 operation을 입력하였다면 빨간 글씨로 바뀝니다.  
operation을 입력하다보면 오타가 입력될 수 있는데, 이를 쉽게 볼 수 있도록 하였습니다.

이하는 표 우측 상단의 버튼 4개의 설명입니다.  

- **Append 버튼**  
Append 버튼을 클릭할 시  
표의 맨 마지막에 한 줄을 추가합니다.

- **Insert 버튼**  
Insert 버튼을 클릭할 시  
현재 선택된 Cell의 줄 바로 밑에 한 줄을 추가합니다.

- **Delete 버튼**  
Delete 버튼을 클릭할 시  
현재 선택된 Cell 한 줄을 삭제합니다.

- **Clear 버튼**  
Clear 버튼을 클릭할 시  
작성한 표 전체가 삭제됩니다.  
SRCFILE은 삭제되지 않습니다.

### 2.1.2. Object Tab
![ObjectTab](https://github.com/user-attachments/assets/dde09603-acbb-4a3b-80e4-772024ca7c99)
Object Tab에서는 DEVF2를 조회할 수 있습니다.  
다른 기능은 없습니다.

### 2.1.3. Listing Tab
![ListingTab](https://github.com/user-attachments/assets/642eeea3-62a0-45b3-9c6d-0c3e1250dd40)
Listing Tab에서는 LISFILE을 조회할 수 있습니다.  
다른 기능은 없습니다.

### 2.1.4. Working Tab
![WorkingTab](https://github.com/user-attachments/assets/edce99f5-d78e-482b-8595-90ab70bb6e6a)
Working Tab에서는 INTFILE을 조회할 수 있습니다.  
다른 기능은 없습니다.

### 2.1.5. 상단 버튼
상단 버튼, 이하 Refresh, Save, Assemble, Simulate, Close 버튼 총 5개의 기능 설명입니다.

#### Refresh
Refresh 버튼을 누를 시  
SRCFILE, DEVF2, LISFILE, INTFILE을 새로 불러옵니다.

만일 Assemble 등을 실행해서 DEVF2, LISFILE, INTFILE의 변화를 보고 싶으시다면  
Refresh 버튼을 꼭 누르셔야 바뀝니다.

#### Save
Save 버튼을 누를 시  
지금까지 바뀐 SRCFILE을 저장합니다.

#### Assemble
Assemble 버튼을 누를 시  

(1) 만일 DOSBox가 열려있지 않은 경우
DOSBox를 실행하여 SICASM.exe를 실행하고,  
일련의 과정(del devf2, ren objfile devf2, l2u devf2 등)을 자동으로 수행한 뒤,  
DOSBox를 닫습니다.

(2) 만일 DOSBox가 이미 열려있는 경우
x 디스크를 할당하여 SICASM.exe를 실행하고,  
일련의 과정(del devf2, ren objfile devf2, l2u devf2 등)을 자동으로 수행한 뒤,  
x 디스크 할당을 해제하고 DOSBox를 종료하지는 않습니다.

#### Simulate
Simulate 버튼을 누를 시  
Simulate Window와 DOSBox를 엽니다.  
Simulate Window는 아래 [목차](#Simualte-Window)를 참고하여 주시기 바랍니다.  
DOSBox를 열어서 현재 .app file이 위치한 디렉토리 주소로 C 디스크를 할당한 뒤
C:로 이동하고 명령어를 입력할 준비를 합니다.

#### Close
SRCFILE에 변경된 내용이 있다면 저장할 것인지 묻는 창을 띄우고,  
변경된 내용이 없다면 창을 닫습니다.

## 2.2. Simulate Window
![Simulate Window](https://github.com/user-attachments/assets/3419b72f-07e3-4059-bb7a-257661ea53e8)
[Main Window](#Main-Window)에서 Simulate 버튼을 누를 시 보이는 Simulate Window에 대한 설명입니다.

### 2.2.1. 저장 경로
sic folder의 위치를 명시하는 곳입니다.

Init 버튼을 누르면, 현재 'SIC Assembly Editor.app'이 위치한 디렉토리를 보여줍니다.  
옆의 folder icon을 눌러 직접 경로를 지정하실 수도 있습니다.  
혹은 회색 박스를 더블클릭하여 내용을 수정하실 수 있습니다.  

### 2.2.2. DOSBox 상태
DOSBox가 켜져있나 확인하는 곳입니다.  
Simulate Winodw 내 각각의 버튼을 누를 때 또는 새로고침 버튼을 누를 때마다 확인하는 과정을 거칩니다.

### 2.2.3. 명령어 매크로
각각의 명령어를 실행할 수 있습니다.  
각각의 명령어는 회색 박스를 더블클릭하여 수정하실 수 있습니다.  
$는 명령어 구분자로, 'mount c ~/sic/sic'와 'C:'를 매크로로 하고 싶다면,  
'mount c ~/sic/sic$C:'와 같은 형식으로 수정하시면 됩니다.  
$로 구분된 명령어는 엔터를 치고, 0.5초를 기다린 후 실행됩니다.

${\bf{\color{red}주의사항}}$  
명령어가 실행되면 DOSBox 창이 포커싱(선택)되는데, 이를 유지해주시기 바랍니다.  
명령어 매크로를 실행하신 후 다른 프로그램을 선택하면 그 프로그램의 입력 박스에 명령어가 입력됩니다.  
고로, 명령어 매크로를 실행하신 후 매크로가 끝날 때까지 대기 부탁드립니다.

그리고, 이 기능을 처음 실행하시면 권한 설정을 하라는 창이 뜹니다.  
이는 [2.3.3. Accessibility Access](#233-Accessibility-Access)를 참고하여 주시기 바랍니다.

### 2.2.4. 스크린샷
스크린샷은 현재 DOSBox 창을 캡쳐하는 기능입니다.  
스크린샷 버튼을 누르면 제목을 입력하라는 창이 나오는데 거기에 제목을 입력해주시면,  
DOSBox 창을 캡쳐하여 YYYYMMDDHHMMSS_{제목}.png의 이름으로 저장합니다.  
저장되는 위치는 'SIC Assembly Editor.app'이 위치한 디렉토리에 ScreenShots란 폴더가 만들어질 겁니다. 그곳에 저장됩니다.

이 기능을 처음 실행하시면 권한 설정을 하라는 창이 뜹니다.  
이는 [2.3.2. Screen Recording](#232-Screen-Recording)을 참고하여 주시기 바랍니다.

스크린샷 버튼 밑에 리스트 형식으로 캡쳐된 파일이 보일텐데, 요소를 **클릭**하면 옆 Screenshot Preview 부분에 보여집니다.  
마우스로 클릭하셔야 보입니다. 방향키 위아래로 움직여도 바뀌지 않습니다.

### 2.2.5. 상단 버튼

#### Refresh
Refresh 버튼은 Save된 명령어 매크로들을 불러오는 기능입니다.  
프로그램 내부에 저장된 명령어들을 불러옵니다.

#### Save
Save 버튼은 현재 창에 입력된 매크로들을 저장하는 기능입니다.  
프로그램 내부에서 저장됩니다.

#### Init
Init 버튼은 명령어 매크로들을 초기화하는 기능입니다.  
저장 경로를 알아서 가져오고, 1부터 7까지 명령어들을 기본 상태로 세팅합니다.  
프로그램을 처음 실행하시면 PLEASE CLICK INIT BUTTON이라고 뜰텐데,  
말 그대로 Init 버튼을 클릭하시면 알아서 세팅됩니다.

## 2.3. 권한 설정

### 2.3.1. access files
![access files](https://github.com/user-attachments/assets/eac419f8-b5a0-4249-8c8b-a204ac401ca7)
프로그램을 실행할 때 SRCFILE, LISFILE, INTFILE 등을 불러오는 기능이 실행됩니다.  
이에 따라 file에 access하는 권한이 필요합니다.

### 2.3.2. Screen Recording
![screen recording](https://github.com/user-attachments/assets/7d645bc0-b38a-4051-8e93-0863bc92e906)
화면을 캡쳐할 때 Screen Recording 권한이 필요합니다.  
이 권한을 세팅하면 프로그램을 다시 껐다 켜야하는데, 껐다 키면 됩니다.

### 2.3.3. Accessibility Access
![Accessibility Access](https://github.com/user-attachments/assets/7ee0f8a8-0bdb-468b-a327-78b74dae286f)
명령어 매크로를 입력할 때 필요한 권한입니다.  
