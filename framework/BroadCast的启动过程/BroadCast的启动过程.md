### BroadCast的启动过程

1. ContextWrapper.registerReceiver  (frameworks/base/core/java/android/content/ContextWrapper.java)

2. ContextImpl.registerReceiver  （frameworks/base/core/java/android/app/ContextImpl.java）

3. ActivityThread.getHandler  (frameworks/base/core/java/android/app/ActivityThread.java)

4. LoadedApk.getReceiverDispatcher  （frameworks/base/core/java/android/app/LoadedApk.java）

5. 