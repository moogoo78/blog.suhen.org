Title: [Mac] 從Leopard升級到Mavericks
Date: 2013-11-02 00:46
Category: computer
Tags: note
Slug: mac_leopard_mavericks

家裡一台很舊的iMac，作業系統跑Leopard (OS X 10.5.8)，很多軟體都不支援如 LINE桌面版... ，或是連Chrome都不更新了，倒是Firefox還很照顧這些老電腦...

最近Mavericks開放免費更新，我的MacBook Air (Lion) 免費升級新的Mavericks後，覺得很好用，實在也很想更新這台iMac，Leopard一般是無法直接升級到Mavericks的，除非花一點錢，先升級成Snow Leopard (OS X 10.6)，才可以免費升級到Mavericks。但是網路上果然有解決方法！！

參考這篇: [How to install Mavericks over Leopard | Macworld](http://www.macworld.com/article/2056564/how-to-install-mavericks-over-leopard.html)



# 1. 下載Mavericks

我的MacBook Air已經更新10.9了，但還是可以再下載。

改一個系統檔:

    :::text
    /System/Library/CoreServices/SystemVersion.plist
    # 把10.9的地方改稱10.8

然後到iTunes Mavericks官方頁面[Mavericks](https://itunes.apple.com/tw/app/id675248567?mt=12)就可以"重新"下載了。下載完的檔案會放在 */Applications/Install\ OS\ X\ Mavericks.app*，大概有5G多，iTunes載完會自動跳出安裝視窗，但是先不理他，可以把這個目錄copy到其他地方，不然系統以為安裝完後就會自動殺掉。

# 2. 製作開機磁碟

用Terminal打入以下:

    :::bash
    sudo /Applications/Install\ OS\ X\ Mavericks.app/Contents/Resources/createinstallmedia --volume /Volumes/MY_EXTURNAL_HD --applicationpath /Applications/Install\ OS\ X\ Mavericks.app --nointeraction

訊息跑完後就好了。(原本磁碟內容會消除)

ref: [How to make a bootable Mavericks install drive | Macworld](http://www.macworld.com/article/2056561/how-to-make-a-bootable-mavericks-install-drive.html)


# 3. 安裝

改系統檔(不確定這是不是一定要):

    :::text
    /System/Library/CoreServices/SystemVersion.plist
    # 把10.5.8改成10.68


外接硬碟接上iMac，重新開機。開機時按住*Option*會跳出選擇開機磁碟，就選剛才製作好的開機碟。就會開始自動安裝了。 爽快。