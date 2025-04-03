源泉徴収義務者情報インタフェース・媒体仕様書

# 第１.３版

平成２９年１０月２５日

国 税 庁厚生労働省日本年金機構

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/ebb1a321b71fdb3e037082d35e0d3610d800dcb8d5281722b2a7cc188f0768b8.jpg)

# －目次－

１ 目的・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・・ １

$\_1-1$ 連絡体制・・・・・・・・・・・・・・・・・・・・・・・・・・・ １

（情報公開法第５条第４号に該当するため不開示）・・・・・・・・・・・・・・２

（情報公開法第５条第４号に該当するため不開示）・・・・・・・・・・・・・・２

２－２ 文字コード体系・・・・・・・・・・・・・・・・・・・・・・・・３

２－３ 送信データの仕様・・・・・・・・・・・・・・・・・・・・・・・４

（情報公開法第５条第４号に該当するため不開示）・・・・・・・・・・・・・・６

３ 障害時対応について・・・・・・・・・・・・・・・・・・・・・・・・ ７

３－１ 連絡体制・・・・・・・・・・・・・・・・・・・・・・・・・・・ ７

３－２ その他事項・・・・・・・・・・・・・・・・・・・・・・・・・・７

# （添付資料）

別添１ 外字一覧表

別添２ 源泉徴収義務者提供情報ファイルフォーマット

別添３ 税務署番号コード表

別添４ 給与支給人員コード表

別添５ 業種番号コード表

別添６ 本支店区分コード表

# １．目的

本仕様書は、所得税の源泉徴収義務者に関する法人情報を、国税庁から厚生労働省（日本年金機構）に対して提供する際に使用する、インターフェースの仕様を定めるものである。

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/50f42f8dfbf5b76776e3ba1b09fdca6c118f6c748caf3a03b6756401f6895ca3.jpg)

１－１．連絡体制

連絡先情報・国税庁

総務課 調査第三係 （代表：03-3581-4161［内線：（※）］）

・厚生労働省

年金局事業管理課 厚生年金保険管理係（代表：03-5253-1111［内線：（※）］）

・日本年金機構

事業推進統括部 厚生年金保険事業推進G（代表：（※）\[内線：（※）\]）

（※ 内線及び日本年金機構の代表番号については、情報公開法第５条第６号柱書に該当するため不開示）

参考：定常的に発生する連絡及び物品引き渡しは以下のとおり $\\textcircled{1}$ 年間計画の送付 毎年３月中頃 電子メール(国税庁 $\\rightrightarrows$ 厚生労働省) $\\circled{2}$ 鍵情報 $\\mathcal{O}$ 送付 毎年11月末頃媒体渡し(国税庁 $\\rightrightarrows$ 厚生労働省)（情報公開法第５条第４号に該当するため不開示）

２－２．文字コード体系

送信データに係る文字コードは、以下のとおりとする。

$1/\\dot{\\setminus}\\dot{1}\\dot{\\setminus}$ 文字： $\\mathrm{ ~~J~~}\\mathrm{ ~~I~~ S~}8$ 単位符号（JIS X 0201-1976）特殊文字のコード規定は、「改行：0D0A(１６進)」

$2/\\dot{\\Upsilon}\\dot{\\Upsilon}\ \\vdash$ 文字：シフトＪＩＳコード（JIS X 0208-1983（ＪＩＳ第一水準、ＪＩＳ第二水準）で規定された文字をシフトした文字コード）

また、外字及びそのコードについては「別添１ 外字一覧表」のとおりとする。

２－３．送信データの仕様

厚生労働省へ送信データとなる源泉徴収義務者の情報ファイルの仕様を以下に示す。

$\\textcircled{\\scriptsize{1}}$ ファイル名及び数等

厚生労働省へ送信する源泉徴収義務者の情報ファイル名及び数等は次のとおりとする。

【テキストファイル】ファイル数：5ファイル名：源泉徴収義務者の情報（東京）$\\Rightarrow$ FCA1.HYA.FCJ1KR13\_\*\*\*\*\*\*\*\*.txt 源泉徴収義務者の情報（関信・札幌・仙台）$\\Rightarrow$ FCA2.HYA.FCJ2KR13\_\*\*\*\*\*\*\*\*.txt 源泉徴収義務者の情報（大阪・福岡・熊本・沖縄）$\\Rightarrow$ FCA3.HYA.FCJ3KR13\_\*\*\*\*\*\*\*\*.txt 源泉徴収義務者の情報（名古屋・金沢・広島・高松）$\\Rightarrow$ FCA6.HYA.FCJ6KR13\_\*\*\*\*\*\*\*\*.txt データ件数：\*\*\*\*\*\*\*\*［8桁］拡張子：txt送達確認：FCA9.HYA.FCJ9KR13\_00000000.dat［0Byteファイル］

$\\circled{2}$ データレコード項目一覧表

厚生労働省へ送信する源泉徴収義務者の情報ファイル内のデータレコード項目一覧表は「表 $2-3-1$ 源泉徴収義務者の情報のデータレコード項目一覧」のとおりとする。

なお、厚生労働省 $\\frown$ 送信する源泉徴収義務者の情報の送達確認ファイルは０バイトファイルとするため、データレコードは存在しない。

表 $2-3-1$ 源泉徴収義務者の情報のデータレコード項目一覧

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/b223253b705610eecf5075c7486f0487dd36022f9854984fccaebd21d9aa32cc.jpg)

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/7cf3d91ed13a200bd579839b8ee4a1ea617ece6c57b71d8e65e005057ae24a53.jpg)

(※１)・・固定長ファイルとする

「表 $2-3-1$ 源泉徴収義務者 $\\oslash$ 情報のデータレコード項目一覧」にある項番 $ _1\\sim$ 項番 $_{10\ \\mathcal{O}}$ 設定値 $\\mathcal{O})$ 詳細は「別添２ 源泉徴収義務者提供情報ファイルフォーマット」に示す。

また、「表 $2-3-1$ 源泉徴収義務者 $\\oslash$ 情報 $\\oslash$ データレコード項目一覧」の各項目 $\\oslash$ コード表と別紙資料 $\\oslash$ 関連を「表 $2-3-2$ コード表一覧」に示す。

表２－３－２ コード表一覧

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/d4452e5b0c235a91da33d30d7f594472644a486dd424b3479bfca92717ac6ae4.jpg)

（情報公開法第５条第４号に該当するため不開示）

# $\\circledast$ 想定データ量

１ＧＢ程度（約２４２万件×３８０ｂｙｔｅ）とする。【参考】 $\\textsf{1G B}\\sigma\_{\\textsf{2}}$ データを３mbps $\\oslash$ 回線で送信する際 $\\oslash$ 所要時間は約65 分。

（計算過程）

$=$ 1,024MByte

・1024MByte×８（bit 換算） $\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad\\qquad=\\quad8$ ,192Mbit

・8,192Mbit÷３Mb $\|,\\mathtt{t}/\\mathtt{s},\\overset{}{=},\\mathtt{\\nabla}2,731\\colon$ s

・2,731s÷60 ≒ 45.5min

・45.5min÷0.7（ワイヤレート） $=$ 65min

$\\circled{5}$ ファイルサイズの制限４ファイル２ＧＢを上限とする。

$\\circled{6}$ ファイルの送達確認

ファイル名称記載の「FCA9.HYA.FCJ9KR13\_00000000.dat」を使用した確認とする。

厚生労働省では、源泉徴収義務者の情報が欠損なく送信されたことを確認するため、国税総合管理システムにてファイル名称にレコード件数を付与することにより、送信後の源泉徴収義務者の情報ファイルのレコード数が、ファイル名称に付与されたレコード件数と合致することを確認可能とする。

また、送信途中の源泉徴収義務者の情報ファイルを処理してしまうことを防止するため、国税総合管理システムにて全ての源泉徴収義務者の情報ファイルの送信が完了後、源泉徴収義務者の情報の送達確認ファイル(0 バイトファイル)を送信する。

（情報公開法第５条第４号に該当するため不開示）

３．障害時対応ついて３－１．連絡体制

$\_1-1$ ．連絡体制に定める連絡先に対して連絡を行うこと。なお、以下に該当する場合、判明した時点で早急に連絡を行うこととする。・ （情報公開法第５条第４号に該当するため不開示）・ 厚生労働省側が受信したデータ件数が不一致となっている場合。

３－２．障害・罹災時等のデータ提供方法

障害・罹災等により所得税の源泉徴収義務者に関する法人情報を、国税庁から厚生労働省（日本年金機構）に対して提供ができない状態となった場合は、原則、復旧次第、回線経由で再度データ提供を行う。毎月第15 稼働日 $\\mathcal{O})$ ８時から23 時以外 $\\oslash$ 時間帯でデータ提供を行う場合は、一時的に国税総合管理システムからの通信を許可するよう厚生労働省(日本年金機構)側で設定を行う。但し、回線経由での連携が当面不可と想定される場合は媒体で情報提供する。なお、詳細は別途協議するものとする。

提供する媒体に係るファイル仕様は以下のとおり。また、件数は、別途紙媒体（件数表）を提示する。

$\\textcircled{\\scriptsize{1}}$ ファイル名称付与方法

情報記録媒体により提供される源泉徴収義務者の情報ファイルは、暗号化された自己復号型ファイルとする。ファイル数及びファイル名等は次のとおりとする。

【自己復号型ファイル】

ファイル数：1

ファイル名：源泉徴収義務者の情報拡張子： exe

自己復号型ファイルを復号することにより、「源泉徴収義務者の情報」フォルダが生成され、その配下に源泉徴収義務者情報のテキストファイルが生成される。ファイル数及びファイル名等は次のとおりとする。

【テキストファイル】ファイル数：4ファイル名：源泉徴収義務者 $\\mathcal{O})$ 情報（東京）$\\Rightarrow$ FCA1.HYA.FCJ1KR13.txt 源泉徴収義務者の情報（関信・札幌・仙台）$\\Rightarrow$ FCA2.HYA.FCJ2KR13.txt 源泉徴収義務者の情報（大阪・福岡・熊本・沖縄）$\\Rightarrow$ FCA3.HYA.FCJ3KR13.txt 源泉徴収義務者の情報（名古屋・金沢・広島・高松）

$\\Rightarrow$ FCA6.HYA.FCJ6KR13.txt 拡張子：txt

$\\circled{2}$ データレコード項目一覧表

格納されている源泉徴収義務者の情報ファイル内のデータレコード項目一覧表は回線経由で引き渡すファイルと同じとする。

３－３．その他

障害・罹災等により所得税の源泉徴収義務者に関する法人情報を、国税庁から厚生労働省（日本年金機構）に対して提供ができない状態となった場合、予定しているデータ抽出日にデータが取得できていないことが想定される。このため、罹災月 $\\mathcal{O})$ 情報提供をスキップした場合、復旧後提供される最新月分のファイルのみ作成し提供することとする（前回送信時点から、送信再開までの間の更新情報が反映されたファイルを最新月分として作成）。

別添１

# 外　字　一　覧　表

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/60763b993f8afa0803f23608543f96f066f32cd7e6949752c140624b9df29d37.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/888f772a53224be0b491dfa722bfcac822907b44b1a1bef6703cd3146b08870e.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/e3ead58f398fd23aed1c09eb3684d849982183f687e1cf17cf10342220f1b555.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/151cf379b398aad41ec86ea3c6c8dfe85334cf039b9fe08c6defc22929f13147.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/d41bdfc895364324b05a07f8bed36ae57f198934c15e22654ed5bbffa1cafb55.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/8f5ba70f0c9777747848221fd34e45aee629e519b9a1b1d7baeb0807981e4510.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/2486b9c5b8e2b5f22aedac5425a596adb79bc4464e4940cd92f032ad9e621d79.jpg)

外字コード一覧（漢字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/4cbeffbb47ccb06da48f24512321c8c7b011b8072e7a80c2e80df55e9ab9ca8d.jpg)

外字コード一覧（丸付き文字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/87c89c218dd8ca17fa53bbbbac73b8feb9692c64737466dc6da096979a8fd0cf.jpg)

# 別添１

外字コード一覧（かっこ付き文字）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/2ed4e251b2798a2319682f2cb86c708ae1c9644fa6f6d1741f41563dc6447bb2.jpg)

外字コード一覧（ローマ数字）

外字コード一覧（単位記号）

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/33ec0962b382d10630f02643c921955810314364f8b10f747756d4c40dac079c.jpg)

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/48b4adffad2e285d2a896cfb97a000a636c95a9581a29fffe4a55ed1c4f5bfb0.jpg)

# 源泉徴収義務者提供情報ファイルフォーマット

源泉徴収義務者の情報（東京） $\\Rightarrow$ FCA1.HYA.FCJ1KR13\_\*\*\*\*\*\*\*\*.txt源泉徴収義務者の情報（関信・札幌・仙台） $\\Rightarrow$ FCA2.HYA.FCJ2KR13\_\*\*\*\*\*\*\*\*.txt源泉徴収義務者 $\\oslash$ 情報（大阪・福岡・熊本・沖縄） $\\Rightarrow$ FCA3.HYA.FCJ3KR13\_\*\*\*\*\*\*\*\*.txt源泉徴収義務者 $\\oslash$ 情報（名古屋・金沢・広島・高松） $\\Rightarrow$ FCA6.HYA.FCJ6KR13\_\*\*\*\*\*\*\*\*.txt\*\*\*\*\*\*\*\*：国税庁においてファイルを送信する際に、レコード件数をセットし提供する。

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/2126bb4ed39b2273cc30e42a0ae863b3f7b35a38ed85cdb89586fc6a507bb4e0.jpg)

＜特記事項＞・区切り文字の設定は行わな $\\backprime\_{\\circ}$ ・文字数が格納エリアを超える場合（文字あふれ）は、あふれた文字数は単純に切り捨てられ、提供されな $\\backprime\_{\\circ}$ ・外字については「＿」(アンダーバー)に置き換えされている場合がある。・レコードのソート順は、第一ソートキーは「局署番号」の昇順、第二ソートキーは「整理番号 $\\mathcal{1}\\mathcal{O}$ 昇順である。

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/e3a7cc98f23f13876d861e27026b78c544be159121c29197525a2f088ed89644.jpg)

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/a2a3c0d0fd8710f97a6c788a7babe11fd983a8d436ff1bbe8841ad6e5d9bccc0.jpg)

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/e613ed47dcd64edad85426b590159ce4cf3006656086432872de541e64578020.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/4ea858c96bea86ab2c46ba52a0d44b05acbe924f8d3925ae2c0e3fd3c7a5dd11.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/88f4edefc1505021927a131e9170f5e3c62a0edf159b0a01e50135286cbb2ce1.jpg)

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/53ac79b5ea69946ad2e18cb74fd53fdcf34e3c4ddfe19cb234a29093b11d83fd.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/e0eeb84c0828e0cfb3730bb1b482bc92bf636c0743f6502bfafad2e0f01c11cb.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/34d37b9fbdfbd476fa1453f284b96bf7c31415ee144e8616534ab39a5c05ec4c.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/ba0415aba0aabb6e6906cec0018142ba109689df4780ef1fe6e11e7144916a29.jpg)

税務署番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/456bfd357274bb341204d3a744c4028e477729d2498328ca5092edea3631bd5c.jpg)

給与支給人員コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/03f9493ebb3581e20bf957cc7cde4b1db078f230d499db53e3d62e0447f6147c.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/d2fe86d9ff511c62ea1dd5dc0c06dcd443076facbe4d4e77f6d1c7f50d11824d.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/d0c86f852ef4d5583dfc39750cf562d1c32d3196511ed8a1e8c82a0d338a1c49.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/9ab5fa7ed0994327d01ff3e5772ae90b0ee436a43ea9e544a3f117cf7ccda0b2.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/49f428de66b735510970a95df108c1e60c301399ca10c3c072754859cbba0cb2.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/adc092873dcb3f04676c8a1f07df57cb002d4a6645daf419adfec02e828d9952.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/c2d570c147e89f345ec5ea9c0c3bc5d48cd048878d0ba46de62e6f5c78de792f.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/c80cfef803dce085d25f15d1d4ae8a33a8e1e7655cc4548cd6aeb0dea02a7027.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/01d07b2a416af0a70a7b87420d4833097bbb83213f5a4e74a8574f06fa669593.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/c28a551b753cc4ec138970979d502ebe34736d85c8a2c96199aa0f8ae60a52ff.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/24138a0f407455265c3cefb4c18019288b985f9eb221096e7b265e5b5bae7b75.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/ba6fef31c2732596d733d1845653aa34ee9b6e6719d6cb99cb8faa09e09d3ebd.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/7e0dda1a439c6acea6ed0b72c2743a0ad52c588e4381b0fa55379feb1eac09a7.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/43d8af2c35a0790b5e719a8b32e802d5a85c4bb21821a9ddd7702effbd0c9290.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/97cc3a2d8930392027bc5d29dd0a9f79ec0d2c6ae14336a9f014a6fa506ef7ec.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/e64e1cc2d9039bbadb7a564e980888f8152d937f37961bfd03fab61c4768614e.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/1403b10ee35f7739ed3193daabd01bc4808152b890314bf6d52a831448ff6663.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/795f2eb206c6ee49c40d911417d70640bdef390394e9838ede04b0e2c85bd7cb.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/a89eb1f511406ac4c6046aea1039289c970707bd6290c0c6423018c43195b6db.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/6b79f085fa87338cabd59daab0598f21ae9433525d0df4b8d492de473911d585.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/478a9fd126a9dc579ae303b5ef07ab1289b783ddae0fc671e501a252f6bd93de.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/979031ddba21a17ef6eea86de1e737b21b1fedf1827b6fc96ea53765b38d53f4.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/24101341cd2143430a503733a4a611e058c0b214f846742e071545d3b4e52025.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/0492a46a90711290dacb3794cac5dd5a78542503f03193d51f250b065eefd2fc.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/677731c1636b769243f45505fb432699838f44734d22ad5601073950dbcb4a20.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/c11e2cc5a14242e2e8e0b7ae1e2db17e7b8e3c216cf8c890f8e6d44952c9b75a.jpg)

# 業種番号コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/b739f809dc31a23dd01b262b3178feddb6f6f768a88670a0b3120920427868fb.jpg)

# 別添６

本支店区分コード表

![](https://www.nta.go.jp/tmp/680837a3-5546-4063-b2cb-c032b1fcd71a/images/033fbac7179da320ca0da7428f958749de8e00aa32ad25c6b3f6b46efce4cc7b.jpg)