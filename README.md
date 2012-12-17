PrsServoManager
===============
　Pirkus社製のコマンド式サーボモータを制御するためのコンポーネントです。
　現在のところ動作が確認できているOSはWindows32bit/64bitのみです。  
　Ubuntuでは動作確認が出来ていないのでご注意ください。  
　  
コンポーネントの仕様
--------------------
　　　　[![画像1][image1]](https://github.com/downloads/s-ryuki/Pictures/PrsServoManager_Comm.png)
[image1]:https://github.com/downloads/s-ryuki/Pictures/PrsServoManager_Comm.png

　　このコンポーネントはInPortをMotionLoader、MotionEditor、またはそれに準ずるコンポーネントから  
　コマンドを受け取ります。そのコマンドをPirkus社製のコマンド式サーボモータに沿ったをものに変換をし、  
　シリアルポートから出力することでサーボモータを制御します。  
　　sensor（OutPort）からはサーボモータのパラメータが出力されます。パラメータとは「サーボモータID」、  
　「サーボの温度」、「現在角度」等といったコマンド式サーボが送信可能なデータです。  

　  
使用方法
--------
　　　(1)Pirkus社製サーボモータを使用したロボットとPCを以下のように接続します。  
　　　　　　　　[![画像3][image3]](https://github.com/downloads/s-ryuki/Pictures/PC-PrsRobot.png)
[image3]:https://github.com/downloads/s-ryuki/Pictures/PC-PrsRobot.png
　　　(2)接続したCOMポート番号を確認し、servomanager.iniを編集します。  
　　　(3)servomoter.iniのサーボモータの各情報を編集し、保存します。  
　　　　　　　　[![画像4][image4]](https://github.com/downloads/s-ryuki/Pictures/PrsServoManager_ini.png)
[image4]:https://github.com/downloads/s-ryuki/Pictures/PrsServoManager_ini.png
####　　　　画面説明####
　　　　　　　①使用するCOMポート番号  
　　　　　　　②使用するサーボモータの通信ボーレート  
　　　　　　　③モーション間の分解能
　　　　　　　④サーボの個数  
　　　　　　　⑤センサ値をShellに表示する/しない  
　　　　　　　⑥サーボモータのIDと番号  
　　　　　　　⑦サーボモータの可動域およびオフセット[/0.1deg]
　  
　　　(4)PrsServoManager.pyを起動します。  
　　　(5)RTSytemEditor上で「モーション再生モード」で使用する場合はMotionLoader、  
　　　「モーション編集モード」で使用する場合はMotionEditorと繋ぎます。  
　  
　Pirkus社製のコマンド式サーボモータPRS-M07S、PRS-M40Sのハードウェアマニュアルはこちらからご覧ください。  
　　　　　[PRS-DE07MS/PRS-S40Mマニュアル](https://github.com/downloads/s-ryuki/HardwareManual/PRS-DE07MS_PRS-S40M_%E7%AC%AC%E5%9B%9B%E7%89%88.pdf)
