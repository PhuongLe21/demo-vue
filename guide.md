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
- Viết tắt: v-on(@), v-bind(:)

- Truyền event từ child sang parent: Ví dụ: Component cha là 1 data list, con sẽ là 1 item trong list đấy, muốn thay đổi nội dung item thì phải thay đổi data ở trên list (có thể hình dung app todoList chẳng hạn)
  React: truyền hàm (as a prop) từ parent sang child, trong child gọi hàm đó và truyền thêm thông tin nếu cần, parent sẽ xử lý logic (thay đổi state: cập nhật lại list => child sẽ render lại)
  Vuejs: Tương tự: note: child sẽ emit 1 event (qua context.emit(tên_emit, data)) và parent sẽ handle 
- Dùng v-model để lấy giá trị giữa template và biến trong script, (ví dụ lấy giá trị từ thẻ input, trong React sẽ phải dùng setState)

-------------------------------------------------------
Tom tat sau khi hoc xong 5 videos ve vue3
- 1 component có 3 phần template, script, style
- Muốn dùng biến hay hàm trong template thì trong js phải export ra, còn dùng component cũng export (hay đăng ký)
- v-model để bind data giữa user nhập vào và xử lý trong js (vd: lấy giá trị từ input)