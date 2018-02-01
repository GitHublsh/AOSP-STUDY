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

9. ActivityStack.startActivityUncheckedLocked(frameworks/base/services/java/com/android/server/am/ActivityStack.java)

10. startActivityLocked(r, newTask, doResume)  (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

11. Activity.resumeTopActivityLocked (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

12. ActivityStack.startPausingLocked (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

13. ApplicationThreadProxy.schedulePauseActivity  (frameworks/base/core/java/android/app/ApplicationThreadNative.java)

14. ApplicationThread.schedulePauseActivity  (frameworks/base/core/java/android/app/ActivityThread.java)

15. ActivityThread.queueOrSendMessage (frameworks/base/core/java/android/app/ActivityThread.java)

16. H.handleMessage (frameworks/base/core/java/android/app/ActivityThread.java)

17. ActivityThread.handlePauseActivity (frameworks/base/core/java/android/app/ActivityThread.java)

18. ActivityManagerProxy.activityPaused  (frameworks/base/core/java/android/app/ActivityManagerNative.java)

19. ActivityManagerService.activityPaused (frameworks/base/services/java/com/android/server/am/ActivityManagerService.java)

20. ActivityStack.activityPaused  (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

21. ActivityStack.completePauseLocked  (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

22. ActivityStack.resumeTopActivityLokced  (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

23.  ActivityStack.startSpecificActivityLocked  (frameworks/base/services/java/com/android/server/am/ActivityStack.java)

24. ActivityManagerService.startProcessLocked  (frameworks/base/services/java/com/android/server/am/ActivityManagerService.java)