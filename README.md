# Android-code

## EditText  
> * 设置弹出键盘回车键显示内容,实现这个功能需要调用EditText的setImeOptions方法
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
> /**
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
## 华为手机输出log
开启工程模式
1：如果是华为手机：进入拨号界面输入：*#*#2846579#*#*依次选择ProjectMenu---后台设置----LOG设置---LOG开关 点击打开
2：如果是华为pad打开自带计算器输入引号中的内容“()()2846579()()=”就会进入工程模式，然后就可以跟手机一样设置logcat开关

