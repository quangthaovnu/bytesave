# bytesave account

## Danh sách commands

### Function: account register
Để sử dụng được bytesave bạn cần phải có một tài khoản.
Người dùng chỉ cần nhập vào địa chỉ email theo cú pháp.
```
    bytesave account --register --email "email"
```
Hệ thống sẽ gửi yêu cầu đến API account register để thực hiện. Quá trình gửi yêu cầu được thực hiện
>   Input: gửi đi một json theo định dạng {"email":[string]} 
    Output:
    Nếu như thực hiện thành công, server sẽ gửi mật khẩu đến địa chỉ email đăng ký. và trả về Function: account register một json có định dạng {"status":"true", "msg":[string]}
    Nếu không thực hiện được hoặc xảy ra lỗi thì giá trị trả về Function: account register một json có định dạng {"status":"false", "msg":[string]}

### Function: account login
Đăng nhập vào bytesave thực hiện bằng cách
```
    bytesave account --login --u "email" --p "password"
```
Trong đó --u là địa chỉ email, --p là password
Khi đó Function: account login sẽ gửi đến API account login.
>    Input: json theo định dạng {"email":[string], "password":[string], "os":[string], "serialNumber":[string], "ipPublic":[string], "ipPrivate":[string], "nameComputer":[string]}
    Output:
    Nếu như thực hiện thành công. API sẽ trả về Function: account login một json có định dạng {"status":"true", "msg":[string]}
    Xảy ra lỗi đăng nhập API sẽ trả về Function: account login một json có định dạng {"status":"false", "msg":[string]}

### Function: account logout
Khi bạn thực hiện tác vụ đăng xuất. Tất cả tác vụ hiện có sẽ bị xóa và không thể phục hồi.
Để thực hiện đăng xuất:
```
    bytesave account --logout
```
Function: account logout sẽ gửi yêu cầu logout đến API account logout
>   Input: theo định dạng json {"serialNumber":[string]}
    Output:
    Nếu như thực hiện thành công. API sẽ trả về Function: account logout một json có định dạng {"status":"true", "msg":[string]}
    Xảy ra lỗi API sẽ trả về Function: account logout một json có định dạng {"status":"false", "msg":[string]}

### Function: account update password
Người dùng muốn đổi mật khẩu
```
    bytesave account --update --u "email" --p "password" --newpass "new password"
```
Function: account update password sẽ gửi yêu cầu đến API account update password bằng một json
>   Input: theo định dạng json {"email":[string], "password":[string], "newPassword":[string]}
    Output:
    Nếu như thực hiện thành công. API sẽ trả về Function: account update password một json có dạng {"status":"true", "msg":[string]}
    Xảy ra lỗi API sẽ trả về Function: account update password một json có định dạng {"status":"false", "msg":[string]}
### Function: account renew 
Để gia hạn sử dụng cho tài khoản
```
    bytesave account renew --u "email"
```
Function: account renew sẽ gửi yêu cầu đến API account renew bằng một json 
>   Input: theo định dạng json {"email":[string]}
    Output:
    Nếu như thực hiện thành công. API sẽ trả về Function: account renew một json có dạng {"status":"true", "msg":[string]}
    Xảy ra lỗi API sẽ trả về Function: account renew một json có định dạng {"status":"false", "msg":[string]}