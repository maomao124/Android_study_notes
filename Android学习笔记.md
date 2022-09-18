<h1 style="color: #ff90fa;text-align: center;font-size:3em">Android学习笔记</h1>









---





# Android的发展历程

安卓（Android）是一种基于Linux内核（不包含GNU组件）的自由及开放源代码的操作系统。主要使用 于移动设备，如智能手机和平板电脑，由美国Google公司和开放手机联盟领导及开发。Android操作系 统最初由Andy Rubin开发，主要支持手机。

* 2005年8月由Google收购注资。 
* 2007年11月，Google与84家硬件制造商、软件开发商及电信营运商组建开放手机联盟共同研发改 良Android系统，并发布了Android的源代码。 
* 第一部Android智能手机发布于2008年10月，由 HTC 公司制造。Android逐渐扩展到平板电脑及 其他领域上，如电视、数码相机、游戏机、智能手表、车载大屏、智能家居等，并逐渐成为了人们 日常生活中不可或缺的系统软件。 
* 2011年第一季度，Android在全球的市场份额首次超过塞班系统，跃居全球第一。 
* 2013年的第四季度，Android平台手机的全球市场份额已经达到78.1%。2013年09月24日谷歌开 发的操作系统Android在迎来了5岁生日，全世界采用这款系统的设备数量已经达到10亿台。 
* 2019年，谷歌官方宣布全世界有25亿活跃的Android设备，还不包含大多数中国设备。



Android几乎每年都要发布一个大版本，技术的更新迭代非常之快



| Android 版本号 | 对应 API | 发布时间 |
| :------------: | :------: | :------: |
|Android 13 |33 |2022年2月|
|Android 12 |31 |2021年10月|
|Android 11| 30| 2020年9月|
|Android 10| 29 |2019年8月|
|Android 9| 28 |2018年8月|
|Android 8 |26/27| 2017年8月|
|Android 7| 24/25| 2016年8月|
|Android 6| 23| 2015年9月|
|Android 5 |21/22| 2014年6月|
|Android 4.4| 19/20 |2013年9月|



虽然Android基于Linux内核，但是Android手机的应用App主要采用Java语言开发。为了吸引众多的Java 程序员，早期的App开发工具使用Eclipse，通过给Eclipse安装ADT插件，使之支持开发和调试App。然 而Eclipse毕竟不是专门的App开发环境，运行速度也偏慢，因此谷歌公司在2013年5月推出了全新的 Android开发环境—Android Studio。Android Studio基于IntelliJ IDEA演变而来，既保持了IDEA方便快 捷的特点，又增加了Android开发的环境支持。自2015年之后，谷歌公司便停止了ADT的版本更新，转 而重点打造自家的Android Studio，数年升级换代下来，Android Studio的功能愈加丰富，性能也愈高 效，使得它逐步成为主流的App开发环境







# Android Studio

## 开发机配置要求

* 内存要求至少8GB，越大越好。 
* CPU要求1.5GHz以上，越快越好。 
* 硬盘要求系统盘剩余空间10GB以上，越大越好。 
* 要求带无线网卡与USB插槽。
* 必须是64位系统，不能是32位系统
* Windows系统至少为Windows 7，推荐Windows 10，不支持Windows XP





## 下载

https://developer.android.google.cn/studio/index.html



## 安装

双击下载完成的Android Studio安装程序



![image-20220917122348508](img/Android学习笔记/image-20220917122348508.png)



![image-20220917122359824](img/Android学习笔记/image-20220917122359824.png)



一直点击下一步



![image-20220917122450608](img/Android学习笔记/image-20220917122450608.png)



![image-20220917122507003](img/Android学习笔记/image-20220917122507003.png)



单击对话框右下角的Finish按钮，完成安装配置工作，同时打开Android Studio欢迎界面



![image-20220917122626877](img/Android学习笔记/image-20220917122626877.png)





## 下载Android的SDK

在Android Studio主界面，依次选择菜单Tools→SDK Manager，或者在Android Studio右上角中单击图标



![image-20220917123334724](img/Android学习笔记/image-20220917123334724.png)



![image-20220917123535758](img/Android学习笔记/image-20220917123535758.png)





SDK下载完成，可以到“我的电脑”中打开Android SDK Location指定的SDK保存路径，发现下面还有十几个目录



```sh
PS C:\Users\mao\AppData\Local\Android> ls


    目录: C:\Users\mao\AppData\Local\Android


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2022/9/15     22:08                Sdk


PS C:\Users\mao\AppData\Local\Android> cd .\Sdk\
PS C:\Users\mao\AppData\Local\Android\Sdk> ls


    目录: C:\Users\mao\AppData\Local\Android\Sdk


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2022/9/15     22:02                .downloadIntermediates
d-----         2022/9/15     22:03                .temp
d-----         2022/9/15     21:54                build-tools
d-----         2022/9/15     21:04                emulator
d-----         2022/9/15     21:02                extras
d-----         2022/9/15     22:08                fonts
d-----         2022/9/15     21:02                licenses
d-----         2022/3/12     12:57                patcher
d-----         2022/9/15     21:02                platform-tools
d-----         2022/3/12     12:59                platforms
d-----         2022/9/15     22:26                skins
d-----         2022/9/15     21:57                system-images
d-----         2022/3/12     12:58                tools
-a----         2022/9/17     12:35             16 .knownPackages


PS C:\Users\mao\AppData\Local\Android\Sdk>
```



* build-tools目录，存放各版本Android的编译工具。 
* emulator目录，存放模拟器的管理工具。 
* platforms目录，存放各版本Android的资源文件与内核JAR包android.jar。 
* platform-tools目录，存放常用的开发辅助工具，包括客户端驱动程序adb.exe、数据库管理工具 sqlite3.exe，等等。 









## 创建项目

![image-20220917124034741](img/Android学习笔记/image-20220917124034741.png)



![image-20220917124124652](img/Android学习笔记/image-20220917124124652.png)



![image-20220917124141062](img/Android学习笔记/image-20220917124141062.png)



![image-20220917124305335](img/Android学习笔记/image-20220917124305335.png)







## 创建内置模拟器

所谓模拟器，指的是在电脑上构造一个演示窗口，模拟手机屏幕的App运行效果。App通过编译之后， 只说明代码没有语法错误，若想验证App能否正确运行，还得让它在Android设备上跑起来。这个设备可 以是真实手机，也可以是电脑里的模拟器。依次选择菜单Run→Run （也可按快捷键Shift+F10），或者 选择菜单Run→Run…，在弹出的小窗中选择待运行的模块名称，Android Studio会判断当前是否存在已 经连接的设备，如果已有连接上的设备就在该设备上安装测试App。

因为一开始没有任何已连上的设备，所以运行App会报错“Error running ：No target device found.”， 意思是未找到任何目标设备。此时要先创建一个模拟器，依次选择菜单Tools→AVD Manager，或者在 Android Studio右上角的按钮中单击图标



![image-20220917124708476](img/Android学习笔记/image-20220917124708476.png)



点击创建



![image-20220917124737339](img/Android学习笔记/image-20220917124737339.png)



![image-20220917124835476](img/Android学习笔记/image-20220917124835476.png)



单击许可授权对话框的Accept选项，表示接受上述条款，再单击Next按钮跳到下一页的镜像下载对话框



等待镜像下载完成，单击右下角的Finish按钮



![image-20220917125033752](img/Android学习笔记/image-20220917125033752.png)





## 运行App

模拟器创建完成后，回到Android Studio的主界面



点击运行按钮



![image-20220917125209578](img/Android学习笔记/image-20220917125209578.png)



![image-20220917125224436](img/Android学习笔记/image-20220917125224436.png)



![image-20220917125331122](img/Android学习笔记/image-20220917125331122.png)











# 运行日志

打开logcat

查看日志：

```sh
2022-09-17 12:52:22.443 6578-6578/? I/android_projec: Late-enabling -Xcheck:jni
2022-09-17 12:52:22.529 6578-6578/? E/android_projec: Unknown bits set in runtime_flags: 0x8000
2022-09-17 12:52:22.533 6578-6578/? W/android_projec: Unexpected CPU variant for X86 using defaults: x86
2022-09-17 12:52:22.939 6578-6646/com.example.my_first_android_project D/libEGL: Emulator has host GPU support, qemu.gles is set to 1.
2022-09-17 12:52:22.939 6578-6646/com.example.my_first_android_project W/libc: Unable to set property "qemu.gles" to "1": connection failed; errno=13 (Permission denied)
2022-09-17 12:52:22.955 6578-6646/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libEGL_emulation.so
2022-09-17 12:52:22.957 6578-6646/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libGLESv1_CM_emulation.so
2022-09-17 12:52:22.961 6578-6646/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libGLESv2_emulation.so
2022-09-17 12:52:23.163 6578-6578/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/View;->computeFitSystemWindows(Landroid/graphics/Rect;Landroid/graphics/Rect;)Z (greylist, reflection, allowed)
2022-09-17 12:52:23.163 6578-6578/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/ViewGroup;->makeOptionalFitsSystemWindows()V (greylist, reflection, allowed)
2022-09-17 12:52:23.285 6578-6644/com.example.my_first_android_project D/HostConnection: HostConnection::get() New Host Connection established 0xdbd0eb40, tid 6644
2022-09-17 12:52:23.363 6578-6644/com.example.my_first_android_project D/HostConnection: HostComposition ext ANDROID_EMU_CHECKSUM_HELPER_v1 ANDROID_EMU_dma_v1 ANDROID_EMU_direct_mem ANDROID_EMU_host_composition_v1 ANDROID_EMU_host_composition_v2 ANDROID_EMU_vulkan ANDROID_EMU_deferred_vulkan_commands ANDROID_EMU_vulkan_null_optional_strings ANDROID_EMU_vulkan_create_resources_with_requirements ANDROID_EMU_YUV_Cache ANDROID_EMU_vulkan_ignored_handles ANDROID_EMU_vulkan_free_memory_sync ANDROID_EMU_vulkan_shader_float16_int8 ANDROID_EMU_vulkan_async_queue_submit ANDROID_EMU_sync_buffer_data GL_OES_vertex_array_object GL_KHR_texture_compression_astc_ldr ANDROID_EMU_host_side_tracing ANDROID_EMU_gles_max_version_2 
2022-09-17 12:52:23.375 6578-6644/com.example.my_first_android_project W/OpenGLRenderer: Failed to choose config with EGL_SWAP_BEHAVIOR_PRESERVED, retrying without...
2022-09-17 12:52:23.409 6578-6644/com.example.my_first_android_project D/EGL_emulation: eglCreateContext: 0xe7f01680: maj 2 min 0 rcv 2
2022-09-17 12:52:23.433 6578-6644/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f01680: ver 2 0 (tinfo 0xdbd508b0)
2022-09-17 12:52:23.450 6578-6644/com.example.my_first_android_project W/Gralloc3: mapper 3.x is not supported
2022-09-17 12:52:23.451 6578-6644/com.example.my_first_android_project D/HostConnection: createUnique: call
2022-09-17 12:52:23.451 6578-6644/com.example.my_first_android_project D/HostConnection: HostConnection::get() New Host Connection established 0xdbd105d0, tid 6644
2022-09-17 12:52:23.503 6578-6644/com.example.my_first_android_project D/HostConnection: HostComposition ext ANDROID_EMU_CHECKSUM_HELPER_v1 ANDROID_EMU_dma_v1 ANDROID_EMU_direct_mem ANDROID_EMU_host_composition_v1 ANDROID_EMU_host_composition_v2 ANDROID_EMU_vulkan ANDROID_EMU_deferred_vulkan_commands ANDROID_EMU_vulkan_null_optional_strings ANDROID_EMU_vulkan_create_resources_with_requirements ANDROID_EMU_YUV_Cache ANDROID_EMU_vulkan_ignored_handles ANDROID_EMU_vulkan_free_memory_sync ANDROID_EMU_vulkan_shader_float16_int8 ANDROID_EMU_vulkan_async_queue_submit ANDROID_EMU_sync_buffer_data GL_OES_vertex_array_object GL_KHR_texture_compression_astc_ldr ANDROID_EMU_host_side_tracing ANDROID_EMU_gles_max_version_2 
2022-09-17 12:52:23.503 6578-6644/com.example.my_first_android_project D/eglCodecCommon: allocate: Ask for block of size 0x1000
2022-09-17 12:52:23.503 6578-6644/com.example.my_first_android_project D/eglCodecCommon: allocate: ioctl allocate returned offset 0x3ffff6000 size 0x2000
2022-09-17 12:52:23.515 6578-6644/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f01680: ver 2 0 (tinfo 0xdbd508b0)
2022-09-17 12:52:31.588 6578-6644/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f01680: ver 2 0 (tinfo 0xdbd508b0)
2022-09-17 12:52:35.990 6578-6578/com.example.my_first_android_project W/ActivityThread: handleWindowVisibility: no activity for token android.os.BinderProxy@d5feb6c
2022-09-17 12:52:36.051 6578-6644/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f01680: ver 2 0 (tinfo 0xdbd508b0)
```



* Log.e：表示错误信息，比如可能导致程序崩溃的异常。 
* Log.w：表示警告信息。
* Log.i：表示一般消息。 
* Log.d：表示调试信息，可把程序运行时的变量值打印出来，方便跟踪调试。
* Log.v：表示冗余信息



一般而言，日常开发使用Log.d即可





虽然在模拟器上能够看到App的运行，却无法看到App的调试信息。以前写Java代码的时候，通过 System.out.println可以很方便地向IDEA的控制台输出日志，当然Android Studio也允许查看App的运 行日志，只是Android不使用System.out.println，而是采用Log工具打印日志



```java
package com.example.my_first_android_project;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d("MainActivity", "onCreate: 调试日志");
        Log.i("MainActivity", "onCreate: 日志");
        Log.w("MainActivity", "onCreate: 警告日志", new RuntimeException());
        Log.e("MainActivity", "onCreate: 错误日志", new RuntimeException());
    }

}
```



查看日志（debug级别）

![image-20220917132203194](img/Android学习笔记/image-20220917132203194.png)



```sh
2022-09-17 13:21:23.203 8137-8137/? I/android_projec: Late-enabling -Xcheck:jni
2022-09-17 13:21:23.222 8137-8137/? E/android_projec: Unknown bits set in runtime_flags: 0x8000
2022-09-17 13:21:23.224 8137-8137/? W/android_projec: Unexpected CPU variant for X86 using defaults: x86
2022-09-17 13:21:23.462 8137-8170/com.example.my_first_android_project D/libEGL: Emulator has host GPU support, qemu.gles is set to 1.
2022-09-17 13:21:23.468 8137-8170/com.example.my_first_android_project W/libc: Unable to set property "qemu.gles" to "1": connection failed; errno=13 (Permission denied)
2022-09-17 13:21:23.461 8137-8137/com.example.my_first_android_project W/RenderThread: type=1400 audit(0.0:49248): avc: denied { write } for name="property_service" dev="tmpfs" ino=8453 scontext=u:r:untrusted_app:s0:c146,c256,c512,c768 tcontext=u:object_r:property_socket:s0 tclass=sock_file permissive=0 app=com.example.my_first_android_project
2022-09-17 13:21:23.498 8137-8170/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libEGL_emulation.so
2022-09-17 13:21:23.501 8137-8170/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libGLESv1_CM_emulation.so
2022-09-17 13:21:23.507 8137-8170/com.example.my_first_android_project D/libEGL: loaded /vendor/lib/egl/libGLESv2_emulation.so
2022-09-17 13:21:23.671 8137-8137/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/View;->computeFitSystemWindows(Landroid/graphics/Rect;Landroid/graphics/Rect;)Z (greylist, reflection, allowed)
2022-09-17 13:21:23.671 8137-8137/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/ViewGroup;->makeOptionalFitsSystemWindows()V (greylist, reflection, allowed)
2022-09-17 13:21:23.747 8137-8137/com.example.my_first_android_project D/MainActivity: onCreate: 调试日志
2022-09-17 13:21:23.747 8137-8137/com.example.my_first_android_project I/MainActivity: onCreate: 日志
2022-09-17 13:21:23.749 8137-8137/com.example.my_first_android_project W/MainActivity: onCreate: 警告日志
    java.lang.RuntimeException
        at com.example.my_first_android_project.MainActivity.onCreate(MainActivity.java:19)
        at android.app.Activity.performCreate(Activity.java:7802)
        at android.app.Activity.performCreate(Activity.java:7791)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1299)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:3245)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3409)
        at android.app.servertransaction.LaunchActivityItem.execute(LaunchActivityItem.java:83)
        at android.app.servertransaction.TransactionExecutor.executeCallbacks(TransactionExecutor.java:135)
        at android.app.servertransaction.TransactionExecutor.execute(TransactionExecutor.java:95)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:2016)
        at android.os.Handler.dispatchMessage(Handler.java:107)
        at android.os.Looper.loop(Looper.java:214)
        at android.app.ActivityThread.main(ActivityThread.java:7356)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
2022-09-17 13:21:23.750 8137-8137/com.example.my_first_android_project E/MainActivity: onCreate: 错误日志
    java.lang.RuntimeException
        at com.example.my_first_android_project.MainActivity.onCreate(MainActivity.java:20)
        at android.app.Activity.performCreate(Activity.java:7802)
        at android.app.Activity.performCreate(Activity.java:7791)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1299)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:3245)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3409)
        at android.app.servertransaction.LaunchActivityItem.execute(LaunchActivityItem.java:83)
        at android.app.servertransaction.TransactionExecutor.executeCallbacks(TransactionExecutor.java:135)
        at android.app.servertransaction.TransactionExecutor.execute(TransactionExecutor.java:95)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:2016)
        at android.os.Handler.dispatchMessage(Handler.java:107)
        at android.os.Looper.loop(Looper.java:214)
        at android.app.ActivityThread.main(ActivityThread.java:7356)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
2022-09-17 13:21:23.817 8137-8168/com.example.my_first_android_project D/HostConnection: HostConnection::get() New Host Connection established 0xdbd0ec80, tid 8168
2022-09-17 13:21:23.833 8137-8168/com.example.my_first_android_project D/HostConnection: HostComposition ext ANDROID_EMU_CHECKSUM_HELPER_v1 ANDROID_EMU_dma_v1 ANDROID_EMU_direct_mem ANDROID_EMU_host_composition_v1 ANDROID_EMU_host_composition_v2 ANDROID_EMU_vulkan ANDROID_EMU_deferred_vulkan_commands ANDROID_EMU_vulkan_null_optional_strings ANDROID_EMU_vulkan_create_resources_with_requirements ANDROID_EMU_YUV_Cache ANDROID_EMU_vulkan_ignored_handles ANDROID_EMU_vulkan_free_memory_sync ANDROID_EMU_vulkan_shader_float16_int8 ANDROID_EMU_vulkan_async_queue_submit ANDROID_EMU_sync_buffer_data GL_OES_vertex_array_object GL_KHR_texture_compression_astc_ldr ANDROID_EMU_host_side_tracing ANDROID_EMU_gles_max_version_2 
2022-09-17 13:21:23.840 8137-8168/com.example.my_first_android_project W/OpenGLRenderer: Failed to choose config with EGL_SWAP_BEHAVIOR_PRESERVED, retrying without...
2022-09-17 13:21:23.875 8137-8168/com.example.my_first_android_project D/EGL_emulation: eglCreateContext: 0xe7f02280: maj 2 min 0 rcv 2
2022-09-17 13:21:23.914 8137-8168/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f02280: ver 2 0 (tinfo 0xdbd1dee0)
2022-09-17 13:21:23.923 8137-8168/com.example.my_first_android_project W/Gralloc3: mapper 3.x is not supported
2022-09-17 13:21:23.929 8137-8168/com.example.my_first_android_project D/HostConnection: createUnique: call
2022-09-17 13:21:23.929 8137-8168/com.example.my_first_android_project D/HostConnection: HostConnection::get() New Host Connection established 0xdbd10710, tid 8168
2022-09-17 13:21:23.937 8137-8168/com.example.my_first_android_project D/HostConnection: HostComposition ext ANDROID_EMU_CHECKSUM_HELPER_v1 ANDROID_EMU_dma_v1 ANDROID_EMU_direct_mem ANDROID_EMU_host_composition_v1 ANDROID_EMU_host_composition_v2 ANDROID_EMU_vulkan ANDROID_EMU_deferred_vulkan_commands ANDROID_EMU_vulkan_null_optional_strings ANDROID_EMU_vulkan_create_resources_with_requirements ANDROID_EMU_YUV_Cache ANDROID_EMU_vulkan_ignored_handles ANDROID_EMU_vulkan_free_memory_sync ANDROID_EMU_vulkan_shader_float16_int8 ANDROID_EMU_vulkan_async_queue_submit ANDROID_EMU_sync_buffer_data GL_OES_vertex_array_object GL_KHR_texture_compression_astc_ldr ANDROID_EMU_host_side_tracing ANDROID_EMU_gles_max_version_2 
2022-09-17 13:21:23.937 8137-8168/com.example.my_first_android_project D/eglCodecCommon: allocate: Ask for block of size 0x1000
2022-09-17 13:21:23.937 8137-8168/com.example.my_first_android_project D/eglCodecCommon: allocate: ioctl allocate returned offset 0x3ffff6000 size 0x2000
2022-09-17 13:21:23.946 8137-8168/com.example.my_first_android_project D/EGL_emulation: eglMakeCurrent: 0xe7f02280: ver 2 0 (tinfo 0xdbd1dee0)
```



查看日志（warn级别）

![image-20220917132258246](img/Android学习笔记/image-20220917132258246.png)



```sh
2022-09-17 13:21:23.222 8137-8137/? E/android_projec: Unknown bits set in runtime_flags: 0x8000
2022-09-17 13:21:23.224 8137-8137/? W/android_projec: Unexpected CPU variant for X86 using defaults: x86
2022-09-17 13:21:23.468 8137-8170/com.example.my_first_android_project W/libc: Unable to set property "qemu.gles" to "1": connection failed; errno=13 (Permission denied)
2022-09-17 13:21:23.461 8137-8137/com.example.my_first_android_project W/RenderThread: type=1400 audit(0.0:49248): avc: denied { write } for name="property_service" dev="tmpfs" ino=8453 scontext=u:r:untrusted_app:s0:c146,c256,c512,c768 tcontext=u:object_r:property_socket:s0 tclass=sock_file permissive=0 app=com.example.my_first_android_project
2022-09-17 13:21:23.671 8137-8137/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/View;->computeFitSystemWindows(Landroid/graphics/Rect;Landroid/graphics/Rect;)Z (greylist, reflection, allowed)
2022-09-17 13:21:23.671 8137-8137/com.example.my_first_android_project W/android_projec: Accessing hidden method Landroid/view/ViewGroup;->makeOptionalFitsSystemWindows()V (greylist, reflection, allowed)
2022-09-17 13:21:23.749 8137-8137/com.example.my_first_android_project W/MainActivity: onCreate: 警告日志
    java.lang.RuntimeException
        at com.example.my_first_android_project.MainActivity.onCreate(MainActivity.java:19)
        at android.app.Activity.performCreate(Activity.java:7802)
        at android.app.Activity.performCreate(Activity.java:7791)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1299)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:3245)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3409)
        at android.app.servertransaction.LaunchActivityItem.execute(LaunchActivityItem.java:83)
        at android.app.servertransaction.TransactionExecutor.executeCallbacks(TransactionExecutor.java:135)
        at android.app.servertransaction.TransactionExecutor.execute(TransactionExecutor.java:95)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:2016)
        at android.os.Handler.dispatchMessage(Handler.java:107)
        at android.os.Looper.loop(Looper.java:214)
        at android.app.ActivityThread.main(ActivityThread.java:7356)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
2022-09-17 13:21:23.750 8137-8137/com.example.my_first_android_project E/MainActivity: onCreate: 错误日志
    java.lang.RuntimeException
        at com.example.my_first_android_project.MainActivity.onCreate(MainActivity.java:20)
        at android.app.Activity.performCreate(Activity.java:7802)
        at android.app.Activity.performCreate(Activity.java:7791)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1299)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:3245)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:3409)
        at android.app.servertransaction.LaunchActivityItem.execute(LaunchActivityItem.java:83)
        at android.app.servertransaction.TransactionExecutor.executeCallbacks(TransactionExecutor.java:135)
        at android.app.servertransaction.TransactionExecutor.execute(TransactionExecutor.java:95)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:2016)
        at android.os.Handler.dispatchMessage(Handler.java:107)
        at android.os.Looper.loop(Looper.java:214)
        at android.app.ActivityThread.main(ActivityThread.java:7356)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.RuntimeInit$MethodAndArgsCaller.run(RuntimeInit.java:492)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:930)
2022-09-17 13:21:23.840 8137-8168/com.example.my_first_android_project W/OpenGLRenderer: Failed to choose config with EGL_SWAP_BEHAVIOR_PRESERVED, retrying without...
2022-09-17 13:21:23.923 8137-8168/com.example.my_first_android_project W/Gralloc3: mapper 3.x is not supported
```









# App开发基础

## App的运行环境

App是在手机上运行的一类应用软件，而应用软件依附于操作系统，无论电脑还是手机，刚开机都会显 示桌面，这个桌面便是操作系统的工作台。个人电脑的操作系统主要有微软的Windows和苹果的Mac OS，智能手机流行的操作系统也有两种，分别是安卓手机的Android和苹果手机的iOS。本书讲述的App 开发为Android上的应用开发，Android系统基于Linux内核，但不等于Linux系统，故App应用无法在 Linux系统上运行。



Android Studio是谷歌官方推出的App开发环境，它提供了三种操作系统的安装包，分别是Windows、 Mac和Linux。这就产生一个问题：开发者可以在电脑上安装Android Studio，并使用Android Studio开 发App项目，但是编译出来的App在电脑上跑不起来。这种情况真是令人匪夷所思的，通常学习C语言、 Java或者Python，都能在电脑的开发环境直接观看程序运行过程，就算是J2EE开发，也能在浏览器通过 网页观察程序的运行结果。可是安卓的App应用竟然没法在电脑上直接运行，那该怎样验证App的界面 展示及其业务逻辑是否正确呢？

* 为了提供App开发的功能测试环境，一种办法是利用Android Studio创建内置的模拟器，然后启动内置 模拟器，再在模拟器上运行App应用
* 另一种办法是使用真实手机测试App，该办法在实际开发中更为常见。由于模拟器本身跑在电脑上面， 占用电脑的CPU和内存，会拖累电脑的运行速度



利用真机调试要求具备以下**5个条件**：

1．**使用数据线把手机连到电脑上**

手机的电源线拔掉插头就是数据线。数据线长方形的一端接到电脑的USB接口，即可完成手机与电脑的 连接



2．**在电脑上安装手机的驱动程序**

一般电脑会把手机当作USB存储设备一样安装驱动，大多数情况会自动安装成功。如果遇到少数情况安 装失败，需要先安装手机助手，由助手软件下载并安装对应的手机驱动



3．**打开手机的开发者选项并启用USB调试**

手机出厂后默认关闭开发者选项，需要开启开发者选项才能调试App。打开手机的设置菜单，进入“系统” →“关于手机”→“版本信息”页面，这里有好几个版本项，每个版本项都使劲点击七、八下，总会有某个版 本点击后出现“你将开启开发者模式”的提示。继续点击该版本开启开发者模式，然后退出并重新进入设 置页面，此时就能在“系统”菜单下找到“开发者选项”或“开发人员选项”了。进入“开发者选项”页面，启用 “开发者选项”和“USB调试”两处开关，允许手机通过USB接口安装调试应用



4．**将连接的手机设为文件传输模式，并允许计算机进行USB调试**

手机通过USB数据线连接电脑后，请求选择某种USB连接方式。这里记得选中“传输文件”，因为充电模式不支持调试App。 选完之后手机桌面弹出确认窗口，提示开发者是否允许当前计算机进行USB调试。这里勾选“始终允许使用这台计算机进行调试”选项，再点击右下角的确定按钮，允许计算机在手机上调试App



5．手机要能正常使用

锁屏状态下，Android Studio向手机安装App的行为可能会被拦截，所以要保证手机处于解锁状态，才 能顺利通过电脑安装App到手机上。 有的手机还要求插入SIM卡才能调试App，还有的手机要求登录会员才能调试App，总之如果遇到无法安 装的问题，各种情况都尝试一遍才好。





## App的开发语言

基于安卓系统的App开发主要有两大技术路线，分别是**原生开发和混合开发**。原生开发指的是在移动平 台上利用官方提供的编程语言（例如Java、Kotlin等）、开发工具包（SDK）、开发环境（Android Studio）进行App开发；混合开发指的是结合原生与H5技术开发混合应用，也就是将部分App页面改成 内嵌的网页，这样无须升级App、只要覆盖服务器上的网页，即可动态更新App页面。



不管是原生开发还是混合开发，都要求掌握Android Studio的开发技能，因为混合开发本质上依赖于原生开发。单就原生开发而言，又涉及多种编程语 言，包括Java、Kotlin、C/C++、XML等



### Java

Java是Android开发的主要编程语言，在创建新项目时，弹出项目配置对话框，看见 Language栏默认选择了Java，表示该项目采用Java编码

虽然Android开发需要Java环境，但没要求电脑上必须事先安装JDK，因为Android Studio已经自带了 JRE

单击项目结构对话框左侧的SDK Location，对话框右边从上到下依次排列着“Android SDK location”、 “Android NDK location”、“JDK location”，其中下方的JDK location提示位于Android Studio安装路径的 JRE目录下，它正是Android Studio自带的Java运行环境



Android Studio自带的JRE使用的版本是11



```sh
PS C:\Program Files\Android Studio\jre\bin> ls


    目录: C:\Program Files\Android Studio\jre\bin


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         2022/9/15     20:56                server
-a----         2022/7/11     15:34          30024 attach.dll
-a----         2022/7/11     15:33        1566536 awt.dll
-a----         2022/7/11     15:34          37192 dt_shmem.dll
-a----         2022/7/11     15:33          34632 dt_socket.dll
-a----         2022/7/11     15:34         670024 fontmanager.dll
-a----         2022/7/11     15:34         549192 freetype.dll
-a----         2022/7/11     15:33          51528 instrument.dll
-a----         2022/7/11     15:33          51528 j2gss.dll
-a----         2022/7/11     15:33          26952 j2pcsc.dll
-a----         2022/7/11     15:34          77640 j2pkcs11.dll
-a----         2022/7/11     15:33          29000 jaas.dll
-a----         2022/7/11     15:34          45896 jabswitch.exe
-a----         2022/7/11     15:34         111944 jaccessinspector.exe
-a----         2022/7/11     15:33          72008 jaccesswalker.exe
-a----         2022/7/11     15:34          25416 jaotc.exe
-a----         2022/7/11     15:33          23880 jar.exe
-a----         2022/7/11     15:33          23880 jarsigner.exe
-a----         2022/7/11     15:34         156488 java.dll
-a----         2022/7/11     15:33          33608 java.exe
-a----         2022/7/11     15:34         158024 javaaccessbridge.dll
-a----         2022/7/11     15:34          23880 javac.exe
-a----         2022/7/11     15:33          23880 javadoc.exe
-a----         2022/7/11     15:34         170824 javajpeg.dll
-a----         2022/7/11     15:34          23880 javap.exe
-a----         2022/7/11     15:34          33608 javaw.exe
-a----         2022/7/11     15:34          21832 jawt.dll
-a----         2022/7/11     15:33          23880 jdb.exe
-a----         2022/7/11     15:33          23880 jdeprscan.exe
-a----         2022/7/11     15:34          23880 jdeps.exe
-a----         2022/7/11     15:33         218440 jdwp.dll
-a----         2022/7/11     15:33          23880 jfr.exe
-a----         2022/7/11     15:33          23880 jhsdb.exe
-a----         2022/7/11     15:34          33608 jimage.dll
-a----         2022/7/11     15:33          23880 jimage.exe
-a----         2022/7/11     15:34          23880 jjs.exe
-a----         2022/7/11     15:34          87880 jli.dll
-a----         2022/7/11     15:33          23880 jlink.exe
-a----         2022/7/11     15:34          23880 jmod.exe
-a----         2022/7/11     15:33          23880 jrunscript.exe
-a----         2022/7/11     15:33          61768 jsound.dll
-a----         2022/7/11     15:34          23872 keytool.exe
-a----         2022/7/11     15:33          23880 kinit.exe
-a----         2022/7/11     15:33          23880 klist.exe
-a----         2022/7/11     15:34          23880 ktab.exe
-a----         2022/7/11     15:33         257864 lcms.dll
-a----         2022/7/11     15:34          36168 le.dll
-a----         2022/7/11     15:34          30024 management.dll
-a----         2022/7/11     15:33          24904 management_agent.dll
-a----         2022/7/11     15:33          36680 management_ext.dll
-a----         2022/7/11     15:34         515400 mlib_image.dll
-a----         2022/7/11     15:34         627528 msvcp140.dll
-a----         2022/7/11     15:33          96072 net.dll
-a----         2022/7/11     15:34          68424 nio.dll
-a----         2022/7/11     15:33          23880 pack200.exe
-a----         2022/7/11     15:34          25928 prefs.dll
-a----         2022/7/11     15:33          21320 rmi.dll
-a----         2022/7/11     15:34          23880 rmid.exe
-a----         2022/7/11     15:34          23880 rmiregistry.exe
-a----         2022/7/11     15:33          40776 saproc.dll
-a----         2022/7/11     15:34          23880 serialver.exe
-a----         2022/7/11     15:34         218440 splashscreen.dll
-a----         2022/7/11     15:33          44872 sspi_bridge.dll
-a----         2022/7/11     15:33         151880 sunec.dll
-a----         2022/7/11     15:33          89416 unpack.dll
-a----         2022/7/11     15:33         140616 unpack200.exe
-a----         2022/7/11     15:33          82248 vcruntime140.dll
-a----         2022/7/11     15:34          56648 verify.dll
-a----         2022/7/11     15:34          32072 w2k_lsa_auth.dll
-a----         2022/7/11     15:33         196936 windowsaccessbridge-64.dll
-a----         2022/7/11     15:33          86344 zip.dll


PS C:\Program Files\Android Studio\jre\bin> pwd

Path
----
C:\Program Files\Android Studio\jre\bin


PS C:\Program Files\Android Studio\jre\bin> ./java -version
openjdk version "11.0.12" 2021-07-20
OpenJDK Runtime Environment (build 11.0.12+7-b1504.28-7817840)
OpenJDK 64-Bit Server VM (build 11.0.12+7-b1504.28-7817840, mixed mode)
PS C:\Program Files\Android Studio\jre\bin>
```





### Kotlin

Kotlin是谷歌官方力推的又一种编程语言，它与Java同样基于JVM（Java Virtual Machine，即Java虚拟 机），且完全兼容Java语言。创建新项目时，在Language栏下拉可选择Kotlin

一旦在创建新项目时选定Kotlin，该项目就会自动加载Kotlin插件，并将Kotlin作为默认的编程语言





### C/C++

不管是Java还是Kotlin，它们都属于解释型语言，这类语言在运行之时才将程序翻译成机器语言，故而执 行效率偏低。虽然现在手机配置越来越高，大多数场景的App运行都很流畅，但是涉及图像与音视频处 理等复杂运算的场合，解释型语言的性能瓶颈便暴露出来



编译型语言在首次编译时就将代码编译为机器语言，后续运行无须重新编译，直接使用之前的编译文件 即可，因此执行效率比解释型语言高。C/C++正是编译型语言的代表，它能够有效弥补解释型语言的性 能缺憾，借助于JNI技术（Java Native Interface，即Java原生接口），Java代码允许调用C/C++编写的程 序。事实上，Android的SDK开发包内部定义了许多JNI接口，包括图像读写在内的底层代码均由 C/C++编写，再由外部通过封装好的Java方法调用





### XML

XML全称为Extensible Markup Language，即可扩展标记语言，严格地说，XML并非编程语言，只是一 种标记语言。它类似于HTML，利用各种标签表达页面元素，以及各元素之间的层级关系及其排列组 合。每个XML标签都是独立的控件对象，标签内部的属性以“android:”打头，表示这是标准的安卓属 性，各属性分别代表控件的某种规格。



```xml
<TextView
android:id="@+id/tv_hello"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Hello World!" />
```



上面的标签名称为TextView，翻译过来叫文本视图，该标签携带4个属性，说明如下：

* id：控件的编号
* layout_width：控件的布局宽度，wrap_content表示刚好包住该控件的内容
* layout_height：控件的布局高度，wrap_content表示刚好包住该控件的内容
* text：控件的文本，也就是文本视图要显示什么文字



综合起来，以上XML代码所表达的意思为：这是一个名为tv_hello的文本视图，显示的文字内容是“Hello World!”，它的宽度和高度都要刚好包住这些文字







## App连接的数据库

在学习Java编程的时候，基本会学到数据库操作，通过JDBC连接数据库进行记录的增删改查，这个数据 库可能是MySQL，也可能是Oracle，还可能是SQL Server。然而手机应用不能直接操作上述几种数据 库，因为数据库软件也得像应用软件那样安装到操作系统上，比如MySQL提供了Windows系统的安装 包，也提供了Linux系统的安装包，可是它没有提供Android系统的安装包呢，所以MySQL没法在 Android系统上安装，手机里面的App也就不能直连MySQL。



既然MySQL、Oracle这些企业数据库无法在手机安装，那么App怎样管理业务方面的数据记录呢？其实 Android早已内置了专门的数据库名为SQLite，它遵循关系数据库的设计理念，SQL语法类似于 MySQL。不同之处在于，SQLite无须单独安装，因为它内嵌到应用进程当中，所以App无须配置连接信 息，即可直接对其增删改查。由于SQLite嵌入到应用程序，省去了配置数据库服务器的开销，因此它又 被归类为嵌入式数据库。



可是SQLite的数据库文件保存在手机上，开发者拿不到用户的手机，又该如何获取App存储的业务数 据？比如用户的注册信息、用户的购物记录，等等。如果像Java Web那样，业务数据统一保存在后端的 数据库服务器，开发者只要登录数据库服务器，就能方便地查询导出需要的记录信息



手机端的App，连同程序代码及其内置的嵌入式数据库，其实是个又独立又完整的程序实体，它只负责 手机上的用户交互与信息处理，该实体被称作客户端。而后端的Java Web服务，包括Web代码和数据库 服务器，同样构成另一个单独运行的程序实体，它只负责后台的业务逻辑与数据库操作，该实体被称作 服务端。客户端与服务端之前通过HTTP接口通信，每当客户端觉得需要把信息发给服务端，或者需要从 服务端获取信息时，客户端便向服务端发起HTTP请求，服务端收到客户端的请求之后，根据规则完成数 据处理，并将处理结果返回给客户端。这样客户端经由HTTP接口并借服务端之手，方能间接读写后端的 数据库服务器（如MySQL）



![image-20220917141729775](img/Android学习笔记/image-20220917141729775.png)



由此看来，一个具备用户管理功能的App系统，实际上并不单单只是手机上的一个应用，还包括与其对 应的Java Web服务。手机里的客户端App，面向的是手机用户，App与用户之间通过手机屏幕交互；而 后端的服务程序，面向的是手机App，客户端与服务端之间通过HTTP接口交互。客



![image-20220917141816844](img/Android学习笔记/image-20220917141816844.png)







## App工程目录结构



![image-20220917142003638](img/Android学习笔记/image-20220917142003638.png)



![image-20220917142223433](img/Android学习笔记/image-20220917142223433.png)



App工程分为两个层次，第一个层次是项目，依次选择菜单File→New→New Project即可创建新项目。 另一个层次是模块，模块依附于项目，每个项目至少有一个模块，也能拥有多个模块，依次选择菜单 File→New→New Module即可在当前项目创建新模块。一般所言的“编译运行App”，指的是运行某个模 块，而非运行某个项目，因为模块才对应实际的App。



该项目下面有两个分类：一个是app（代表app模块）；另一个是Gradle Scripts。



![image-20220917142401137](img/Android学习笔记/image-20220917142401137.png)



其中，app下面又有3个子目录：

* manifests子目录，下面只有一个XML文件，即AndroidManifest.xml，它是App的运行配置文 件
* java子目录，下面有3个包，其中第一个包存放当前模块的Java源代码，后 面两个包存放测试用的Java代码
* res子目录，存放当前模块的资源文件。res下面又有4个子目录
  * drawable目录存放图形描述文件与图片文件
  * layout目录存放App页面的布局文件
  * mipmap目录存放App的启动图标
  * values目录存放一些常量定义文件，例如字符串常量strings.xml、像素常量dimens.xml、颜色常 量colors.xml、样式风格定义styles.xml等





Gradle Scripts下面主要是工程的编译配置文件，主要有：

* build.gradle，该文件分为项目级与模块级两种，用于描述App工程的编译规则
* proguard-rules.pro，该文件用于描述Java代码的混淆规则
* gradle.properties，该文件用于配置编译工程的命令行参数，一般无须改动
* settings.gradle，该文件配置了需要编译哪些模块。初始内容为include ':app'，表示只编译app模块
* local.properties，项目的本地配置文件，它在工程编译时自动生成，用于描述开发者电脑的环境 配置，包括SDK的本地路径、NDK的本地路径等





### 编译配置文件build.gradle

新创建的App项目默认有两个build.gradle，一个是Project项目级别的build.gradle；另一个是Module 模块级别的build.gradle



项目级别的build.gradle指定了当前项目的总体编译规则，打开该文件在buildscript下面找到 repositories和dependencies两个节点，其中repositories节点用于设置Android Studio插件的网络仓 库地址，而dependencies节点用于设置gradle插件的版本号。由于官方的谷歌仓库位于国外，下载速度 相对较慢，因此可在repositories节点添加阿里云的仓库地址，方便国内开发者下载相关插件。



```
// Top-level build file where you can add configuration options common to all sub-projects/modules.
plugins {
    //插件
    id 'com.android.application' version '7.2.2' apply false
    id 'com.android.library' version '7.2.2' apply false
}

//任务
task clean(type: Delete) {
    delete rootProject.buildDir
}
```





模块级别的build.gradle对应于具体模块，每个模块都有自己的build.gradle，它指定了当前模块的详细编译规则

```
//插件
plugins {
    id 'com.android.application'
}

android {
    // 指定编译用的SDK版本号
    compileSdk 32

    defaultConfig {
        // 指定该模块的应用编号，也就是App的包名
        applicationId "com.example.my_first_android_project"
        // 指定App适合运行的最小SDK版本号
        minSdk 25
        // 指定目标设备的SDK版本号。表示App最希望在哪个版本的Android上运行
        targetSdk 32
        // 指定App的应用版本号
        versionCode 1
        // 指定App的应用版本名称
        versionName "1.0"

        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}

// 指定App编译的依赖信息
dependencies {

    // 指定引用jar包的路径
    //implementation fileTree(dir: 'libs', include: ['*.jar'])
    // 指定编译Android的高版本支持库
    implementation 'androidx.appcompat:appcompat:1.3.0'
    implementation 'com.google.android.material:material:1.4.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.0.4'
    // 指定单元测试编译用的junit版本号
    testImplementation 'junit:junit:4.13.2'
    androidTestImplementation 'androidx.test.ext:junit:1.1.3'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.4.0'
}
```





### AndroidManifest.xml

AndroidManifest.xml指定了App的运行配置信息，它是一个XML描述文件



```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.example.my_first_android_project">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.My_first_android_project"
        tools:targetApi="31">

        <!-- activity节点指定了该App拥有的活动页面信息，其中拥有android.intent.action.MAIN的activity说明它是入口页面 -->
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```



AndroidManifest.xml的根节点为manifest，它的package属性指定了该App的包名。manifest下面有个application节点，它的各属性说明如下：

* android:allowBackup，是否允许应用备份。允许用户备份系统应用和第三方应用的apk安装包和应用数据，以便在刷机或者数据丢失后恢复应用，用户即可通过adb backup和adb restore来进行对应用数据的备份和恢复。为true表示允许，为false则表示不允许。
* android:icon，指定App在手机屏幕上显示的图标
* android:label，指定App在手机屏幕上显示的名称。
* android:roundIcon，指定App的圆角图标。
* android:supportsRtl，是否支持阿拉伯语／波斯语这种从右往左的文字排列顺序。为true表示支持，为false则表示不支持。
* android:theme，指定App的显示风格。



application下面还有个activity节点，它是活动页面的注册声明，只有在AndroidManifest.xml中 正确配置了activity节点，才能在运行时访问对应的活动页面。初始配置的MainActivity正是App的默认 主页，之所以说该页面是App主页，是因为它的activity节点内部还配置了以下的过滤信息：

```xml
 <intent-filter>
         <action android:name="android.intent.action.MAIN" />
         <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
```

其中action节点设置的android.intent.action.MAIN表示该页面是App的入口页面，启动App时会最先打 开该页面。

而category节点设置的android.intent.category.LAUNCHER决定了是否在手机屏幕上显示 App图标，如果同时有两个activity节点内部都设置了android.intent.category.LAUNCHER，那么桌面就 会显示两个App图标







## App的设计规范

App将看得见的界面设计与看不见的代码逻辑区分开，然后 利用XML标记描绘应用界面，同时使用Java代码书写程序逻辑，从而形成App前后端分离的设计规约， 有利于提高App集成的灵活性



### 界面设计与代码逻辑

手机的功能越来越强大，某种意义上相当于微型电脑，比如打开一个电商App，仿佛是在电脑上浏览网 站。网站分为用户看得到的网页，以及用户看不到的Web后台；App也分为用户看得到的界面，以及用 户看不到的App后台。虽然Android允许使用Java代码描绘界面，但不提倡这么做，推荐的做法是将界面 设计从Java代码剥离出来，通过单独的XML文件定义界面布局



把界面设计与代码逻辑分开，不仅参考了网站的Web前后端分离，还有下列几点好处：

* 使用XML文件描述App界面，可以很方便地在Android Studio上预览界面效果。比如新创建的App 项目，默认首页布局为activity_main.xml，单击界面右上角的Design按钮，即可看到预览界面。如果XML文件修改了Hello World的文字内容，立刻就能在预览区域观看最新界面。倘若使用Java代码描 绘界面，那么必须运行App才能看到App界面
* 一个界面布局可以被多处代码复用，比如看图界面，既能通过商城购物代码浏览商品图片，也能通过商品评价代码浏览买家晒单
* 反过来，一段Java代码也可能适配多个界面布局，比如手机有竖屏与横屏两种模式，默认情况App采用同一套布局，然而在竖屏时很紧凑的界面布局，切换到横屏往往变得松垮乃至变形。鉴于竖屏与横屏遵照一样的业务逻辑，仅仅是屏幕方向不同，若要调整的话，只需分别给出竖屏时候的 界面布局，以及横屏时候的界面布局。因为用户多数习惯竖屏浏览，所以res/layout目录下放置的XML 文件默认为竖屏规格，另外在res下面新建名为layout-land的目录，用来存放横屏规格的XML文件。 land是landscape的缩写，意思是横向，Android把layout-land作为横屏XML的专用布局目录。然后在 layout-land目录创建与原XML同名的XML文件，并重新编排界面控件的展示方位，调整后的横屏界面，从而有效适配了屏幕的水平方向



![image-20220917191736913](img/Android学习笔记/image-20220917191736913.png)







### 利用XML标记描绘应用界面

```xml
<TextView
android:id="@+id/tv_hello"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Hello World!" />
```



TextView标签以“<”开头，以“/>”结尾，为何尾巴多了个斜杆呢？要是没有斜杆，以左右尖括号包 裹标签名称，岂不更好？其实这是XML的标记规范，凡是XML标签都由标签头与标签尾组成，标签头以 左右尖括号包裹标签名称，形如“”；标签尾在左尖括号后面插入斜杆，以此同标签头区分开，形如“”。标 签头允许在标签名称后面添加各种属性取值，而标签尾不允许添加任何属性，因此上述TextView标签的 完整XML定义是下面这样的：

```xml
<TextView
android:id="@+id/tv_hello"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="Hello World!">
</TextView>
```

考虑到TextView仅仅是个文本视图，其标签头和标签尾之间不会插入其他标记，所以合并它的标签头和 标签尾，也就是让TextView标签以“/>”结尾，表示该标签到此为止

然而不是所有情况都能采取简化写法，简写只适用于TextView控件这种末梢节点。好比一棵大树，大树 先有树干，树干分岔出树枝，一些大树枝又分出小树枝，树枝再长出末端的树叶。一个界面也是先有根 节点（相当于树干），根节点下面挂着若干布局节点（相当于树枝），布局节点下面再挂着控件节点 （相当于树叶）。因为树叶已经是末梢了，不会再包含其他节点，所以末梢节点允许采用“/>”这种简写方式。



* 每个界面只有一个根节点，却可能有多个布局节点，也可能没有中间的布局节点，此时所有控件节点都挂在根节点下面
* 根节点必须配备“xmlns:android="http://schemas.android.com/apk/res/android"”，表示指定 XML内部的命名空间，有了这个命名空间，Android Studio会自动检查各节点的属性名称是否合法，如 果不合法就提示报错。至于布局节点就不能再指定命名空间





### 使用Java代码书写程序逻辑

在XML文件中定义界面布局，已经明确是可行的了，然而这只是静态界面，倘若要求在App运行时修改 文字内容，该当如何是好？倘若是动态变更网页内容，还能在HTML文件中嵌入JavaScript代码，由js片 段操作Web控件。但Android的XML文件仅仅是布局标记，不能再嵌入其他语言的代码了，也就是说， 只靠XML文件自身无法动态刷新某个控件



XML固然表达不了复杂的业务逻辑，这副重担就得交给App后台的Java代码了。Android Studio每次创 建新项目，除了生成默认的首页布局activity_main.xml之外，还会生成与其对应的代码文件 MainActivity.java

```java
package com.example.my_first_android_project;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d("MainActivity", "onCreate: 调试日志");
        Log.i("MainActivity", "onCreate: 日志");
        Log.w("MainActivity", "onCreate: 警告日志", new RuntimeException());
        Log.e("MainActivity", "onCreate: 错误日志", new RuntimeException());
    }
}
```



可见MainActivity.java的代码内容很简单，只有一个MainActivity类，该类下面只有一个onCreate方 法。注意onCreate内部的setContentView方法直接引用了布局文件的名字activity_main，该方法的意 思是往当前活动界面填充activity_main.xml的布局内容。现在准备在这里改动，把文字内容改成中文。 首先打开activity_main.xml，在TextView节点下方补充一行android:id="@+id/tv_hello"，表示给它起 个名字编号；然后回到MainActivity.java，在setContentView方法下面补充几行代码

```xml
    <TextView
            android:id="@+id/tv_hello"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            app:layout_constraintVertical_bias="0.55" />
```



```java
package com.example.my_first_android_project;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d("MainActivity", "onCreate: 调试日志");
        Log.i("MainActivity", "onCreate: 日志");
        Log.w("MainActivity", "onCreate: 警告日志", new RuntimeException());
        Log.e("MainActivity", "onCreate: 错误日志", new RuntimeException());

        TextView TextView = this.findViewById(R.id.tv_hello);
        TextView.setText("你好，世界！");
    }
}
```



新增的两行代码主要做了这些事情：先调用findViewById方法，从布局文件中取出名为tv_hello的 TextView控件；再调用控件对象的setText方法，为其设置新的文字内容



![image-20220917193119074](img/Android学习笔记/image-20220917193119074.png)





## App的活动页面

### 创建新的App页面

#### **1．创建XML文件**

在Android Studio左上方找到项目结构图，右击res目录下面的layout，弹出右键菜单



![image-20220917193548334](img/Android学习笔记/image-20220917193548334.png)



![image-20220917193618147](img/Android学习笔记/image-20220917193618147.png)



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

</LinearLayout>
```





#### **2．创建Java代码**

同样在Android Studio左上方找到项目结构图，右击java目录下面的包名，弹出右键菜单



![image-20220917193901980](img/Android学习笔记/image-20220917193901980.png)



![image-20220917193918049](img/Android学习笔记/image-20220917193918049.png)





```java
package com.example.my_first_android_project;


import android.os.Bundle;


import androidx.annotation.Nullable;
import androidx.appcompat.app.AppCompatActivity;

/**
 * Project name(项目名称)：my_first_android_project
 * Package(包名): com.example.my_first_android_project
 * Class(类名): Main2
 * Author(作者）: mao
 * Author QQ：1296193245
 * GitHub：https://github.com/maomao124/
 * Date(创建日期)： 2022/9/17
 * Time(创建时间)： 19:39
 * Version(版本): 1.0
 * Description(描述)： 无
 */

public class Main2 extends AppCompatActivity
{
    @Override
    public void onCreate(@Nullable Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.layout2);
    }
}
```





#### **3．注册页面配置**

创建好了页面的XML文件及其Java代码，还得在项目中注册该页面，打开AndroidManifest.xml，在 application节点内部补充如下一行配置：

```xml
<activity android:name=".Main2">

</activity>
```

添加了上面这行配置，表示给该页面注册身份，否则App运行时打开页面会提示错误“activity not found”。如果activity的标记头与标记尾中间没有其他内容





### 快速生成页面源码

经过创建XML文件、创建Java代码、注册页面配置3个步骤，就算创建好了一个新页面，没想到 区区一个页面也这么费事，怎样才能提高开发效率呢？其实Android Studio早已集成了快速创建页面的 功能，只要一个对话框就能完成所有操作



右键菜单中依次选择New→Activity→Empty Activity

![image-20220917195154902](img/Android学习笔记/image-20220917195154902.png)





![image-20220917195302587](img/Android学习笔记/image-20220917195302587.png)



回到Android Studio左上方的项目结构图，发现res的layout目录下多了个activity_main3.xml，同时 java目录下多了个MainActivity3，并且MainActivity3代码已经设定了加载activity_main3布局。接着打开AndroidManifest.xml，找到application节点发现多了下面这行配置：

```xml
<activity
android:name=".MainActivity3"
android:exported="false" />
```







### 跳到另一个页面

一旦创建好新页面，就得在合适的时候跳到该页面，假设出发页面为A，到达页面为B，那么跳转动作是 从A跳到B。由于启动App会自动打开默认主页MainActivity，因此跳跃的起点理所当然在MainActivity， 跳跃的终点则为目标页面的Activity。这种跳转动作翻译为Android代码，格式形如“startActivity(new Intent(源页面.this, 目标页面.class));”。如果目标页面名为MainActivity3，跳转代码便是下面这样的：

```java
// 活动页面跳转，从MainActivity跳到MainActivity3
startActivity(new Intent(MainActivity.this, MainActivity3.class));
```



因为跳转动作通常发生在当前页面，也就是从当前页面跳到其他页面，所以不产生歧义的话，可以使用 this指代当前页面



activity_main.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center">

    <TextView
            android:id="@+id/tv_hello"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            app:layout_constraintVertical_bias="0.55" />

    <Button
            android:id="@+id/button1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="点击跳转到第二个页面"
            tools:ignore="MissingConstraints" />

    <Button
            android:id="@+id/button2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="点击跳转到第三个页面"
            tools:ignore="MissingConstraints"
            tools:layout_editor_absoluteY="62dp"
            tools:layout_editor_absoluteX="0dp" />


</LinearLayout>
```



layout2.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:gravity="center"
        android:background="#cccccc">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ff00ff00"
            android:textSize="36sp"
            android:text="第二个页面"/>

</LinearLayout>
```



activity_main3.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity3"
        android:gravity="center"
        android:background="#222222">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ff00ff"
            android:textSize="36sp"
            android:text="第三个页面" />

</LinearLayout>
```



MainActivity

```java
package com.example.my_first_android_project;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d("MainActivity", "onCreate: 调试日志");
        Log.i("MainActivity", "onCreate: 日志");
        Log.w("MainActivity", "onCreate: 警告日志", new RuntimeException());
        Log.e("MainActivity", "onCreate: 错误日志", new RuntimeException());

        TextView TextView = this.findViewById(R.id.tv_hello);
        TextView.setText("你好，世界！");

        Button button1 = findViewById(R.id.button1);
        Button button2 = findViewById(R.id.button2);
        button1.setOnClickListener(new View.OnClickListener()
        {
            @Override
            public void onClick(View view)
            {
                startActivity(new Intent(MainActivity.this, Main2.class));
            }
        });
        button2.setOnClickListener(new View.OnClickListener()
        {
            @Override
            public void onClick(View view)
            {
                startActivity(new Intent(MainActivity.this, MainActivity3.class));
            }
        });

    }


}
```





运行：

![image-20220917203805364](img/Android学习笔记/image-20220917203805364.png)



![image-20220917203815653](img/Android学习笔记/image-20220917203815653.png)



![image-20220917203825162](img/Android学习笔记/image-20220917203825162.png)













# 简单控件

## 文本显示

### 设置文本的内容

方式一：通过属性android:text设置文本



```xml
    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="通过属性android:text设置文本"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />
```



方式二：在Java代码中调用文本视图对象的setText方法设置文本



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="通过属性android:text设置文本"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:id="@+id/test"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ff0000"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

</LinearLayout>
```



```java
package mao.android_set_text_content;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @SuppressLint("SetTextI18n")
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView = findViewById(R.id.test);
        textView.setText("在Java代码中调用文本视图对象的setText方法设置文本");
    }
}
```





![image-20220917210611958](img/Android学习笔记/image-20220917210611958.png)



意思说这几个字是硬 编码的字符串，建议使用来自@string的资源。Android Studio不推荐在XML布局文件里直接写字符串，因为可能有好几个页面都显示“a”，若想把这句话换成“b”，就得一个一个XML 文件改过去，无疑费时费力。故而Android Studio推荐把字符串放到专门的地方管理，这个名为@string 的地方位于res/values目录下的strings.xml



```xml
<resources>
    <string name="app_name">android_set_text_content</string>
    <string name="text">来自strings.xml的文本</string>
</resources>
```



添加完新的字符串定义，回到XML布局文件，将android:text属性值改为“@string/字符串名”



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="通过属性android:text设置文本"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:id="@+id/test"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ff0000"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/text"
            android:textColor="#5fffff"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />
</LinearLayout>
```





若要在Java代码中引用字符串资源，则调用setText方法时填写形如“R.string.字符串名”的参数



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center">

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="通过属性android:text设置文本"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:id="@+id/test"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ff0000"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/text"
            android:textColor="#5fffff"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />

    <TextView
            android:id="@+id/text2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#5fccfc"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textSize="20sp" />
</LinearLayout>
```



```java
package mao.android_set_text_content;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @SuppressLint("SetTextI18n")
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView = findViewById(R.id.test);
        textView.setText("在Java代码中调用文本视图对象的setText方法设置文本");

        TextView textView2 = findViewById(R.id.text2);
        textView2.setText(R.string.text);
    }
}
```



运行：

![image-20220917211413888](img/Android学习笔记/image-20220917211413888.png)







### 设置文本的大小

TextView允许设置文本内容，也允许设置文本大小，在Java代码中调用setTextSize方法，即可指定文本大小

这里的大小数值越大，则看到的文本也越大；大小数值越小，则看到的文本也越小。在XML文件中则通 过属性android:textSize指定文本大小

文本大小存在不同的字号单位，XML文件要求在字号数字后面写明单位类型，常见的字号单位主要 有px、dp、sp 3种



#### px

px是手机屏幕的最小显示单位，它与设备的显示屏有关。一般来说，同样尺寸的屏幕（比如6英寸手 机），如果看起来越清晰，则表示像素密度越高，以px计量的分辨率也越大



#### dp

dp有时也写作dip，指的是与设备无关的显示单位，它只与屏幕的尺寸有关。一般来说，同样尺寸的屏 幕以dp计量的分辨率是相同的，比如同样是6英寸手机，无论它由哪个厂家生产，其分辨率换算成dp单位都是一个大小



#### sp

sp的原理跟dp差不多，但它专门用来设置字体大小。手机在系统设置里可以调整字体的大小（小、标 准、大、超大）。设置普通字体时，同数值dp和sp的文字看起来一样大；如果设置为大字体，用dp设置 的文字没有变化，用sp设置的文字就变大了。 字体大小采用不同单位的话，显示的文字大小各不相同。例如，30px、30dp、30sp这3个字号，在不同 手机上的显示大小有所差异。有的手机像素密度较低，一个dp相当于两个px，此时30px等同于15dp； 有的手机像素密度较高，一个dp相当于3个px，此时30px等同于10dp。假设某个App的内部文本使用字 号30px，则该App安装到前一部手机的字体大小为15dp，安装到后一部手机的字体大小为10dp，显然 后一部手机显示的文本会更小。





```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:gravity="center"
        android:padding="5dp"
        android:orientation="vertical">

    <TextView
            android:id="@+id/tv_px"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="你好，世界（px大小）"
            android:textSize="30px" />

    <TextView
            android:id="@+id/tv_dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="你好，世界（dp大小）"
            android:textSize="30dp" />

    <TextView
            android:id="@+id/tv_sp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="你好，世界（sp大小）"
            android:textSize="30sp" />


</LinearLayout>
```





![image-20220917213210015](img/Android学习笔记/image-20220917213210015.png)



接着打开手机的设置菜单，依次选择“显示”→“字体与显示大小” 调整字体大小



![image-20220917213330373](img/Android学习笔记/image-20220917213330373.png)



![image-20220917213356649](img/Android学习笔记/image-20220917213356649.png)



发现字号单位30px和30dp的文字大小不变，而30sp的文字随着系统字体一起变大了



纯数字的setTextSize方法，内部默认字号单位为sp（COMPLEX_UNIT_SP）





| 名称 | 解释 |
| ---- | ---- |
|px（Pixel像素）|也称为图像元素，是作为图像构成的基本单元，单个像素的大小并不固定，跟随屏幕大小和素数量的关系变化，一个像素点为1px。|
|Resolution（分辨率）|是指屏幕的垂直和水平方向的像素数量，如果分辨率是 1920*1080 ，那是垂直方向有 1920 个像素，水平方向有 1080 个像素。|
|Dpi（像素密度） |是指屏幕上每英寸（1英寸 = 2.54 厘米）距离中有多少个像素点。|
|Density（密度） |是指屏幕上每平方英寸（2.54 ^ 2 平方厘米）中含有的像素点数量。|
|Dip / dp (设备独立像素)|也可以叫做dp，长度单位，同一个单位在不同的设备上有不同的显示效果，具体效果根据设备的密度有关，|





#### 计算规则

以一个 4.95 英寸 1920 * 1080 的 nexus5 手机设备为例

**Dpi :**

1. 计算直角边像素数量： 1920^2+1080^2=2202^2（勾股定理）。 

2. 计算 DPI：2202 / 4.95 = 445。 
3. 得到这个设备的 DPI 为 445 （每英寸的距离中有 445 个像素）。



**Density：**

上面得到每英寸中有 445 像素，那么 density 为每平方英寸中的像素数量，应该为： 445^2=198025



**Dip：**

所有显示到屏幕上的图像都是以 px 为单位，Dip 是我们开发中使用的长度单位，最后他也需要转换成 px，计算这个设备上 1dip 等于多少 px：

**px = dip x dpi /160**

320 x 480分辨率，3.6寸的手机：dpi为160，1dp=1px





* **对于相同分辨率的手机，屏幕越大，同DP的组件占用屏幕比例越小**
* **对于相同尺寸的手机，即使分辨率不同，同DP的组件占用屏幕比例也相同**



dp的UI效果只在相同尺寸的屏幕上相同，如果屏幕尺寸差异过大，则需要重做dp适配





```xml
<TextView
        android:id="@+id/tv_sp2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="你好，世界（sp大小）"
        android:textSize="30sp" />
```

```java
package mao.android_set_text_size;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView = findViewById(R.id.tv_sp2);
        textView.setTextSize(28);
    }
}
```



源码

```java
/**
 * Set the default text size to the given value, interpreted as "scaled
 * pixel" units.  This size is adjusted based on the current density and
 * user font size preference.
 *
 * <p>Note: if this TextView has the auto-size feature enabled than this function is no-op.
 *
 * @param size The scaled pixel size.
 *
 * @attr ref android.R.styleable#TextView_textSize
 */
@android.view.RemotableViewMethod
public void setTextSize(float size) {
    setTextSize(TypedValue.COMPLEX_UNIT_SP, size);
}
```



![image-20220917220128390](img/Android学习笔记/image-20220917220128390.png)









### 设置文本的颜色

除了设置文字大小，文字颜色也经常需要修改，毕竟Android默认的灰色文字不够醒目。在Java代码中调 用setTextColor方法即可设置文本颜色，具体在Color类中定义了12种颜色



![image-20220918103922626](img/Android学习笔记/image-20220918103922626.png)



```java
package mao.android_set_text_color;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView1 = findViewById(R.id.t1);
        textView1.setTextColor(Color.RED);
        textView1.setTextSize(30);
    }
}
```



可是XML文件无法引用Color类的颜色常量，为此Android制定了一套规范的编码标准，将色值交由透明 度alpha和RGB三原色（红色red、绿色green、蓝色blue）联合定义。该标准又有八位十六进制数与六 位十六进制数两种表达方式，例如八位编码FFEEDDCC中，FF表示透明度，EE表示红色的浓度，DD表示 绿色的浓度，CC表示蓝色的浓度。透明度为FF表示完全不透明，为00表示完全透明。RGB三色的数值越 大，表示颜色越浓，也就越暗；数值越小，表示颜色越淡，也就越亮。RGB亮到极致就是白色，暗到极 致就是黑色。



至于六位十六进制编码，则有两种情况，它在XML文件中默认不透明（等价于透明度为FF），而在代码 中默认透明（等价于透明度为00）。以下代码给两个文本视图分别设置六位色值与八位色值，注意添加 0x前缀表示十六进制数



```java
package mao.android_set_text_color;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView1 = findViewById(R.id.t1);
        textView1.setTextColor(Color.RED);
        textView1.setTextSize(30);
        TextView textView3 = findViewById(R.id.t3);
        textView3.setTextColor(0xffffff);
    }
}
```



运行测试App，发现控件的文本不见了，其实是变透明了



在XML文件中可通过属性android:textColor设置文字颜色，但要给色值添加井号前缀“#”，设定好文本颜色



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center"
        android:background="#cc00aa">

    <TextView
            android:id="@+id/t1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World2!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textColor="#ffffff"/>

    <TextView
            android:id="@+id/t3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World3!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />


</LinearLayout>
```



就像字符串资源那样，Android把颜色也当作一种资源，打开res/values目录下的colors.xml



```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="purple_200">#FFBB86FC</color>
    <color name="purple_500">#FF6200EE</color>
    <color name="purple_700">#FF3700B3</color>
    <color name="teal_200">#FF03DAC5</color>
    <color name="teal_700">#FF018786</color>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
</resources>
```



然后回到XML布局文件，把android:textColor的属性值改为“@color/颜色名称”



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center"
        android:background="#cc00aa">

    <TextView
            android:id="@+id/t1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World2!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textColor="#ffffff"/>

    <TextView
            android:id="@+id/t3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World3!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World4!"
            android:textColor="@color/purple_200"
            android:textSize="24sp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

</LinearLayout>
```





不仅文字颜色，还有背景颜色也会用到上述的色值定义，在XML文件中通过属性android:background设 置控件的背景颜色。Java代码则有两种方式设置背景颜色，倘若色值来源于Color类或十六进制数，则调 用setBackgroundColor方法设置背景；倘若色值来源于colors.xml中的颜色资源，则调用 setBackgroundResource方法，以“R.color.颜色名称”的格式设置背景。



```java
package mao.android_set_text_color;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.graphics.Color;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @SuppressLint("ResourceAsColor")
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView1 = findViewById(R.id.t1);
        textView1.setTextColor(Color.RED);
        textView1.setTextSize(30);
        TextView textView3 = findViewById(R.id.t3);
        textView3.setTextColor(0xffffff);
        TextView textView5 = findViewById(R.id.t5);
        textView5.setTextColor(R.color.teal_200);
    }
}
```



注意属性android:background和setBackgroundResource方法，它俩用来设置控件的背景，不单单是 背景颜色，还包括背景图片。在设置背景图片之前，先将图片文件放到res/drawable***目录（以 drawable开头的目录，不仅仅是drawable目录），然后把android:background的属性值改为 “@drawable/不含扩展名的图片名称”，或者调用setBackgroundResource方法填入“R.drawable.不含扩 展名的图片名称”。





Color类还有很多方法



![image-20220918105753912](img/Android学习笔记/image-20220918105753912.png)



![image-20220918105814990](img/Android学习笔记/image-20220918105814990.png)



![image-20220918105830889](img/Android学习笔记/image-20220918105830889.png)



![image-20220918105903213](img/Android学习笔记/image-20220918105903213.png)



![image-20220918105922815](img/Android学习笔记/image-20220918105922815.png)





```java
package mao.android_set_text_color;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.graphics.Color;
import android.os.Bundle;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @SuppressLint("ResourceAsColor")
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView1 = findViewById(R.id.t1);
        textView1.setTextColor(Color.RED);
        textView1.setTextSize(30);
        TextView textView3 = findViewById(R.id.t3);
        textView3.setTextColor(0xffffff);
        TextView textView5 = findViewById(R.id.t5);
        textView5.setTextColor(R.color.teal_200);
        TextView textView6 = findViewById(R.id.t6);
        //从红色、绿色、蓝色分量返回一个 color-int。
        // alpha 分量隐式为 255（完全不透明）。
        // 这些组件值应该是\([0..255]\)，但是没有执行范围检查，
        // 所以如果它们超出范围，则返回的颜色是未定义的
        textView6.setTextColor(Color.rgb(0,255,0));
    }
}
```



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center"
        android:background="#cc00aa">

    <TextView
            android:id="@+id/t1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World2!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            android:textColor="#ffffff"/>

    <TextView
            android:id="@+id/t3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World3!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World4!"
            android:textColor="@color/purple_200"
            android:textSize="24sp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t5"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World5!"
            android:textSize="24sp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    <TextView
            android:id="@+id/t6"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World6!"
            android:textSize="24sp"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />
</LinearLayout>
```





![image-20220918110208896](img/Android学习笔记/image-20220918110208896.png)









## 视图基础

### 设置视图的宽高

手机屏幕是块长方形区域，较短的那条边叫作宽，较长的那条边叫作高。App控件通常也是长方形状， 控件宽度通过属性android:layout_width表达，控件高度通过属性android:layout_height表达，宽高的 取值主要有下列3种：

* match_parent：表示与上级视图保持一致。上级视图的尺寸有多大，当前视图的尺寸就有多大。
* wrap_content：表示与内容自适应。对于文本视图来说，内部文字需要多大的显示空间，当前视 图就要占据多大的尺寸。但最宽不能超过上级视图的宽度，一旦超过就要换行；最高不能超过上级视图 的高度，一旦超过就会隐藏。

* 以dp为单位的具体尺寸，比如300dp，表示宽度或者高度就是这么大。



在XML文件中采用以上任一方式均可设置视图的宽高，但在Java代码中设置宽高就有点复杂了，首先确 保XML中的宽高属性值为wrap_content，这样才允许在代码中修改宽高。接着打开该页面对应的Java代 码，依序执行以下3个步骤：

* 步骤一，调用控件对象的getLayoutParams方法，获取该控件的布局参数，参数类型为 ViewGroup.LayoutParams
* 步骤二，布局参数的width属性表示宽度，height属性表示高度，修改这两个属性值，即可调整控件的宽高
* 步骤三，调用控件对象的setLayoutParams方法，填入修改后的布局参数使之生效

不过布局参数的width和height两个数值默认是px单位，需要将dp单位的数值转换为px单位的数值，然后才能赋值给width属性和height属性。



```java
package mao.android_set_width_and_height_of_the_view;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Context;
import android.os.Bundle;
import android.view.ViewGroup;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView1 = findViewById(R.id.t1);
        ViewGroup.LayoutParams layoutParams = textView1.getLayoutParams();
        layoutParams.height = dip2px(this, 50);
        layoutParams.width = dip2px(this, 200);
        textView1.setLayoutParams(layoutParams);
    }

    /**
     * 根据手机的分辨率从 dp 的单位 转成为 px(像素)
     *
     * @param context 上下文
     * @param dpValue dp值
     * @return int
     */
    public static int dip2px(Context context, float dpValue)
    {
        // 获取当前手机的像素密度（1个dp对应几个px）
        float scale = context.getResources().getDisplayMetrics().density;
        return (int) (dpValue * scale + 0.5f); // 四舍五入取整
    }

}
```







```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        android:gravity="center"
        android:background="#333333">

    <TextView
            android:id="@+id/t1"
            android:background="@color/purple_200"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintTop_toTopOf="parent" />


    <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="5dp"
            android:background="#00ffff"
            android:text="视图宽度采用wrap_content定义"
            android:textColor="#000000"
            android:textSize="17sp" />

    <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="5dp"
            android:background="#00ffff"
            android:text="视图宽度采用match_parent定义"
            android:textColor="#000000"
            android:textSize="17sp" />

    <TextView
            android:layout_width="300dp"
            android:layout_height="wrap_content"
            android:layout_marginTop="5dp"
            android:background="#00ffff"
            android:text="视图宽度采用固定大小"
            android:textColor="#000000"
            android:textSize="17sp" />

</LinearLayout>
```



![image-20220918112230262](img/Android学习笔记/image-20220918112230262.png)







### 设置视图的间距

* android:layout_marginTop="5dp"，该属性的作用是让当前视图与上方间隔一段距离
* android:layout_marginLeft让当前视图与左边间隔一段距离
* android:layout_marginRight让当前视图与右边间隔一段距离
* android:layout_marginBottom让当前视图与下方间隔一段距离
* 如果上下左右 都间隔同样的距离，还能使用android:layout_margin一次性设置四周的间距



layout_margin不单单用于文本视图，还可用于所有视图，包括各类布局和各类控件。因为不管布局还 是控件，它们统统由视图基类View派生而来，而layout_margin正是View的一个通用属性，所以View的 子子孙孙都能使用layout_margin。在View的大家族中，视图组ViewGroup尤为特殊，它既是View的子 类，又是各类布局的基类。布局下面能容纳其他视图，而控件却不行，这正源自ViewGroup的组装特性。



除了layout_margin之外，padding也是View的一个通用属性，它用来设置视图的内部间距，并且 padding也提供了paddingTop、paddingBottom、paddingLeft、paddingRight四个方向的距离属性。 同样是设置间距，layout_margin指的是当前视图与外部视图（包括上级视图和平级视图）之间的距 离，而padding指的是当前视图与内部视图（包括下级视图和内部文本）之间的距离



```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:layout_width="match_parent"
        android:layout_height="300dp"
        android:background="@color/purple_200"
        tools:context=".MainActivity"
        android:orientation="vertical">

    <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_margin="20dp"
            android:background="@color/design_default_color_secondary"
            android:padding="30dp">

        <View
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:background="@color/design_default_color_error" />

    </LinearLayout>

</LinearLayout>
```



![image-20220918115335207](img/Android学习笔记/image-20220918115335207.png)









### 设置视图的对齐方式

App界面上的视图排列，默认靠左朝上对齐，这也符合日常的书写格式。然而页面的排版不是一成不变 的，有时出于美观或者其他原因，要将视图排列改为朝下或靠右对齐，为此需要另外指定视图的对齐方 式。在XML文件中通过属性android:layout_gravity可以指定当前视图的对齐方向，当属性值为top时表 示视图朝上对齐，为bottom时表示视图朝下对齐，为left时表示视图靠左对齐，为right时表示视图靠右 对齐。如果希望视图既朝上又靠左，则用竖线连接top与left，此时属性标记为 android:layout_gravity="top|left"；如果希望视图既朝下又靠右，则用竖线连接bottom与right，此时属性标记为android:layout_gravity="bottom|right"。



注意layout_gravity规定的对齐方式，指的是当前视图往上级视图的哪个方向对齐，并非当前视图的内部 对齐。若想设置内部视图的对齐方向，则需由当前视图的android:gravity指定，该属性一样拥有top、 bottom、left、right 4种取值及其组合。它与layout_gravity的不同之处在于：layout_gravity设定了当 前视图相对于上级视图的对齐方式，而gravity设定了下级视图相对于当前视图的对齐方式；前者决定了 当前视图的位置，而后者决定了下级视图的位置。





```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:background="@color/cardview_dark_background"
        android:orientation="horizontal">


    <LinearLayout
            android:layout_width="0dp"
            android:layout_height="400dp"
            android:layout_weight="1"
            android:background="@color/purple_200"
            android:layout_margin="30dp"
            android:padding="10dp"
            android:layout_gravity="bottom"
            android:gravity="right">


        <View
                android:layout_width="80dp"
                android:layout_height="100dp"
                android:background="@color/design_default_color_error" />

    </LinearLayout>

    <LinearLayout
            android:layout_width="0dp"
            android:layout_height="400dp"
            android:layout_weight="1"
            android:background="@color/purple_200"
            android:layout_margin="30dp"
            android:padding="10dp"
            android:gravity="bottom|left">

        <View
                android:layout_width="80dp"
                android:layout_height="100dp"
                android:background="@color/design_default_color_error" />

    </LinearLayout>

</LinearLayout>
```



![image-20220918131311587](img/Android学习笔记/image-20220918131311587.png)







## 常用布局

