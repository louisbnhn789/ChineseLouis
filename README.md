# ChineseLouis 2.0

Ứng dụng học tiếng Trung offline 30 phút/ngày, giao diện tiếng Việt, có lộ trình 182 ngày.

## Cập nhật 2.0

- Mục **Ngữ pháp** riêng: 40 bài từ cơ bản đến ứng dụng, có công thức, cách dùng, lỗi dễ nhầm, 80 câu ví dụ có audio và 80 câu bài tập kèm giải thích. Ví dụ tập trung vào công việc trong nhà máy.
- Mục **Kho từ**: thêm chính xác 1.000 mục từ/cụm từ, không trùng chữ bản ngữ trong kho cũ. Tổng cộng 1311 mục học riêng biệt, gồm mục học của lộ trình cũ.
- Các chủ đề thông dụng: nhận ca, thao tác, vật liệu, linh kiện điện tử, dụng cụ, lắp ráp, ép nhựa/mạ, máy móc, bảo trì, chất lượng, đo kiểm, RF, độ tin cậy, ESD, kho, đóng gói, xuất hàng, mua hàng, nhà cung cấp, họp, báo cáo, audit, bàn giao và sinh hoạt hằng ngày.
- Tìm theo chữ bản ngữ, Pinyin, nghĩa tiếng Việt; lọc chủ đề; nghe từng mục; đánh dấu đã nhớ hoặc đưa vào ôn tập; kiểm tra nghe/đọc kho từ 12 câu.
- Gợi ý bài ngữ pháp theo ngày sau giai đoạn phát âm nhập môn. Chọn học một cấu trúc hoặc 5–10 mục từ trong phần 10 phút học mới; không cần học dồn cả kho từ.

## Offline và dữ liệu

Bài học, ngữ pháp, ví dụ và audio đều nằm trong APK. Không xin quyền Internet. Micro chỉ dùng khi ghi âm; mỗi bản ghi mới thay bản trước. Tiến độ/điểm nằm trên điện thoại. Không có chấm phát âm hoặc nét viết tự động. Nội dung và câu ví dụ tự biên soạn; audio tổng hợp gTTS; Pinyin tạo bằng pypinyin, đối chiếu audio khi học từ đa âm. Ví dụ kỹ thuật không thay thế WI hoặc tiêu chuẩn nhà máy.

## Cài đặt

Android 8 trở lên. Tải APK ở **Actions → lần chạy thành công → Artifacts → ChineseLouis-APK**, giải nén và mở APK trên điện thoại.

ChineseLouis 2 dùng mã ứng dụng mới để cài song song với bản 1, vì bản 1 không lưu khóa ký. Không cần gỡ bản 1. Tiến độ bản 1 không tự chuyển sang bản 2. Khóa ký của bản 2 được lưu cache cho các bản dựng sau.

## Dựng và kiểm tra

Chạy `pip install pypinyin==0.53.0 gTTS==2.5.4`, `python curriculum.py`, `python expand_course.py`, `python generate_audio.py`, rồi `gradle :app:assembleDebug :app:lintDebug` với JDK 17 / Gradle 8.9 / Android SDK 35. `course.json` trong APK được sinh bởi quy trình này; file nền trong Git không chứa toàn bộ dữ liệu mở rộng.

CI xác nhận 1.000 mục bổ sung không trùng, 40 bài ngữ pháp, đáp án bài tập, audio đầy đủ, chữ ký APK, và Android Lint. APK ký debug dùng để tự luyện; chưa phát hành Play Store và chưa kiểm thử trên điện thoại thật.
