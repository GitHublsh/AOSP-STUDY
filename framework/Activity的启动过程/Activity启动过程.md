### Activity启动过程

这里只记录整个流程，细节都在源码里。

1. Launcher.startActivitySafely（src/com/android/launcher2/Launcher.java）

2. Activity.startActivity（frameworks/base/core/java/android/app/Activity.java）

3. Activity.startActivityForResult（frameworks/base/core/java/android/app/Activity.java）

4. Instrumentation.execStartActivity（frameworks/base/core/java/android/app/Instrumentation.java）

5. ActivityManagerProxy.startActivity（frameworks/base/core/java/android/app/ActivityManagerNative.java）

6. ActivityManagerService.startActivity（frameworks/base/services/java/com/android/server/am/ActivityManagerService.java）

7. ActivityStack.startActivityMayWait（frameworks/base/services/java/com/android/server/am/ActivityStack.java）

8. ActivityStack.startActivityLocked（frameworks/base/services/java/com/android/server/am/ActivityStack.java）