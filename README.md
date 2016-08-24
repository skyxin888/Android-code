# Android-code

##EditText  
* 设置弹出键盘回车键显示内容,实现这个功能需要调用EditText的setImeOptions方法
```
/**
*
* IME_ACTION_SEARCH 搜索
* IME_ACTION_SEND 发送
* IME_ACTION_NEXT 下一步
* IME_ACTION_DONE 完成
*/
mInputEditTxt.setImeOptions(EditorInfo.IME_ACTION_SEARCH);
```
* 监听输入法中的回车按钮，可以通过监听EditText的按键点击事件来实现：
```
/**
 * 监听输入法按键
 * 
 * */
mInputEditTxt.setOnKeyListener(new OnKeyListener() {
    @Override
    public boolean onKey(View v, int keyCode, KeyEvent event) {
        if (keyCode == KeyEvent.KEYCODE_ENTER && event.getAction() == KeyEvent.ACTION_UP) {
            System.out.println("KEYCODE_ENTER");
            return true;
        }
        return false;
    }
});
```

