# ChineseLouis 中文

Ứng dụng Android học tiếng Trung từ số 0, giao diện tiếng Việt. **182 ngày / 26 tuần, 30 phút mỗi ngày, 311 từ và cụm từ khác nhau.**

## Cài đặt

Mở tab **Actions → Build ChineseLouis APK → lần chạy màu xanh → Artifacts → ChineseLouis-APK**. Giải nén ZIP, chép `ChineseLouis.apk` sang điện thoại và mở để cài. Cho phép cài ứng dụng từ nguồn đó khi Android hỏi. Hỗ trợ Android 8 trở lên. Đây là APK tự luyện ký debug, chưa phát hành trên Play Store. Chữ ký debug của các lần dựng có thể khác; khi cập nhật nếu Android báo xung đột chữ ký, không gỡ bản cũ nếu còn muốn giữ tiến độ.

## Chức năng

- Lịch học 182 ngày: ôn 5 phút, học mới 10 phút, nghe 8 phút, nói 5 phút, viết 2 phút.
- Pinyin, thanh điệu, từ vựng, câu mẫu có nghĩa tiếng Việt và audio Mandarin được đóng gói trong APK.
- Ghi âm tối đa 90 giây, phát lại để tự so với mẫu. Mỗi lần ghi thay bản trước.
- Luyện hình chữ bằng tay trên màn hình. Chưa có hướng dẫn thứ tự nét hoặc chấm tự động.
- Kiểm tra đọc và nghe 12 câu, lưu điểm cao nhất; ôn các từ trả lời sai. Ngày thứ 7 của mỗi tuần ôn tối đa 4 tuần gần nhất; ngày cuối ôn toàn khóa.
- Lưu tiến độ trên điện thoại; học không cần tài khoản hoặc Internet. Không xin quyền Internet. Quyền micro được hỏi khi ghi âm. Gỡ ứng dụng sẽ xóa dữ liệu học.

## Nội dung và giới hạn

Nội dung tự biên soạn cho tự học cơ bản, không sao chép HSK Standard Course hoặc audio thương mại. Có thể học bổ sung bằng HSK Standard Course 1 mua hợp pháp. Audio tổng hợp qua gTTS ở thời điểm dựng (cần mạng trên máy dựng), sau đó được đóng gói để chạy offline. Không có nhận dạng hoặc chấm phát âm tự động. Bài kiểm tra không phải kỳ thi/chứng chỉ HSK.

## Dựng và kiểm tra

GitHub Actions tự dựng khi có commit lên `main`. Dùng JDK 17, Gradle 8.9, AGP 8.7.3, Android SDK 35. Quy trình kiểm tra cấu trúc 26 tuần / 182 ngày, tạo và xác nhận đủ audio, dựng APK, chạy Android Lint, xác nhận chữ ký và audio trong APK. File APK tải ở Artifacts sau khi quy trình thành công. Chưa kiểm thử trên điện thoại thật; hãy kiểm tra nghe, ghi âm và lưu tiến độ ở chế độ máy bay sau khi cài.
