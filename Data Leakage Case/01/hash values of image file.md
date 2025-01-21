What are the hash values (MD5 & SHA-1) of all images?<br>
Does the acquisition and verification hash value match?<br><br>

간단하게 번역하자면,<br>
모든 이미지의 해시 값(MD5 및 SHA-1)은 무엇인가요?<br>
획득 및 검증 시 해시 값이 일치하나요? 정도가 되겠다.<br><br><br>


FTK Imager를 사용하여 다운받은 문제 파일(https://cfreds-archive.nist.gov/data_leakage_case/data-leakage-case.html)을 넣어준다.<br><br>

![1](https://github.com/user-attachments/assets/5c51989a-9406-47e8-9a23-d8e8acf34d94)<br>
E01만 넣으면 된다.<br><br>

![2](https://github.com/user-attachments/assets/c40d3341-2d8d-47ca-97e5-cbc8bb490118)<br>
해시 값을 얻기 위해서, FTK Imager의 File - Verify drive/image 메뉴를 이용해서 이미지 해시를 검증할 수 있다.<br><br>

![3](https://github.com/user-attachments/assets/18eb603d-a139-4f29-b41e-df4018a84a5f)<br>
위 사진은 이미지 해시의 결과 값이다.<br><br>

![4](https://github.com/user-attachments/assets/79468f60-7f0f-4a79-80a4-575ff1aab640)<br>
FTK Imager의 View 메뉴에서 Properties를 통해 이미지 파일의 stored verification hashes를 비롯한 다양한 속성들을 확인할 수 있다.<br><br>

acquired date : 2015-04-23<br>
acquired on OS : Windows 7<br>
examiner : dForensic_team<br>
