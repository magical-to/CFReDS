53. Recover deleted files from USB drive ‘RM#2’.<Br><br>

RM#2라는 USB 드라이브에서 삭제된 파일을 복구하면 된다.<br><br>

위 문제를 해결하기 위해서 FTK Imager를 또 사용해 볼 것이다.<br><Br>

'RM#2' 파일은<br>
https://cfreds-archive.nist.gov/data_leakage_case/data-leakage-case.html<br>
페이지에서 Personal Computer 밑에 있는 Removable Media #2를 다운받으면 된다.<br><br>

![alt text](1.png)<br>
위 이미지는, FTK Imager를 이용해 Raw 이미지를 불러온 것이다. 빨간색으로 표시해둔 곳을 살펴보면, 디렉토리 경로 관련 단서를 발견할 수 있다.<br><br>

![alt text](2.png)<br>
HxD로 해당 파일을 열고, Directory Entry의 시그니쳐인 Hex-Value(78467846), ASCII : xFxF를 검색해서 찾은 결과의 일부이다.<br><br>

\DESIGN\winter*storm.amr, \DESIGN\winter_whether_advisory.zip, \pricing decision\my_favorite_cars.db, \pricing decision\my_favorite_movies.7z, \pricing decision\new_years_day.jpg, \pricing decision\super_bowl.avi, \PROGRESS\my_friends.svg, \PROGRESS\my_smartphone.png, \PROGRESS\new_year_calendar.one, \PROPOSAL\a_gift_from_you.gif, \PROPOSAL\landscape.png, \technical review\diary*#1d.txt, \technical review\diary*#1p.txt, \technical review\diary*#2d.txt, \technical review\diary*#2p.txt, \technical review\diary*#3d.txt, \technical review\diary\_#3p.txt<br><br>

RM#2라는 USB가 포맷이 되어버리기 이전의 폴더와 파일 구조이다.<br><br>

![alt text](3.png)<br>
정리하면, 위 사진과 같다.<br><br>

![alt text](4.png)<br>
AutoPsy 프로그램을 이용해서도 지워진 파일들을 확인해 볼 수 있다.<br><br>

54. What actions were performed for anti-forensics on USB drive ‘RM#2’?
    [Hint: this can be inferred from the results of Question 53.]<br><br>

USB 드라이브 ‘RM#2’에서 **디지털 포렌식 방해(안티 포렌식)**를 위해 어떤 조치가 수행되었는가?를 묻고 있다.<br>
[힌트: 이는 질문 53의 결과를 통해 유추할 수 있다.]<br><br>

빠른 포맷 이전의 일부 디렉터리 항목이 할당되지 않은 영역에 존재한다는 것을 보아, USB 빠른 포맷 기능을 사용했다는 것을 알 수 있다.<br><Br>

USB를 빠른 포맷하게 되면 파일시스템만 재설치하는 과정을 거치고, 모든 영역을 포맷하지 않기 때문에, 비할당 영역에서 이전의 데이터를 발견할 수 있게 된다.<br><br>

1. 파일 시스템의 MFT(마스터 파일 테이블) 또는 FAT(파일 할당 테이블)만 초기화된다.<br>
2. 실제 데이터 영역은 삭제되지 않음 → 즉, 기존의 파일 데이터는 그대로 남아 있지만, 파일 시스템에서 이를 인식하지 못할 뿐이다.<br>
3. 일부 디렉터리 항목(파일 이름, 경로 등)이 삭제되지 않고 할당되지 않은 공간(unallocated space)에 남아 있을 수 있다.<br><br>

4. What files were copied from PC to USB drive ‘RM#2’?<br><br>

PC에서 RM#2라는 USB 드라이브로 어떠한 파일들이 복사가 되었는 지를 묻고 있다.<br><br>

위 파일 목록 중에서 winter_whether_advisory.zip 파일을 점프목록의 RM#2의 경로에서 확인할 수 있다. 수정시각이 생성시각보다 이전인데, 이 말은 즉슨 해당 파일들이 PC에ㅓㅅ USB로 복사되었다는 것을 알 수 있다.
