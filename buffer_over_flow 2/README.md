<img width="1368" height="1385" alt="image" src="https://github.com/user-attachments/assets/d88b2fce-e823-48eb-b05f-035cf8080bb4" />

# 1.Find bug

<img width="2364" height="778" alt="image" src="https://github.com/user-attachments/assets/e4e3d8e3-6359-4cc5-b0d8-290a39163b7f" />

Đi vào vuln ta thấy : 

<img width="829" height="225" alt="image" src="https://github.com/user-attachments/assets/9c6cd402-f5de-422e-a7ab-0cc9c8a8878c" />

Vậy là có lỗi bof ở gets 

# 2.Idea:

Ta thấy có hàm win, đi vào hàm win 

<img width="2249" height="813" alt="image" src="https://github.com/user-attachments/assets/61cd896f-ac3b-4f49-87a7-7102263c2f8a" />

Thấy check 2 arg nếu giống thì in flag 

-> Vậy ta sẽ overwrite saved RIP, redirect to win với 2 arg giống như yêu cầu -> get flag

# 3.Exploit:

Tìm offset rồi redirect to win nhưng trước khi truyền argv `vẫn phải thêm return address` 

<img width="552" height="124" alt="image" src="https://github.com/user-attachments/assets/000eec58-8b79-4c55-8590-f38455b020bc" />

Do stack layout

<img width="432" height="958" alt="image" src="https://github.com/user-attachments/assets/85fbb914-85b7-4f5c-954f-47d279728cd0" />


### Script : 

<img width="1150" height="1377" alt="image" src="https://github.com/user-attachments/assets/001cd2f9-131e-4af4-ac3b-c50be6b4eef3" />

# 4. Get Flag

<img width="2541" height="1214" alt="image" src="https://github.com/user-attachments/assets/6e14b47c-5685-4887-b4b4-be5631e01008" />
