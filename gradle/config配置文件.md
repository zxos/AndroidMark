# Android配置文件

---

#### Config.gradle写法

1.创建config.gradle放置于项目根目录，与project.gradle同级

2.在project.gradle文件中引入，写上“ apply from "config.gradle" ”

3.文件大致写法

```
ext{

    android = [
                ...
                versionCode            : 1,
                ...
                ]
    dependencies = [
                    ...
                    "support-v4"      : "com.android.support:support-v4:24.1.1",
                    ...
                   ]
    ...
}
```

4.在app.gradle中使用\(遍历config.gradle中的dependencies\)

```
dependencies {
                rootProject.ext.dependencies.each {k, v -> implementation v}
}
```



