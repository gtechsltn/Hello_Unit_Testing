# Unit Testing trong C#

https://learn.microsoft.com/en-us/visualstudio/test/unit-test-basics?view=vs-2022

https://docs.telerik.com/devtools/justmock/basic-usage/arrange-act-assert

https://www.linkedin.com/pulse/elevate-your-unit-testing-aaa-pattern-c-collins-tonui/

https://www.c-sharpcorner.com/article/unit-testing-c-sharp-in-net-core-using-nunit/

https://www.c-sharpcorner.com/article/mock-testing-with-moq/

https://methodpoet.com/aaa-in-unit-testing/

https://semaphoreci.com/blog/aaa-pattern-test-automation

# Unit Testing trong Flutter

https://medium.com/@NALSengineering

1. Unit Tests
2. Integration Tests
3. Widget Tests
4. Golden Tests

### Mocking và Stubbing

+ Mocking là việc tạo ra 1 object giả thay vì sử dụng object thật. Chúng ta thường sử dụng mocking để mock các dependency của object cần test.
+ Sau khi tạo ra object giả, chúng ta có thể giả lập các method của nó và kiểm soát kết quả trả về của các method của nó. Kỹ thuật này được gọi là Stubbing.

### Unit Testing sẽ cần học các phần sau:

+ Writing your first Unit Test.
+ Phân biệt các khái niệm: Mock, Fake, Stub.
+ Các hàm test, group, setUp, tearDown, setUpAll, tearDownAll.
+ Các best practices.
+ Cách viết code để dễ viết test.
+ Các lỗi hay mắc phải khi viết test.
+ Ứng dụng AI như ChatGPT và Github Copilot để viết unit test nhanh hơn.
+ Tích hợp CI để kiểm tra các bài test và report Test Coverage.

### Về cách đặt tên của một Unit Test

[unit name] ... [should] ... [expected output] ... [when] ... context

Ví dụ: ValidateEmail_Should_ReturnsTrue_When_TheEmailIsNotEmpty

Về body của một unit test, thông thường sẽ follow Arrange, Act, and Assert (AAA) pattern.

Sai lầm 1: Không sử dụng Dependency Injection (DI)

Sai lầm 2: Sử dụng top-level function và top-level variable bên trong hàm cần test.

Sai lầm 3: Gọi hàm của plugin có implement native code bên trong hàm cần viết test.

Sai lầm 4: Xử lý logic và UI vào cùng một class hoặc một hàm.

Sai lầm 5: Sử dụng DateTime.now()

=> phải thay DateTime.now() bởi clock.now()

Sai lầm 6: Code một hàm quá lớn hoặc tách ra nhiều hàm quá nhỏ
