# 清明重陽電子化計劃

## 動機

清明我去拜山，各位孝子賢孫都好有心，燒好多野俾D先人。但係燒祭品的時候，會釋放大量致癌物，造成空氣污染。
於是我就諗，有咩方法可以令到一眾後人表現到孝心之剩，又可以保護到環境。

政府成立科創局，大力推動科技創新。最近又設立[無盡思念](https://www.memorial.gov.hk/Default.aspx)網站，
令拜山電子化再唔係夢。

當然，要改變多年的傳統唔簡單，好多老一輩認為電子拜山太兒戲。佢地冇錯，就咁係網站上邊亂咁按幾野，絕對
表現唔到各位後人的孝心。但係咁唔代表電子化的方向係錯誤嘅，只係代表我地電子化的服務做得唔夠認真，唔夠
完善。我地應該要去解決問題，而唔係遇到少少困難，未嘗試就放棄，創新往往要經歷好多失敗。

## 方向

上文提到，老一輩認為電子拜山太兒戲。記念網站只能表現出對先人嘅懷念之情，但係係傳統中國文化當中，供奉
祖先都係重要嘅一環。電子拜山往往缺乏左供奉嘅一環，我希望可以透過電子燒香，電子化寶去填補電子拜山E一個
弱點。

單靠我個人嘅力量同水平，好難去推廣一個電子化寶。代入用户嘅角度去思考，無端端三唔識七，做咩要用你個網站？我用
你個網站去化寶，個網站會唔會私吞左D金銀元寶俾自己D祖先？完全冇公信力可言。

正如科創局局長所講，創新最緊要係有個平台，而電子化寶其實係一種交易系統，由陽間金錢交換做陰司紙同紙紮。
清明重陽電子化講到尾都係E-commerce。一個E-commerce最重要就係個貨幣系統，當中不可缺少嘅一環就係銀行。

# 冥府網上銀行

作為一個平台，最緊要提供到好用服務，容易做integration，咁先吸引到其他公司使用，著名的例子就有AWS，同埋
Twilio。因此冥府網上銀行會設計成RESTful API。

## Offline To Offline

銀行嘅主要功能不外乎係存款同提款，係電子系統當中，只係一D數字上的加減，唔係最考功夫的地方。冥府網上銀行
最需要技術，最需要專業知識的地方，係如何將實體冥幣轉換做電子冥幣，同埋將電子冥幣轉換送到先人手中。E個技
術問題，需要第三方寺廟同院舍協助解決，詳細方案將會在下文解釋。

## 系統設計

### 相關角色

1. 本系統：提供冥幣交易服務。
2. 寺院：處理線下冥幣，包括冥幣存款提款。
3. 孝子賢孫：可利用本系統供奉先人。

### 流程

#### 開戶

1. 孝子賢孫利用API開設網上銀行戶口，並設置銀行密碼。
2. 孝子賢孫得到銀行戶口號碼。

####

#### 存款

1. 孝子賢孫到寺院提供網上銀行戶口(無需密碼)並交款。
2. 寺院把金錢換算為冥幣後，利用本系統提供嘅API secret key，匯款至網上銀行戶口。

#### 提款

1. 先人向寺院要求提款(不需要聯系本系統任何工作人員)。
2. 由寺院對先人作出身份認證(不需要聯系本系統任何工作人員)。
3. 寺院利用本系統提供嘅API secret key，於網上銀行戶口提款。

#### 交易

未有解決方案。

# 進度

完成基本介紹
