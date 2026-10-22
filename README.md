# BẢN ĐỒ SỐ 22 CƠ SỞ LƯU TRÚ PHÚ QUỐC

## 1. Giới thiệu

Bộ mẫu website dành cho sinh viên thực hành xây dựng bản đồ số. Dữ liệu được chuyển trực tiếp từ file Excel `MAU_THU_THAP_DU_LIEU_22_CSLT_THEO_KHU_VUC(2).xlsx` do giảng viên cung cấp. Đây là bản đồ **minh họa phục vụ giảng dạy, chưa phải danh mục lưu trú đã được thẩm định hoặc công bố chính thức**.

**Đủ 22 địa điểm theo cơ cấu trong Excel:** 7 khách sạn/resort 5 sao, 5 khách sạn 4 sao, 5 khách sạn 3 sao và 5 homestay. Tên, địa chỉ, hạng sao, tọa độ, mô tả và nội dung khảo sát giữ theo bảng Excel (chỉ loại bỏ khoảng trắng thừa). Hạng sao *theo dữ liệu sinh viên* chứ không phải kết quả xác minh độc lập.

## 2. Ba tệp cốt lõi

- `index.html`: toàn bộ giao diện bản đồ Leaflet, tra cứu, lọc, thẻ địa điểm, cửa sổ chi tiết, nút chỉ đường, tương thích điện thoại.
- `du_lieu.js`: 22 địa điểm đã nhập từ Excel; gồm tọa độ, mô tả, dữ liệu khảo sát, URL ảnh và trang nguồn ảnh.
- `README.md`: hướng dẫn sử dụng, cách thay ảnh và những lưu ý cần rà soát.

Chỉ cần giữ **3 tệp trong cùng một thư mục**. Mở `index.html` trong Chrome/Edge hoặc đưa lên GitHub Pages. Cần kết nối Internet để tải thư viện Leaflet, nền bản đồ OpenStreetMap và ảnh từ website nguồn. Khi một ảnh không tải được, giao diện thay bằng hình minh họa đồ họa tự tạo, tránh khung ảnh lỗi.

## 3. Các chức năng

1. Ghim 22 vị trí được lấy nguyên từ cột `Latitude` và `Longitude` trong `DANH_SACH_22_CSLT`.
2. Lọc toàn bộ, 5 sao, 4 sao, 3 sao, homestay và tìm kiếm không phân biệt dấu tiếng Việt.
3. Chạm vào thẻ hoặc ghim để mở phần chi tiết: tên, mã, địa chỉ, mô tả, tiện ích, phòng, ăn uống, khảo sát và giá nếu có.
4. Mở đường đi trên Google Maps bằng **tọa độ trong Excel** hoặc mở liên kết Maps gốc từ Excel để so sánh.
5. Chế độ bản đồ sáng/tối, toàn màn hình trên máy tính và danh sách đóng/mở trên điện thoại.

## 4. Nguồn dữ liệu và ảnh

- Dữ liệu gốc: sheet `DANH_SACH_22_CSLT`, dòng 5-26; dùng cột B, C, D, E, F, G, H, I, J và N. 
- Thông tin chi tiết: sheet `KHAO_SAT_CHI_TIET`, dòng 5-26, các cột E đến Q.
- **Các ô K, L, M trong danh sách chỉ chứa chuỗi như `K5`, `L5`, `M5`, không phải tên ảnh thực tế.** Không có ảnh khảo sát gốc được đính kèm. Con số `Số ảnh = 3` trong Excel không chứng minh ba ảnh tồn tại.
- Đã bổ sung URL ảnh cho **19 cơ sở** từ các trang công khai có ảnh nhận diện của cơ sở; **3 cơ sở (HS03, HS04, HS05)** dùng ảnh chung của khu vực gần đó, được ghi rõ 'Ảnh khu vực minh họa, không phải hình cơ sở'. Các ảnh không phải do sinh viên đi thực địa chụp.
- Các URL ảnh là liên kết ngoài; ảnh có thể bị chặn nhúng, đổi địa chỉ hoặc bị xóa. Mỗi địa điểm có đường dẫn tới trang đã tìm ảnh.
- **Quyền ảnh:** việc ảnh hiển thị công khai trên Internet không có nghĩa được phép tái sử dụng. Bộ mẫu này là bản thực hành. Trước khi đưa website lên mạng công khai, giảng viên/nhóm cần thay bằng ảnh tự chụp có phép, ảnh do cơ sở cho phép, hoặc ảnh có giấy phép phù hợp; ghi nguồn, tác giả và giấy phép theo yêu cầu.

### Danh sách nguồn ảnh đã gắn

| Mã điểm | Cơ sở theo Excel | Loại ảnh | Nguồn tham khảo |
|---|---|---|---|
| 5S01 | Meliá Vinpearl Phú Quốc | Cơ sở (ảnh từ web) | [Meliá - Website chính thức](https://www.melia.com/en/hotels/vietnam/phu-quoc/melia-vinpearl-phu-quoc) |
| 5S02 | Crowne Plaza | Cơ sở (ảnh từ web) | [Crowne Plaza - Website chính thức](https://phuquoc.crowneplaza.com/5-reasons-crowne-plaza-phu-quoc-starbay-is-the-perfect-destination/) |
| 5S03 | Seasells Phú Quốc | Cơ sở (ảnh từ web) | [Traveloka - Seashells Phú Quốc](https://www.traveloka.com/vi-vn/hotel/vietnam/seashells-phu-quoc-hotel--spa-3000010043411) |
| 5S04 | Wyndham Grand | Cơ sở (ảnh từ web) | [Join UP! - Wyndham Grand Phú Quốc](https://joinup.ee/en/hotel/64472) |
| 5S05 | La Festa Phú Quốc | Cơ sở (ảnh từ web) | [Sun Paradise Land - La Festa](https://sunparadiseland.com/tw/SunParadiseLandPhuQuoc/tin-tuc/tan-suo2026nian-fu-guo-dao-zui-shou-huan-ying-de-shi-da-hao-hua-jiu-dian-16608) |
| 5S06 | JW Marriot | Cơ sở (ảnh từ web) | [Phetravel - JW Marriott Phú Quốc](https://phetravel.com/so-sanh-5-resort-5-sao-phu-quoc-dep-nhat-cho-honeymoon) |
| 5S07 | Ocean Bay | Cơ sở (ảnh từ web) | [IZITOUR - Ocean Bay Resort](https://izitour.com/en/tropical-escape-phu-quoc-4-days) |
| 4S01 | Phú Quốc Ocean Pearl | Cơ sở (ảnh từ web) | [KKday - Phú Quốc Ocean Pearl](https://www.kkday.com/en/hotel/product/333616) |
| 4S02 | Aquasun Hotel Phú Quốc | Cơ sở (ảnh từ web) | [Join UP! - Aquasun Hotel](https://joinup.ee/en/hotel/64363) |
| 4S03 | Mường Thanh Luxury Phú Quốc Hotel | Cơ sở (ảnh từ web) | [Crystal Bay - Mường Thanh Luxury](https://crystalbay.com/en/35-muong-thanh-luxury-phu-quoc-hotel-a-comprehensive-review-for-the-discerning-traveler-n62286.html) |
| 4S04 | AVS Hotel Phu Quoc | Cơ sở (ảnh từ web) | [AVS Hotel - Website cơ sở](https://avshotelphuquoc.com/) |
| 4S05 | Haya Hotel Phu Quoc | Cơ sở (ảnh từ web) | [Kompas Tour - Haya Hotel](https://kompastour.com/ge/eng/country/vietnam/fukuok/haya_hotel/) |
| 3S01 | Leaf Hotel | Cơ sở (ảnh từ web) | [Agoda - Leaf Hotel](https://gtour.gmarket.co.kr/TourV2/Item?goodscode=4151976754) |
| 3S02 | Golden Dragon Hotel | Cơ sở (ảnh từ web) | [Booking.com - Golden Dragon Hotel](https://www.booking.com/hotel/vn/golden-dragon-phu-quoc2.html) |
| 3S03 | Praha Hotel | Cơ sở (ảnh từ web) | [Kompas Tour - Praha Hotel](https://kompastour.com/kz/rus/country/vietnam/fukuok/praha_hotel_phu_quoc/) |
| 3S04 | Sailing Hotel | Cơ sở (ảnh từ web) | [MIA.vn - Sailing Hotel](https://mia.vn/cam-nang-du-lich/sailing-hotel-phu-quoc-khach-san-3-sao-gan-dinh-cau-70) |
| 3S05 | Venus Hotel | Cơ sở (ảnh từ web) | [Priceline / Booking - Venus Hotel](https://www.priceline.com/hotel-deals/en-us/P5000494963/H42534506/venus-hotel-sky-bar-phu-quoc.ssp) |
| HS01 | CHILL HOUSE by the Beach | Cơ sở (ảnh từ web) | [CHILL HOUSE - Website chính thức](https://chillhousephuquoc.com/?product=chill-14-bien-ban-cong-bon-tam) |
| HS02 | Lotus Home | Cơ sở (ảnh từ web) | [Mytour - Lotus Home khu Cây Sao](https://mytour.vn/en/blog/bai-viet/lotus-home-phu-quoc-serene-beauty-amidst-pearl-island.html) |
| HS03 | Tiny House | Khu vực, không phải cơ sở | [VPQ - Toàn cảnh Sunset Town](https://vpq.vn/sunset-town-hoang-hon-trac-tuyet-tai-thi-tran-hoang-hon.html) |
| HS04 | Happy Bông | Khu vực, không phải cơ sở | [Đất Việt Tour - Grand World](https://datviettour.com.vn/tin-tuc/ca-the-gioi-thu-nho-lai-vua-bang-khu-nghi-duong-grand-world-phu-quoc) |
| HS05 | Sóc nhím Homestay& Grandworld Phú Quốc | Khu vực, không phải cơ sở | [Bayu Buana Travel - Grand World](https://www.bayubuanatravel.com/tours/05d04n-the-escape-of-vietnam-phu-quoc-with-vinwonders-theme-park-grand-world-avq1) |

## 5. Cách sinh viên thay bằng ảnh chụp thực địa

Bước 1. Chụp ảnh và xin phép chủ cơ sở (nếu cần). Nên có ảnh mặt tiền, không gian/phòng hoặc tiện ích, và một nét đặc trưng; tránh đưa người khác lên ảnh khi chưa đồng ý.

Bước 2. Tạo thư mục mới tên `anh` cùng cấp với `index.html` và `du_lieu.js`, rồi lưu ảnh, ví dụ `anh/5S01_01.jpg`.

Bước 3. Mở `du_lieu.js`, tìm `"id": "5S01"`; thay `image` thành `"anh/5S01_01.jpg"`, đổi `imageKind` thành `"property"`, thay `imageLabel` và `imageSource` cho chính xác. Nếu ảnh tự chụp, có thể ghi `imageSource` là `Ảnh thực địa của nhóm sinh viên`, còn `imagePage` để `""`.

Bước 4. Kiểm tra ảnh bằng cách mở lại website. **Nếu nộp website qua GitHub Pages, tải cả thư mục `anh/` lên repository**. Lúc đó tổng số tệp sẽ lớn hơn ba; bản mẫu ban đầu sử dụng liên kết ảnh để giữ đúng ba tệp.

## 6. Những vấn đề từ Excel cần sinh viên rà soát

- **HS02 – Lotus Home:** địa chỉ và tọa độ thuộc khu ấp Cây Sao (phía Đông đảo), nhưng phần giới thiệu/điểm kết nối lại mô tả khu Sunset Town và Cầu Hôn (phía Nam). Cần đối chiếu chính xác cơ sở và ghi chép khảo sát. Ảnh chọn theo cơ sở Lotus Home ở Cây Sao, không theo phần ghi Sunset Town.
- **3S05 – Venus Hotel:** địa chỉ ghi `60A Trần Hưng Đạo, Dương Đông`, nhưng tọa độ Excel `10.033150, 104.004301` chỉ về phía Nam đảo. Cần kiểm tra và sửa nếu xác định khác nhau. Web **cố ý giữ nguyên tọa độ Excel**, không tự dịch chuyển ghim.
- Có tên viết tắt/khác tên thường dùng trên web (ví dụ `Crowne Plaza`, `Seasells Phú Quốc`, `JW Marriot`), và một số địa chỉ vẫn ghi tỉnh Kiên Giang. Tên và cách ghi địa chỉ trong website đang kế thừa Excel, không mặc nhiên là tên pháp lý hiện hành.
- Cột giá không có ngày kiểm tra đáng tin cậy tại từng dòng. Website hiển thị nhãn **"Giá tham khảo ghi trong Excel"**, không khẳng định giá đặt phòng thời điểm hiện tại.
- Các cột kiểm tra R-S-T ở `DANH_SACH_22_CSLT` trong bản Excel hiển thị `#REF!`; bảng tổng hợp còn một số ô `#ERROR!`. Website **không sử dụng** các kết quả kiểm tra lỗi này và **không tuyên bố đã kiểm tra xong dữ liệu**.
- Phân hạng khách sạn, địa chỉ, tọa độ và thông tin tiện ích chưa được đối chiếu có hệ thống với nguồn của cơ quan quản lý hoặc khảo sát gốc. Trước khi công bố cần lập bằng chứng xác minh riêng cho từng điểm.

## 7. Đưa lên GitHub Pages miễn phí

1. Đăng nhập [GitHub](https://github.com), tạo một repository mới (ví dụ `ban-do-luu-tru-phu-quoc`) ở chế độ **Public**.
2. Vào `Add file` > `Upload files`; đưa **ba tệp trong thư mục bản mẫu** (`index.html`, `du_lieu.js`, `README.md`) lên thư mục gốc. Không tải cả thư mục bao quanh nếu muốn URL gốc tự mở `index.html`.
3. Vào `Settings` > `Pages`, chọn `Deploy from a branch` và nhánh `main`, thư mục `/(root)`; nhấn `Save`.
4. Truy cập `https://TEN-TAI-KHOAN.github.io/ban-do-luu-tru-phu-quoc/`. Đây chỉ là mẫu đường dẫn, không phải website đã được xuất bản.
5. Khi thay dữ liệu/ảnh, tải tệp mới lên repository và commit.

## 8. Tài liệu nền tảng

- [Leaflet 1.9.4](https://leafletjs.com/reference.html)
- [OpenStreetMap – ghi công và quy định sử dụng bản đồ](https://operations.osmfoundation.org/policies/tiles/)
- [GitHub Pages – bắt đầu](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)

**Ngày tạo bản mẫu:** 22/10/2026. **Mục đích:** bài tập xây dựng bản đồ số từ dữ liệu Excel, không phải cổng tư vấn đặt phòng.
