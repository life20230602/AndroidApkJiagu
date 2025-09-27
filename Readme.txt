1、修改 env.properties 配置JAVA_HOME 和android_home目录


2、在命令执行 java -noverify -jar jiagu.jar

-apk 指定要加固的apk
-key 指定keystore文件
-kp 指定keystore密码
-alias 指定keystore alias
-rpkg 重命名功能，可以把apk重命名一个包名，非必选
-apmetadata 修改application 标签下的metadata key=value格式，非必选
-appNameMixin 应用名称混入特殊字符
-appIcon 修改应用图标，非必选
-output 加固文件输出目录或者输出文件名，如果打包多个指定目录，非必选
-randomKeystore 随机keystore文件，非必选
-disableProtectedRes 是否需要禁用资源保护，资源保护会增加包体积，非必选
-genNum 一次签名打包个数，如果多个，-output必须指定一个目录，非必须
-excludeRes 排除不需要保护的资源名，不需要后缀，比如 start_up.png 写成start_up就行
-disableDcProtected 禁用反编译保护


标准完全随机用法
java -noverify -jar jiagu.jar -randomKeystore -randomPackageName -apk xx.apk