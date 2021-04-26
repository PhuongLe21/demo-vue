Lesson 1:
### Install
- npm i -g @vue/cli
- vue create app-name

### Discover
- 1 file vue có 3 phần
  - template
  - script
  - style (nếu thêm attribute scoped thì css chỉ app dụng cho file đó)

Lesson 2: 
- Khởi tạo dữ liệu ban đầu:
  - Dùng hàm setup và trong hàm này return biến (có dùng ref ), rồi biến này sẽ dùng trong template
- Dùng v-for để loop và v-bind:key
- Props dùng để giao tiếp giữa các component, truyền từ cha sang con qua v-bind:ten-props=value, bên con nhận phải đăng ký bằng: props: [ mang cac props ]
- Muốn bind 1 giá trị trong thẻ html => dùng dấu :, ví dụ :class=["normal class", completed ? 'gachngang' : '' ]