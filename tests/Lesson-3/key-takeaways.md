# Git
## Undo actions
- **Sửa lại commit message gần nhất**
```js
git commit --amend -m "message"
```
- **Staging area => Working directory (2 -> 1)**
```js
git restore --staged <file_name>
git restore --staged .
```
- **Repository => staging area (3 -> 2)**
```js
git reset HEAD~N
```
Reset (N) commit tính từ commit gần nhất
Commit đầu tiên không thể xóa, chỉ có thể xóa thư mục .git rồi init lại từ đầu

## Branching
- Lấy code từ server về local: `git pull origin main`
- Xem danh sách nhánh: `git branch` 
- Tạo nhánh mới: `git branch <branch_name>`
- Chuyển nhánh: `git checkout <branch_name_muốn_chuyển>`
- Tạo kết hợp chuyển nhánh: `git checkout -b <branch_name>`
- Xóa nhánh: `git branch -D <branch_name>`
- Xem lại code ở 1 commit cũ: `git checkout <revision>`
(dùng lệnh `git log` để lấy revision (commit ID))

## .gitignore file
Chức năng: Dùng để bỏ qua các file không cần git theo dõi
- Ignore file: `<file_name>`
- Ignore folder: `<folder-name>/`

# Javascript
## Các quy tắc đặt tên:
- Tên file: `kebab-case`
- Tên biến: `camelCase`
- Tên class: `PascalCase`
## Object: đối tượng
Chức năng: tập hợp các giá trị vào cùng một **biến** hoặc **hằng số**
```js
let/const <ten_object> = {
    <thuoc_tinh>: <gia_tri>,
    ...
}

// Ex:
const person = {
    name: "Hien",
    role: student
};
```
Lưu ý: không thể thay thế object bằng object mới nhưng có thể edit/add/delete thuộc tính trong object
```js
const student = {name: "Ngan"};
student = {age: 20}; // err: không thể thay thế object = object mới
student.name = "Ngoc"; // valid: có thể thay thế thuộc tính
student.age = 20; // valid: có thể thêm thuộc tính
student["role"] = "student"; // valid: có thể thêm thuộc tính
delete student.age; // valid: có thể xóa thuộc tính
```
## Array: mảng
- Khai báo mảng: `const mixed = [1, "Hello", true,  ,];`
- Truy xuất độ dài mảng: `console.log(mixed.length);`
- Truy xuất phần tử theo index: `console.log(mixed[2]);`

## Function: hàm
```js
function <nameFunction>() {
    // code
}
//Ex:
function sayHello() {
    console.log("Hello World!");
}

sayHello(); // 👉 "Hello World!"
```

### Hàm push: 
Chức năng: thêm 1 hoặc nhiều phần tử vào cuối mảng
```js
const arr = [1, 2];
arr.push(3);
console.log(arr); // in ra [1, 2, 2]
```







