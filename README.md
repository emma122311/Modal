# Sweetalert
## 點下去用 Modal 用Sweetalert 去做
### 1.在所需 Case中 帶入 sweetalert.min.js 
### 2.把如下 function 程式複製貼上 
```
      function alertup() {
            swal("你確定要刪除資料嗎?", {
                //   title: ,
                //   text: "Once deleted, you will not be able to recover this imaginary file!",
                icon: "warning",
                buttons: ["取消", "確認"],
                dangerMode: true,

            })
                .then((willDelete) => {
                    if (willDelete) {
                        swal("成功", {
                            icon: "success",
                        });

                        var d1 = window.parent.frames[1].document.getElementById('player');
                        d1.muted = false;
                        d1.play();
                    } else {
                        swal("失敗", {
                            icon: "error"
                        });
                    }
                });
        }
```
### 3.把 onclick="alertup() 放入所需處
 // 參考 sweetalert 詳情網址 http://mishengqiang.com/sweetalert/
 
 // 參考網頁鑫宇科技中的團隊投資
