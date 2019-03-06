# XEditText

## fork过来主要是为了解决被加了最大长度的属性，然后用户通过复制粘贴到控件，因为光标位置问题导致奔溃的情况，不过发现另外一个问题，暂时无法修复，就是控件加了digits不起作用

## Gradle
```groovy
    dependencies{
        compile 'com.xw.repo:xedittext:${LATEST_VERSION}@aar'
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