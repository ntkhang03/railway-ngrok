# Railway-Ngrok
Sử dụng Ngrok để thâm nhập vào mạng nội bộ của Railway Docker để sử dụng ubuntu

## 1/ Đăng ký tài khoản railway & ngrok

* Đầu tiên bạn cần phải có 1 tài khoản github. Đăng ký [tại đây](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) nếu chưa có
1. Truy cập [Railway](https://railway.app/login) Truy cập trang web để đăng ký tài khoản Railway và đăng nhập trực tiếp bằng tài khoản github của bạn
2. Truy cập [Ngrok](https://dashboard.ngrok.com/auth) Vào trang web, và đăng ký tài khoản miễn phí
3. Truy cập [Ngrok Authtoken](https://dashboard.ngrok.com/auth) sao chép và lưu mã `Authtoken` của bạn

Notes: Tài khoản miễn phí Ngrok của một khu vực chỉ có thể có một tunnel service, vì vậy nếu bạn muốn triển khai nhiều dự án, vui lòng sửa đổi khu vực

## 2/ Triển khai

Nhấp vào nút bên dưới để triển khai

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https://github.com/ntkhang03/Railway-Ngrok&envs=NGROK_TOKEN,PASSWORD,PORT,REGION&PASSWORDDesc=M%E1%BA%ADt%20kh%E1%BA%A9u%20d%C3%B9ng%20%C4%91%E1%BB%83%20%C4%91%C4%83ng%20nh%E1%BA%ADp%20ssh&NGROK_TOKENDesc=Authtoken%20%C4%91%C3%A3%20%C4%91%C4%83ng%20k%C3%BD%20trong%20ngrok&PORTDesc=Open%20port%20you%20need%2C%20default%20is%2080&PORTDefault=80&REGIONDesc=Khu%20v%E1%BB%B1c%20ngrok%2C%20m%E1%BA%B7c%20%C4%91%E1%BB%8Bnh%20l%C3%A0%20jp%2C%20t%C3%B9y%20ch%E1%BB%8Dn%20us%2Feu%2Fap%2Fau%2Fsa%2Fjp%2Fin&REGIONDefault=jp&referralCode=IGBnmG)

`PASSWORD`: Điền vào mật khẩu để đăng nhập ssh (do bạn tùy chọn)

`NGROK_TOKEN`: Điền vào `Authtoken` đã đăng ký trong `Ngrok`

`PORT`: Điền vào cổng (PORT) bạn đã tạo ứng dụng và Railway sẽ tự động chuyển tiếp nó đến tên miền được cấp cho bạn, mặc định: 80

`REGION`: Điền vào khu vực có tunnel service, càng gần càng tốt, mặc định là jp, tùy chọn us/eu/ap/au/sa/jp/in

## 3/ Lưu ý
Tất cả dữ liệu sẽ bị xóa nếu bạn restart lại project railway
