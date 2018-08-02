# live555
live555是在linux x64进行编译的，自己在linux进行二次开发，记录一下自己的开发过程。
1.先进行体验live555的功能。
  进入mediaServer文件夹，运行live555MediaServer可执行文件，这是一个rtsp服务器。下载VLC播放器，输入URL进行播放rtsp服务器推送的视频流（url例子：rtsp://192.168.233.128:8554/test.264）。  
  在mediaServer文件夹下，有一个名字为test.264的测试文件夹，如果想更换推送的视频文件，放置在mediaServer文件夹下，url中test.264可以替换为对应的文件名即可。  
2.live555库中使用的例子，都放在testProgs目录。要进行二次开发，对于服务端的代码，请参照testOnDemandRTSPServer.cpp，客户端代码，参照RTSPClient.cpp。
就服务端而言，要改的就是把服务器从文件读取数据，改为从实时读取数据。大家可以参考https://www.cnblogs.com/mlj318/archive/2013/01/23/2872932.html。
lichen
