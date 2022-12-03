# Roktrack - Pylon-Guided Robotic Mower
![Sambnail0](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/mainsambnail.jpg)
![Sambnail1](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/sambnail1.jpg)
![multipurpose](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/multipurpose.jpg)
![effect1](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/beforeafter_homeback.jpg)
![effect2](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/beforeafter_community.jpg)
https://youtu.be/5oMwZd8DZL8
## System Structure
![Overview](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20220915_130832.JPG)
2022/12/03 [climbing](#climbing) を追記しました。
## How it works.
### Fill mode
Roktrack heads to the pylon recognized based on camera image. When it approaches the pylon more than a certain amount, it turns around and searches fot next one. By speeding up the turning timing with each lap, it will enter from the outside to the inside.

Roktrackはカメラで撮影した画像を基にパイロンを認識し、その方向に向かっていきます。パイロンに一定以上近づくと旋回して次のパイロンを探します。周回を重ねるごとに、旋回タイミングを早めることで外側から内側に入り込んでいきます。

Roktrack 前往根据摄像头图像识别的塔架。当它接近塔架超过一定量时，它会转身寻找下一个。通过加快每圈的转弯时间，它将从外向内进入。
![HowToWork](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/howitwork.JPG)

### One-way mode
By controlling it to move slightly to the left when approaching the pylon, it is now possible to trace the pylons lined up in a straight line.If you install a pylon every 20 meters, you can guide as much as you want, and it can be used as a mowing of ridges and as an outdoor patrol robot.

パイロンに最接近する際に少し左側に寄せるように制御することで直線状に並んだパイロンをなぞるように進めるようになりました。20m毎にパイロンを設置すればいくらでも誘導でき、畦草刈りや屋外巡回ロボットとして利用できます。

现在，通过控制它，以便它靠近左边一点点，当接近塔，它来跟踪塔排列成直线。每20米安装一个塔，你可以引导尽可能多的，你可以使用它作为割草和户外巡逻机器人。
![HowToWorkOneWay](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/Screenshot_20221111-100620~2.JPG)

## climbing
### steep slope(<60°)(experimental)
![steep](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/steep.gif)
It is planned to be able to work on slopes of up to 60 degrees by installing wires and linking two units.

ワイヤーを備え付け、2台で連携することで60°までの斜面で作業出来るようになる予定。

计划通过安装电线和连接两个单元，能够在高达 60 度的斜坡上工作。

### wall(=90°)(experimental)
![wall](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/wall.gif)
By preparing a wire and slave unit, you can control the movement on the YZ plane from the XY plane. It may be possible to apply it to wall printers in the future.

ワイヤーと子機を準備すれば、XY平面から、YZ平面での動作をコントロール可能。将来的には壁面プリンターなどに応用可能かも。

如果准备了线和从属单元，则可以从 XY 平面控制 YZ 平面上的移动。未来或许可以将其应用到墙壁打印机上。

## multipurpose
![multipurpose](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/sambnail/multipurpose.jpg)

- mower
- Spreader (can spread seeds and fertilizer)
- sweeper
- Blower (can blow dust)
- Vacuum cleaner

*Experimental functions other than mower

---

- 草刈り
- 散布機（種や肥料が撒ける）
- スイーパー（掃き掃除）
- ブロア（粉塵を飛ばせる）
- 掃除機

※草刈以外は実験的な機能

---

- 割草机
- 吊具
- 扫地机
- 鼓风机
- 清洁器

## Hardware
### Inside
Roktrack has two RS-775 motor to mow and two 37GB555 motor(56rpm) to drive crawler, 10Ah Lifepo4 4s 12V battery. 

Roktrackは草刈用のRS-775モーターを2つ、クローラー駆動用の37GB555モーター(56rpm)を2つ、10AhのLifepo4 4S 12Vバッテリーを備えています。

Roktrack 有两个用于割草的 RS-775 电机和两个用于驱动履带的 37GB555 电机（56rpm），10Ah Lifepo4 4s 12V 电池。
![Inside](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20220915_131314.JPG)
### Appearance
- Improved appearance with web camera and pan/tilt function
- M10 universal screws supporting the camera are painted black
- The cover covering the RPi is an aluminum duct cut in half to ensure ventilation, heat insulation, and water resistance

---

- Webカメラを採用し外観向上、パン・チルト機能
- カメラを支えるM10全ねじを黒に塗装
- RPiを覆うカバーは半分に切ったアルミダクトで通気性・断熱性・耐水性確保

---

- 改进了带有网络摄像头的外观，平移/倾斜功能
- 所有支持相机的M10螺丝都涂成黑色
- 用切成两半的铝管覆盖在RPi上，以确保通风、绝缘和防水。

![Appearance](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_091711.jpg)

![Cover](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_091812.jpg)

![CoverOpen](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_091844.jpg)

### Camera
Using Logicool C525 camera. Switching high(1280x960) and low(640x480) resolution on the situation enable long range detection.

ジャンク売り場で見つけたLogicool C525 カメラを使用。状況に応じて高(1280x960)、低(640x480)の2つの解像度を切り替える事で長射程を実現。

使用 Logicool C525 相机。根据情况切换高 (1280x960) 和低 (640x480) 分辨率可实现远程检测。
![LogicoolCamera](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_091715.jpg)
### Back
With physical switch to turn off 12V power supply.

12V系電源を切る物理スイッチ付き。

用物理开关关闭 12V 电源。
![Back](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/STORYPIC_00009435_BURST220919162430.JPG)
### Side
By supporting the crawler from both sides of the chassis and cover, the strength is improved and the grass is prevented from entering.

クローラーをシャーシとカバーの両方向から支えることで強度向上と草が入り込むことを防止。

通过从底盘和罩盖两侧支撑履带，提高强度，防止草进入。
![Side](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/DSC_0117.JPG)
### Tools
In-vehicle tool for removing tangled grass and spare parts.Stored inside as grass entanglement rarely occurs anymore.

絡みついた草を除去するための車載工具と予備部品。草の絡みつきがほとんど起きなくなったため、内部に格納。

用于清除缠结草和备件的车载工具。储存在里面，因为草的纠缠很少发生了。
![Tools](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/DSC_0114.JPG)

![InVehicleTools1](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_094926.jpg)

![InVehicleTools2](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20221018_094942.jpg)
## Software
### Raspberry pi 4
Pylon detection by YOLOv7 custom model and operation control.

YOLOv7カスタムモデルによるパイロン検知と運転制御。

通过 YOLOv7 自定义模型和操作控制进行 Pylon 检测。
![全体ソフトウェア構成](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/20220915_134518.JPG)

### Mobile app
Confirmation of the current mowing situation and remote sensing by artificial satellite.

現在の草刈状況の確認と人工衛星によるリモートセンシング。

人工卫星对当前割草情况的确认和遥感。
![モバイルアプリ](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/app.JPG)

## Spec
### Effective distance

Learning with YOLOv7 + high-mount camera + variable resolution enables long-distance detection

Sunny: 40m Cloudy: 20m High contrast env: 15m

YOLOv7による学習＋ハイマウントカメラ＋可変解像度により長距離検知が可能

晴天：40m 曇天：20m 高コントラスト下：15m

YOLOv7学习+高位摄像头+可变分辨率实现远距离检测

晴天：40m 阴天：20m 高对比度环境：15m
![長距離検出](https://raw.githubusercontent.com/ysuito/RoktrackPage/master/img/DSC_0087.JPG)
### frame rate
- Low resolution: 0.5FPS
- High resolution: 0.2FPS

- 低解像度: 0.5FPS
- 高解像度:  0.2FPS

- 低分辨率：0.5FPS
- 高分辨率：0.2FPS
### working time
About 3 hours.
### batteries
- Lifepo4 4S 12.8V 10Ah (1000cycle)
- mobile battery 10000mAh (500cycle)
### mowing width
200mm
### speed
1km/h
### steps that can be climbed
50mm
### slope
30 degree
### size
high mount camera: 370mmx370mmx530mm

low mount camera: 370mmx380mmx230mm
### weight
5.5kg
### operating temperature
max outside temperature 35℃
### Fuse
rated 10A

# ストーリー
## 開発の背景
中山間地の草刈りは想像以上の重労働。
騒音、振動、排気ガス(2st!!)、怪我、虫、 熱中症、飛び散る草、すぐに生える

→何とかしたいが、現実はエンジン刈払機でやるしかない

## 試行錯誤
### 草刈性能向上の困難性
前提として雑草の中には何が落ちているかわかりません。刃に接触してしまう石が存在していたり、長尺の草はシャフトに絡みついてしまいます。以下の課題のバランスを取らなければなりません。

- 草を刈るためのパワー
- 草を刈るための刃の鋭さ
- 障害物への刃の接触
- 巻き付き防止
- 障害物に乗り上げてしまわないこと

雑草を刈るには切れ味もしくはパワーが必要です。一般に切れ味を向上させると刃が薄くなるため耐久性が確保できません。刃を厚くするとパワーが必要ですが、パワーがあがった分、障害物に接触した際に厚くした刃が削れてしまいます。刈り刃に関しては多くの試作を繰り返しましたが、石の転がる環境で2〜３時間稼働させると必ず刃が破損しました。たどり着いた答えがツインモーター化でした。これによりまず、一つあたりの刃の径が半分になり、トルクが倍になりました。次に乗り上げ・接触ですが、シャーシ下で一番乗り上げたり障害物に接触しやすいのは、左右履帯のちょうど真ん中です。シングルモーター方式だと必ずモーターを中心に位置しないと行けないため、最も接触しやすくなっておりましたが、これを解消しました。接触が少なくなったため、耐久性を維持したまま刃を極めて鋭いカッターの刃にすることができました。これらにより筐体より大きな30cm程度の草を刈れるようになりました。本方式にしてから２０時間以上稼働させていますが、刃の破損は発生しておりません。

### 段差・斜面
芝生の庭などと異なり、中山間地では至るところに段差や斜面が存在しています。市販のロボット草刈り機はすべてタイヤ駆動ですが、Roktrackでは最初からクローラー（履帯）式を採用しました。しかし、クローラーと言っても筐体の絶対サイズが小さいため5cm程度の段差でも登ることができません。小さなクローラーでも段差を乗り越えられるようにドライブスプロケットに外側に張り出すように偏心タイヤ（後にかざぐるま型）を備えました。これにより段差に近づくとタイヤが引っかかり筐体が持ち上がるので、クローラーの下面に段差が接触出来るようになりました。しかしこのままでは、一定以上登ると後ろにひっくり返ってしまうので、とにかく前方荷重・低重心にすることで段差上面に荷重移動して乗り越えられるようになりました。斜面についても転倒防止と少しでもトラクションを高めるために、前方荷重・低重心にする必要がありました。これらにより、30度程度の斜面なら稼働できるようになっています。（これ以上の角度については、本筐体を少し工夫することで対応できるような仕組みを構想中。）

足回り、モーター、モータードライバ、カップリングなどの駆動系部品はほとんどAliexpressで調達しました。（大雪の中配達して頂いた配達員さんありがとうございます。）ボディはほとんどアルミ複合板で賄いました。加工しやすく、耐候性も高くとても使いやすいです。

### 有効草刈範囲と操作性
#### ロープによる境界判定
ロボット草刈り機開発に取り掛かった当初は、草刈り範囲にロープをキツめに張って、ロボット側には触覚を模したセンサーを取り付け境界判定をしていました。それなりにうまく行ったのですが新しい範囲を設定するのが非常に手間でした。また、庭などで使う場合は、ロープを降ろし忘れると足を引っ掛けて危ないので満足の行く出来とはなりませんでした。この方式は、範囲分のロープが必要ですし、新たな範囲設定が非常に手間でした。

#### GUIによる仮想境界設定
次はYOLOv5による物体検出を用い、三脚にカメラ付きRPiを設置し、その先にESP32で制御する草刈機を置くという方式にしました。スマホからRPiのGUIにアクセスし、カメラ画像に対してユーザーがポリゴンを描き、草刈り範囲とすることで、その範囲内で行動するようにRPiから草刈機に指示を出し続けるというものでした。とても柔軟に範囲設定が出来たのですが、草刈り有効範囲とシステム構成の複雑化がネックとなりました。前者については、30cm程度の物体では5mくらいまでしか物体検出が有効でなく、満足の行く範囲を一度に刈ることが出来ませんでした。また、カメラと草刈機、スマホという３つのデバイスを用いなければならず、可搬性と接続安定性の観点からストレスフルでしたので、次の方式を開発するに至ります。GUIの見た目などは先進的・未来的な感じがして最初は満足感はあったのですが、2週間から1ヶ月立つとまた草は生えてくるので、すぐに飽きてしまいました。

#### カラーコーン（パイロン）誘導方式
YOLOv7による物体検出はそのまま引き継ぎ、カラーコーンを検出してその中をぐるぐる回る方式に取り掛かりました。カラーコーンはホームセンターにいけば一つ３００円で入手できます。工事現場などで利用されているだけあって耐候性・安定性抜群でとても軽くてスタッキング出来ます。草刈範囲に変更があっても、カラーコーンを追加したり移動させたりするだけで対応できます。３０００枚の画像を撮影しラベル付け、Pytorch＋YOLOv5で学習させたところ、好条件下(晴天日陰一切なし)では40m先、悪条件下（木漏れ日環境）でも15ｍ先まで認識出来るようになりました。カラーコーンを正方形に設置した場合、机上では1600㎡の草刈に対応出来ます（そんな広い場所がなくテスト出来ていません）。また操作性に関しても、カラーコーンをおいてスイッチを押すだけで勝手に動き出すようになり繰り返しの作業も苦ではなくなりました。 また、目論んでいなかった副産物として、カラーコーンを2つだけ設置すれば面的にではなく線的に草刈りが可能となりました。動画のように畦の草刈りに適用できる可能性も出てきました。

#### 運用継続性
普通のカラーコーンの高さは70cm程度です。草で一定以上覆われてしまうと物体検出が出来なくなって草刈り不能となってしまいます。草が伸びきる前に定期的に草刈りをする必要があります。しかし、家の裏の庭ですら定期的に観察することは面倒で放置しがちです。そのため、アプリ側でESAのSentinel-2の衛星画像（解像度10m）を取得し、過去草刈地点の現在のNDVI（正規化差植生指数）を求め、直近の植生をリモートセンシングできるようにしました。 家から離れた遠隔地であっても、わざわざ現地に赴く必要なく草の伸び具合がわかります。

## 名称の由来
「Stroke」(泳ぎのクロールのような偏心タイヤ)＋「Track」(履帯)→「Roktrack」

## 運用、運用、運用

UIがカッコよくても草はすぐに生えます。
→パイロン置いてスイッチ入れるだけで刈れます。

いくらパワーがあっても草はすぐに生えます。
→12.8Vの4S LifePo4の低速充電で1000回位ゆっくり刈れるはず

部品が壊れても草はすぐに生えます。
→消耗部品はとても簡単に交換出来ます。

## 刈り取りできた雑草一覧
- Clover クローバー
- Persicaria longiseta イヌタデ
- Cayratia japonica ヤブガラシ
- Horsetail スギナ
- Commelina ツユクサ
- Sorrel スイバ
- Dokudami ドクダミ
- Crabgrass メヒシバ
- Persicaria thunbergii ミゾソバ

## 応用

- 大きな回転ブラシを作って庭掃除ロボ化したい(市販の電気ホウキでは屋外では容量不足)
- 不整地が得意なので何とか除雪の役に立てたい
- 工夫を凝らして60度くらいまでの斜面に対応させたい

# 更新履歴

- 2022/09/18 11:06 画像と動画を差し替え。
- 2022/10/07 20:00 冬になる前の追い込み開発内容を反映。
- 2022/10/18 15:00 ある程度の機能開発が終わったので、見た目をよくしました。他にもバンパーの割り込み化やUSBメモリへのログ出力機能など。速度を2km/h→1km/hに修正
- 2022/11/13 15:00 one-wayモードの追加。ギアモーター回転数の修正(52->56rpm)。タグの修正をしました。
- 2022/11/20 23:30 寒くなって刈る草がなくなったので試してみた草刈以外の実験的な機能を追記。
- 2022/12/03 13:00 急斜面・壁面対応状況について追記。