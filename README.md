Hoàng Mạnh Cường 2321050103# PTPMQL

1.Cấu trúc thư mục dự án .NET MVC

Controllers: Chứa các thư mục controller
Models: Chứa các lớp đại diện cho CSDL cho ứng dụng
Views: Thư mục chứa các thành phần hiển thị giao diện người dùng
wwwroot: Chứa file tĩnh (css, js, images)
Program.cs: Cấu hình dự án
appsettings.json: cấu hình dự án

---

2.  Định tuyến (Routing) trong ASP.NET MVC

Routing là cơ chế ánh xạ URL tới Controller và Action.

Cú pháp mặc định trong Program.cs:

app.MapControllerRoute(
name: "default",
pattern: "{controller=Home}/{action=Index}/{id?}"
);

Ý nghĩa:

- controller: tên controller
- action: tên phương thức
- id: tham số (không bắt buộc)

Ví dụ:

- /Demo/Index → DemoController, action Index

  3.Namespace trong C#
  Namespace dùng để nhóm các class lại với nhau, tránh trùng tên.

  Ví dụ:
  namespace Buoi3_MVC.Controllers
  {
  public class DemoController : Controller
  {
  }
  }

4. Controller,View trong ASP.NET MVC

- Controller :

* Nằm trong thư mục Controllers
* Nhiệm vụ của Controller:
  - Xử lý các yêu cầu của người dùng gửi tới từ View.
  - Truy xuất dữ liệu trong cơ sở dữ liệu.
  - Gọi các mẫu View và trả về dữ liệu
* Mặc định khi tạo project sẽ có HomeController
* Trong controller sẽ chứa các action (ví dụ: Index, Privacy), mỗi action sẽ thực thi một nhiệm vụ cụ thể (trả về các view tương ứng)

- View :

* Có phần mở rộng là “.cshtml”
* Nằm trong thư mục Views/Controler_Name (tương ứng với HelloWorldController sẽ có thư mục HelloWorld trong thư mục Views)
* Nhiệm vụ của View: Cung cấp giao diện người dùng (HTML) bằng C#
