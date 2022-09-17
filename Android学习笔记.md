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



