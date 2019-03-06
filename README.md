# XEditText

## fork过来主要是为了解决被加了最大长度的属性，然后用户通过复制粘贴到控件，因为光标位置问题导致奔溃的情况，不过发现另外一个问题，暂时无法修复，就是控件加了digits不起作用

## Gradle
```groovy
    dependencies{
        implementation 'com.github.tomxukui:XEditText:v2.2.7'
    }
```

***
## Usage
```xml
  <com.xw.repo.XEditText
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="default, just likes EditText"
      app:x_disableClear="true"/>

  <com.xw.repo.XEditText
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="clear drawable"/>

  <com.xw.repo.XEditText
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="default password input"
      android:inputType="textPassword"/>

  <com.xw.repo.XEditText
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="pwd input, custom drawables"
      android:inputType="textPassword" <!-- don't set gravity to center, center_horizontal, right or end, otherwise the ClearDrawable will not appear. -->
      app:x_clearDrawable="@mipmap/ic_clear" <!--support vector drawable-->
      app:x_hidePwdDrawable="@mipmap/ic_hide" <!--support vector drawable-->
      app:x_showPwdDrawable="@mipmap/ic_show"/> <!--support vector drawable-->

  <com.xw.repo.XEditText
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="the pattern to separate the content"
      app:x_pattern="3,4,4"
      app:x_separator=" "/>
```
**Need to listen to the focus state? Call `.setOnXTextChangeListener()` instead of `.setOnTextChangeListener()`**  
Check the sample for more details.

## License
```
The MIT License (MIT)

Copyright (c) 2016 woxingxiao

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
