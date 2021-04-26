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