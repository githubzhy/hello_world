使用Android SDK 和 JDK 的命令 签名打包APK
 创建签名
  keytool -genkey -v -keystore stone.keystore -alias stone -keyalg RSA -keysize 2048 -validity 10000  生成签名文件
 为apk签名
  jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore stone.keystore unsigned.apk stone 不生成新文件
 检测apk是否签名
  jarsigner  -verbose -certs -verify signed.apk 
 优化apk
  zipalign -f -v 4 signed_unaligned.apk signed_aligned.apk 
  
  
  android源码
1, AndroidRef http://androidxref.com/
2, https://www.codeaurora.org/

下载frameworks/av
git clone https://source.codeaurora.org/quic/la/platform/frameworks/av -b aosp-new/master

----------------------------------------------------------------------------------

http://webrtc.org.cn/

www.ffmpeg.org
http://bbs.chinaffmpeg.com/forum.php


BookMarks
1 webrtc录音 http://www.webrtcbbs.com/forum.php?mod=viewthread&tid=278


