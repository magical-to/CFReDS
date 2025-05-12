Identify the partition information of PC image.<br><br>

파티션 정보는 MBR에 저장되어 있다.<br>
https://m.blog.naver.com/kangyh5/221846708215(참고)<br><br>

![1](https://github.com/user-attachments/assets/981489b1-7c8d-4a91-af08-6c82e794cc5d)<br>
bytes per sector는 512이며,<br>
partition #1은<br>
Boot flag : 80 / File system type : 07 / LBA : 00 00 08 00 / SIZE : 00 03 20 00<br>
부트 파티션 / NTFS / 시작위치 : 0x8000 sector(=0x1000000 bytes) / 크기 : 0x32000 sector(=0x6400000 bytes = 104857600 bytes = 100MB)<br><br>

partition #2는<br>
Boot flag : 00 / File system type : 07 / LBA : 00 03 28 00 / SIZE : 02 7C D0 00<br>
부트 파티션 X / NTFS / 시작위치 : 0x32800 sector(=0x6500000 bytes) / 크기 : 0x27CD000 sector (=0x4F9A00000 bytes = 21367881728 bytes = 20378MB)<br><br>

요롷게 정리할 수 있겠다.<br>
