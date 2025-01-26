When did the suspect burn CD-R?<br>
[Hint: It may be one or more times.]<br><br>

용의자는 언제 CD-R을 burn 했는지 묻고 있다.<br>
[힌트: 한 번 이상일 수 있습니다.]<br><br>

우선, 레지스트리를 분석 해보자.<br>
분석할 레지스트리 경로는 다음과 같다.<br>
HKU\informant\Software\Microsoft\Windows\CurrentVersion\Explorer\CD Burning<br><br>

Registry Explorer의 Last write timestamp 시간 값을 UTC+0이므로<Br>
2015-03-24 16:53:16(UTC-4)에 CD를 burning type 1, 'USB 플래시 드라이브에서처럼 사용'을 선택하였다.<br><br>

시스템 이벤트 로그(133)를 확인하는 방법, NTFS Log Tracker를 이용해 파일시스템 로그를 확인하는 방법도 존재한다.<br><br>
