2. What operating system was used on the computer?<br>
3. When was the install date?<br>
4. What is the timezone settings?<br>
5. Who is the registered owner?<br>
6. What is the computer account name?<br>
7. What is the primary domain name?<br>
8. When was the last recorded computer shutdown date/time?<br>
9. How many accounts are recorded (total number)?<br>
10. What is the account name of the user who mostly uses the computer?<br>
11. Who was the last user to logon to the computer?<br><br>

각각, 컴퓨터에서 사용된 운영 체제는 무엇인가?<br>
설치 날짜는 언제인가?<br>
시간대 설정은 어떻게 되어 있나?<br>
등록된 소유자는 누구인가?<br>
컴퓨터 계정 이름은 무엇인가?<br>
기본 도메인 이름은 무엇인가?<br>
마지막으로 기록된 컴퓨터 종료 날짜/시간은 언제인가?<br>
기록된 계정 수(총 개수)는 몇 개인가?<br>
이 컴퓨터를 가장 많이 사용하는 사용자의 계정 이름은 무엇인가?<br>
마지막으로 이 컴퓨터에 로그인한 사용자는 누구인가?를 묻고 있다.<br><br>

우선, Registry를 추출해보려고 한다. Data Leaking Case의 #3번을 참고하면 된다.<br><br>

![alt text](1.png)<br>
이번에는 Autopsy를 적극 기용해보려고 한다.<br>
SCHARDT.001 이미지 파일을 그대로 Add Data Source를 통해 업로드해주면, 위 사진에서 볼 수 있듯이, 데이터 소스 드라이브에 대한 정보를 요약해서 보여주는데, OS가 Microsoft Windows XP라고 나와있다. 따라서 2번에 대한 답은<br> 2. Microsoft Windows XP가 되게 된다. 참고로, 기본 드라이브 폴더에서 boot.ini 파일을 통해서도 확인이 가능하다.<br><br>

3번에서는 설치 날짜를 묻고 있다.<br><br>

OS를 설치한 날짜를 알기 위해서는 위도우 설치 정보가 담겨 있는 레지스트리를 찾아야 한다.<br><br>

Windows 98/ME 버전은 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FirstInstallDateTime<br><br>

Windows NT/XP/Vista/7/10 버전은 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\InstallDate<br>
에서 확인할 수 있다.<br><br>

Windows NT에서 찾아야 하는데 Windows 눌러놓고 헤맸다;<br><br>

![alt text](2.png)<br>
위 사진처럼 InstallDate의 Value가 0x41252e3b인 것을 확인할 수 있다.<br><br>

이를 10진수로 바꾸게 되면, 1092955707이 되며 시간 형태로 바꾸게 되면,<br>
2004년 8월 20일 16시 48분 27초 (KST)이다.<br><br>

4번에서는 시간대 설정이 어떻게 되어있는가를 묻고 있다.<br><br>

Timezone은 3번 문제에서도 알 수 있듯이,<br>
HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\TimeZoneInformation<br>
해당 레지스터에서 확인이 가능하다.<br><br>

![alt text](image.png)<br>
위 사진이 해당 경로이며, 시간대 설정이 Central Standard Time으로 되어있는 것을 확인할 수 있었다.<br><br>
