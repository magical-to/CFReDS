Explain installed OS information in detail.(OS name, install date, registered owner...)<br><br>

윈도우 OS 정보는 HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion<br>
경로에 있다.<br><br>

이미지 파일 내 레지스트리를 획득하기 위해 Arsenal Image Mounter, WinHex와 분석하기 위해 Registry Explorer를 사용할 것이다.<br><br>

![alt text](1.png)<br>
다음은 Arsenal Image Mounter를 사용해서 이미지 마운팅을 한 모습이다.<br><br>

![alt text](2.png)<br>
다음과 같이 WinHex에서 Tools 메뉴에서 Open disk를 선택해 Arsenal Virtual를 클릭한다.<br><br>

![alt text](3.png)<br>
다음과 같이 FTK Imager로 분석을 해도 상관없다. 어찌 되었든, \Windows\System32\config에서 components, system, sam, security, software 파일을 추출한다.<br><br>

![alt text](4.png)<br>
이렇게 뽑아내면 된다!<br><br>

![alt text](5.png)<br>
Registry Explorer에서 File - Load Hive를 통해 5개의 파일을 전부 로드 하면 다음과 같은 화면을 볼 수 있다.<br><br>

![alt text](6.png)<br><br>
ProductName은 Windows 7 Ultimate이며 InstallDate는 1427034866인데 unix time 기준이므로, Sun Mar 22 2015 23:34:26 UTC+0900 (한국 표준시)이다.<br>
RegisteredOwner은 informant이다.<br><br>
