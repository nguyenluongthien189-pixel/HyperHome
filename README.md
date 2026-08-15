# 🏡 HyperHome

> **Plugin Quản Lý Nhà (Home Management) Hiệu Năng Cao Cho Minecraft (Spigot / Paper / Folia 1.21+)**

![Java Version](https://img.shields.io/badge/Java-21-orange.svg)
![Minecraft Version](https://img.shields.io/badge/Minecraft-1.21%2B-brightgreen.svg)
![Platform Support](https://img.shields.io/badge/Platform-Paper%20%7C%20Folia-blue.svg)
![License](https://img.shields.io/badge/License-Proprietary-red.svg)

**HyperHome** là một plugin quản lý nhà (Homes) cao cấp, độc quyền, giàu tính năng và được tối ưu hóa hiệu năng tối đa cho các máy chủ Minecraft chuyên nghiệp. Plugin được thiết kế đặc biệt để hỗ trợ kiến trúc đa luồng của **Folia** cũng như hệ thống máy chủ **Paper/Purpur**.

---

## ✨ Tính Năng Nổi Bật

- ⚡ **Hỗ Trợ Folia Native**: Tương thích hoàn toàn với kiến trúc đa vùng (Region Scheduler) và tác vụ bất đồng bộ (Async Scheduler) của Folia & Paper.
- 🎨 **Giao Diện GUI Đẹp Mắt**:
  - Menu chính dạng lưới sinh động cho phép xem danh sách nhà, icon giường & phẩm màu.
  - Tùy chỉnh Icon hiển thị cho từng Home với thư viện hàng trăm Material.
  - Giao diện xác nhận xóa chống nhấn nhầm.
- 📝 **Sign GUI Tương Tác**:
  - Đổi tên nhà trực tiếp thông qua biển (Sign GUI).
  - Xem thông tin tọa độ chi tiết trên biển.
- 🔒 **Phân Quyền & Giới Hạn Theo Rank**: Cấu hình số lượng nhà tối đa khác nhau tùy theo Permission của từng Rank (Ví dụ: default: 1 home, VIP: 3 homes).
- 🚫 **Blacklist Thế Giới**: Cấm tạo Home tại các thế giới chỉ định (Spawn, AFK Zone, Event...).
- ⏳ **Hệ Thống Dịch Chuyển An Toàn**:
  - Đếm ngược thời gian dịch chuyển kèm hiệu ứng Actionbar & âm thanh.
  - Tự động hủy dịch chuyển khi di chuyển quá cự ly cho phép hoặc khi nhận sát thương.
- 💾 **Lưu Trữ SQLite Bất Đồng Bộ**: Xử lý dữ liệu SQLite bằng WAL Mode, giảm thiểu tối đa hiện tượng lag/khựng máy chủ.
- 🌈 **Hỗ Trợ Hex Color**: Hỗ trợ mã màu Hex `&#RRGGBB` và mã màu truyền thống `&`.

---

## 📋 Yêu Cầu Hệ Thống

- **Java**: Version 21 trở lên.
- **Server Software**: Paper, Folia, Purpur, Canvas (Phiên bản Minecraft **1.21+**).

---

## 🚀 Hướng Dẫn Cài Đặt

1. Tải file `HyperHome-1.0-SNAPSHOT.jar` đã được đóng gói chính thức.
2. Thả file `.jar` vào thư mục `plugins/` của máy chủ.
3. Khởi động lại máy chủ hoặc nạp plugin.
4. Cấu hình các file trong thư mục `plugins/HyperHome/` theo nhu cầu.

---

## 📜 Lệnh & Quyền (Commands & Permissions)

| Lệnh | Mô tả | Quyền mặc định |
| :--- | :--- | :--- |
| `/home [tên]` | Dịch chuyển tới nhà đã lưu hoặc mở Menu chính nếu không nhập tên. | Mọi người chơi |
| `/homes` | Mở giao diện Menu danh sách nhà. | Mọi người chơi |
| `/sethome <tên>` | Thiết lập vị trí đứng hiện tại thành nhà mới. | Mọi người chơi |
| `/delhome <tên>` | Xóa một nhà đã lưu. | Mọi người chơi |
| `/hyperhome reload` | Tải lại toàn bộ tệp cấu hình & ngôn ngữ. | `home.admin` |

---

## ⚙️ Cấu Hình Mô Tả

### `settings.yml` (Trích đoạn)

```yaml
language: "Vi.yml"
teleport-time: 5
teleport-effects: false

# Thế giới không cho phép sethome
blacklist:
  - "spawn"
  - "Afkzone"

permissions:
  home-admin: "home.admin"
  home-limits:
    - default:home.default:1
    - vip:home.free:2
```

---

## 👨‍💻 Tác Giả

- **Đội ngũ phát triển**:`ItzShino`, `Yaanghi`

---

## 🔒 Giấy Phép & Bản Quyền (License & Copyright)

**Copyright © 2026 HyperDev. All Rights Reserved.**

Dự án này là **Mã Nguồn Đóng / Độc Quyền (Closed Source / Proprietary)**.
- Nghiêm cấm phân phối lại, chia sẻ mã nguồn hoặc phát hành lại công khai dưới mọi hình thức khi chưa có sự đồng ý bằng văn bản từ tác giả.
- Chỉ được phép biên dịch và sử dụng nội bộ trong hệ thống máy chủ được cấp phép.
