# Ubuntu セットアップ マニュアル Part2

- [Ubuntu セットアップ マニュアル Part2](#ubuntu-セットアップ-マニュアル-part2)
  - [セットアップの前に 〜使用するパーツの準備〜](#セットアップの前に-使用するパーツの準備)
  - [セットアップ](#セットアップ)
    - [PCの起動](#pcの起動)
    - [インストール](#インストール)
  - [アップデートとドライバのインストール](#アップデートとドライバのインストール)


## セットアップの前に 〜使用するパーツの準備〜
- SSD 256GB以上が望ましい(先生から480GBがもらえる)
- インストール USB(作成済み)
- インストール対象のPC(ゴツいPCがあるよ)

## セットアップ
では、いよいよUbuntuをセットアップしていきましょう。<br>
___

### PCの起動
まずSSDとUSBをPCに挿し、PCを起動します。
メーカーロゴが表示されたら、すぐにF8キーまたはF11キーを押します。(使用するPCに合わせて、とにかく*boot menu*を開きましょう。)
すると*boot menu* が表示されるので、そこから`kioxia~`と書かれたUSBメモリを選択しましょう。<br>
*boot menu*が実装されていないPCの場合は、BIOSの設定からboot diskを選択する必要があります。
その後`GRUB boot menu`が表示されるので、*try or install ubuntu*を選択します。暫く待つとUbuntuが起動します。

### インストール
Ubuntuが起動すると、Installerが自動的に起動します。Installerの指示に従ってインストール作業を行いましょう。<br>
*※この時、SSDはインストール時にフォーマットして用いるようにしてください。*

___
## アップデートとドライバのインストール
再起動すると、SSDからUbuntuが起動します。ここから、必須の設定を行います。<br>
まずはUbuntuのアップデートを行います。Terminal上で、<br>
`sudo apt update`<br>
と、<br>
`sudo apt upgrade`<br>
を実行してください。Ubunutu付属のパッケージがアップデートされます。その後必ず再起動してください。<br>

次に**NVIDIA Driver**(Geforceのドライバ)をインストールしましょう。Terminal上で、<br>
`ubuntu-drivers devices`<br>
を実行してください。
`recommend`と書かれたドライバを用いて、<br>
`sudo apt install nvidia-driver-xxx`<br>
(xxxは任意のバージョン名、パッケージ名は変更になっている可能性あり)としてNVIDIA driverをインストールしましょう。<br>

インストール後に再起動して、Terminal上で<br>
`nvidia-smi`<br>
を実行してGeforceの詳細が表示されれば、インストールは成功です。


<span style="color: gray">
ubuntuにおけるnvidia-driverはよく壊れますし、よくインストールに失敗します。もし失敗したり、壊れた場合は、一度nvidia-driverをアンインストールし、インストールしなおしてみましょう。それでもダメな場合はnouveau無効化(別ファイルに紹介します)などの手段を取りましょう。時にはubuntuを一からセットアップした方が早い場合もあります。
</span>
<br><br>


お疲れ様でした。このファイルの内容は以上です。Part3に進んでください。
