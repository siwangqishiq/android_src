### Android系统简要启动流程

通电 -> bios -> linux内核加载 
->init进程 ->zygote进程 ->system_server进程 
->lancher App ->Lancher Activity

init进程  
Android/system/core/init/main.cpp
FirstStageMain(挂载系统运行目录) -> SetupSelinux -> SecondStageMain (init.cpp) 开启系统属性服务 fork zygote进程

zygote进程
Android/frameworks/base/cmds/app_process/app_main.cpp
app_runtime 类 启动ART虚拟机  注册 jni方法完成后 反射调用 com.android.internal.os.ZygoteInit main()方法






