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
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
- Imperative va Declarative 
  - Ví dụ như hàm map trong js là declarative, còn nếu k có map phải dùng for để duyệt chẳng hạn (imperative). Nghĩa là khi declarative programing thì mình sẽ dùng ở mức
    trừu tượng hơn (mức cao hơn) mà k cần quan tâm under the hood ntn.
  Tượng tự như declarative rendering trong Vue, khi khai báo biến trong script và dùng trong template thì Vue làm lots of word under the hood. (Data and DOM linked)

- Directive:
  v-bind: reactive behavior to DOM.
- Handle User Input: trong template: v-on:click="fn name", trong script thì khai báo methods rồi khai báo hàm trong đấy
  Note: khi state(biến) change, we don't touch DOM, cause Vue handled it
- Condition and loop: v-if and v-for  