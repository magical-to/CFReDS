10. What applications were installed by the suspect after installing OS?<br>
용의자가 운영체제를 설치한 이후에 설치한 애플리케이션은 무엇인가를 묻고 있다.<br><br>

64비트 응용프로그램 설치기록의 레지스트리 경로는 다음과 같다.<br>
HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\~<br>
![image](https://github.com/user-attachments/assets/ffb13344-37d2-437e-af91-e385a6457462)<br>
위의 그림과 같이 약 5개의 프로그램이 설치됨.<br><br>

32비트 응용프로그램 설치기록의 레지스트리 경로는 다음과 같다.<br>
HKLM\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall\~<br>
![image](https://github.com/user-attachments/assets/2b3e6dfa-f840-48c1-a9df-78121a4cfa4d)<br><br>


11. List application execution logs.<br>
(Executable path, execution time, execution count...)<br>
애플리케이션 실행 로그를 나열하라.<br>
(실행 파일 경로, 실행 시각, 실행 횟수 등 포함)<br><br>

사용자가 실행한 GUI 기반 프로그램의 실행 횟수, 마지막 실행 시간 등을 저장하는 레지스트리<br>
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist<br><br>

MUICache<br>
HKEY_CURRENT_USER\Software\Microsoft\Windows\ShellNoRoam\MUICache<br>
HKEY_CLASSES_ROOT\Local Settings\Software\Microsoft\Windows\Shell\MUICache<br><br>

AppCompatCache<br>
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\AppCompatCache<br><br>

RecentDocs<br>
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs<br><br>

RunMRU<br>
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\RunMRU<br><br>

