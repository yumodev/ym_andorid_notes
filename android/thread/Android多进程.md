## Android多个程序间进程通信

   Android跨进程通信有四种方式，分别对应四种组件，Activity、ContentProvider、Broiadcast、Service。

   * Activity跨进程通信
      Activity既可以在进程内访问，也可以跨进程访问。跨进程间的Activity访问通过隐式Intent实现的。自定义一个可以被跨进程访问的Activity，需要制定Action。
      启动一个打电话Activity如下：；
      Intent  callIntent = new Intent(Intent.ACTION_CALL,Uri.parse("tel:12345678"));
      startActivity(callIntent);
      
* ContentProvider
       Android可以通过ContentProvider实现在同一个应用程序中被访问。
       
* 广播
    
* AIDL 远程服务调用

## 一个App如何启动另外一个App

  通过一个包名启动另外一个App如下
 
```  
Intent intent = getPackageManager().getLaunchIntentForPackage(packageName);
   startActivity(intent);
```

