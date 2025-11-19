<p align="center">
<a href="./README.md">[English]</a> | <a href="./README.vi.md">[Tiếng Việt]</a>
</p>

![OM_Banner_X2 (1)](https://github.com/user-attachments/assets/853153b7-351a-433d-9e1a-d257b781f93c)

<p align="center">
<a href="https://arxiv.org/abs/2412.18588">Bài báo Kỹ thuật</a> |
<a href="https://docs.openmind.org/">Tài liệu</a> |
<a href="https://x.com/openmind_agi">X</a> |
<a href="https://discord.gg/openmind">Discord</a>
</p>

**OM1 của OpenMind là một môi trường chạy AI dạng mô-đun (modular AI runtime) trao quyền cho các nhà phát triển tạo và triển khai các tác tử AI đa phương thức (multimodal AI agents) trên nhiều môi trường kỹ thuật số và robot vật lý**, bao gồm Humanoids, Ứng dụng Điện thoại, trang web, Robot bốn chân (Quadrupeds), và các robot giáo dục như TurtleBot 4. Các tác tử OM1 có thể xử lý nhiều đầu vào khác nhau như dữ liệu web, mạng xã hội, nguồn cấp dữ liệu camera và LIDAR, đồng thời cho phép thực hiện các hành động vật lý bao gồm chuyển động, điều hướng tự động và hội thoại tự nhiên. Mục tiêu của OM1 là giúp việc tạo ra các robot có khả năng cao, tập trung vào con người trở nên dễ dàng, dễ nâng cấp và (tái) cấu hình để phù hợp với các hình thức vật lý khác nhau.

## Khả năng của OM1

* **Kiến trúc Mô-đun (Modular Architecture)**: Được thiết kế bằng Python để đơn giản hóa và tích hợp liền mạch.
* **Đầu vào Dữ liệu (Data Input)**: Dễ dàng xử lý dữ liệu và cảm biến mới.
* **Hỗ trợ Phần cứng qua Plugins (Hardware Support via Plugins)**: Hỗ trợ phần cứng mới thông qua các plugin cho các điểm cuối API và kết nối phần cứng robot cụ thể với `ROS2`, `Zenoh`, và `CycloneDDS`. (Chúng tôi khuyến nghị sử dụng `Zenoh` cho tất cả các phát triển mới).
* **Màn hình Gỡ lỗi Dựa trên Web (Web-Based Debugging Display)**: Giám sát hệ thống đang hoạt động với WebSim (có sẵn tại http://localhost:8000/) để gỡ lỗi trực quan dễ dàng.
* **Các Điểm cuối Được Cấu hình Sẵn (Pre-configured Endpoints)**: Hỗ trợ Chuyển văn bản thành giọng nói (Text-to-Speech), nhiều mô hình LLM từ OpenAI, xAI, DeepSeek, Anthropic, Meta, Gemini, NearAI và nhiều Mô hình Ngôn ngữ Thị giác (VLMs) với các điểm cuối được cấu hình sẵn cho từng dịch vụ.

## Tổng quan về Kiến trúc
![Artboard 1@4x 1 (1)](https://github.com/user-attachments/assets/dd91457d-010f-43d8-960e-d1165834aa58)

## Bắt đầu

Để bắt đầu với OM1, chúng ta hãy chạy tác tử Spot. Spot sử dụng webcam của bạn để chụp và gắn nhãn các đối tượng. Các chú thích văn bản này sau đó được gửi đến LLM, và LLM trả về các lệnh hành động `movement`, `speech` và `face`. Các lệnh này được hiển thị trên WebSim cùng với thông tin thời gian cơ bản và thông tin gỡ lỗi khác.

### Quản lý Gói và Môi trường Ảo (Package Management and VENV)

Bạn sẽ cần trình quản lý gói [`uv`](https://docs.astral.sh/uv/getting-started/installation/).

### Clone Repo

```bash
git clone [https://github.com/OpenMind/OM1.git](https://github.com/OpenMind/OM1.git)
cd OM1
git submodule update --init
uv venv
