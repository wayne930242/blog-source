---
title: CoC 7 的追逐怎麼處理？一個解決方案
categories: TRPG
date: 2021-01-06 14:24:59
tags:
  - 規則
  - CoC
---

{% img /img/bike-riding.jpg %}

追逐，在 CoC 7 的遊戲中十分重要。無論是逃亡還是追趕，都是令人緊張的時刻。

我知道有許多守密人不喜歡它，因為要做的事情有點太多。在這篇文章中，我會提出個有趣簡便的追逐規則解決方案。

開始前，讓我們複習一下追逐規則。

<!--more-->

# CoC 7 追逐規則

追逐規則分成四個部分：

1. 建立追逐
2. 建立區位
3. 開始追逐
4. 結束追逐

**1. 建立追逐**：所有參與追逐者，進行一次 Con 檢定或是交通工具的技能檢定。如果極限成功， MOV +1，如果失敗， MOV -1，其他狀況下 MOV 不變。確定有多少人會進入追逐：

- **剔除追不上的人**：逃跑者中 MOV 最低的人是門檻，所有沒達到的追趕者都可以剔除。

**2. 建立區位**：區位是一個抽象的空間單位，可以想成「一回合中，速度最慢的移動者可以離開的空間」。速度最慢的移動者如果是人類，這可能是一個房間、一層樓。如果是交通工具，可能是一個街區、一個路口。然後守密人根據前方路線，建立一個又一個區位。

狀況更複雜的話，逃跑者可能分頭跑、一起跑、分組跑，守密人可能得決定多條路線的區位。

區位的類型包括：

- **淨空**：追逐者可以無障礙地進入、離開這個區位。
- **危害**：追逐者離開該區位前進時，必須通過某個檢定（守密人決定難度和需要的技能或屬性），如果失敗，他會失去 1D3 個行動（見「3. 開始追逐」）。更慢地通過危害可以讓這個檢定有獎勵骰（2 MOV 一個獎勵、3 MOV 兩個獎勵）。
- **障礙**：在障礙去除或通過某個檢定前，追逐者無法離開該區位前進。

**3. 開始追逐**：決定行動順序，通常就是按照 DEX 排列。每個追逐者可以採取多個行動：

- MOV 最低的所有追逐者，只能進行一次行動。
- 比 MOV 最低的追逐者快的人，每多 1 MOV 可以多進行一次行動。

每次行動可以用來進行一項動作：

- 往前跑，移動一個區位。如果是交通工具，可能移動 2 至 5 個區位。
- 發起一次攻擊：使用戰鬥、火器或駕駛技能（有些東西可能會進行不只一次攻擊）。
- 施放一個咒語。
- 作其他需要花時間的事，像是開鎖，或是製造危害/障礙。
- 往後跑，或站著不動。

**4. 結束追逐**：有以下幾種結束追逐的方法：

- 跑到了守密人設想的地點。
- 跑到可以躲藏的地方通過檢定躲起來，並且，追逐者並未通過發現隱藏的檢定。
- 守密人覺得跑得夠遠了、跑出場景了。

# 問題在哪？

對於守密人來說，最困難的事情在於決定區位的內容。畢竟，追逐的場合經常不是劇本中所描述的。這就像是戰鬥，只是情境更加複雜。官方雖然有提供「隨機障礙/危害表」，但是守密人依然容易手忙腳亂。

規則雖然看起來有點複雜，但是試幾次以後你應該會慢慢習慣才對。

問題就是太手忙腳亂了，一下子要畫區位、一下子要標追逐者位置、一下子還要決定區位內容（不管是使用隨機區位還是別的，這都是很辛苦的事），還要思考：什麼時候可以讓玩家角色進行躲藏。

我提出的解決方案是，保留這個「隨機障礙/危害表」，但讓狀況變得更好處理。這個方法來自於我在看《Aces and Eights》時受到的啟發。

# 解決方案

我們需要以下工具：

- 一副撲克牌（拿掉鬼牌）
- 幾個可以代表追逐者的指示物

建立區位：

- 將撲克牌面朝下排成一列，每張代表一個**區位**。
- 將指示物放在撲克牌上。在追逐開始前，將追逐者和逃亡者之間的間距排好（通常差距 2 **區位**）。
- 每當有指示物進入一個區位時，翻開撲克牌，根據牌面宣讀該區位的狀況。
- 如果那邊看起來是暢通無阻的地方，在翻牌時額外翻開一張，取低的作為區位的牌面。

牌面意義（根據官方的隨機區位表）：

- A-7：代表**淨空**。這種情況略大於一半。
- 8-10：紅色代表**危害**，黑色代表**障礙**，檢定難度是「一般」。
- J、Q：紅色代表**危害**，黑色代表**障礙**，檢定難度是「困難」。
- K：紅色代表**危害**，黑色代表**障礙**，檢定難度是「極限」。

應用：

- 如果你想使用**突發危害**規則：每當角色進入 A 或 5 的時候，讓他進行**幸運**檢定，（沒有幸運的 NPCs 可以擲 POW），失敗時，**突發危害**發生（克服難度通常為「一般」）。
- 你可以用撲克牌簡單地呈現岔路，讓玩家可以決定朝哪個方向前進。
- 你可以決定一個號碼是「能夠躲藏的地方」（如 2 號），讓玩家角色可以在這裡嘗試躲藏來逃脫追逐。
- 你可以先抽出 10 張牌，表示這是這次追逐最多的區位。意思是，只要這邊的牌用完就逃脫了。
- 你可以先抽出 20 張牌，加入鬼牌，宣告這就是玩家要尋找的逃脫點。你可能想要先抽出 5 張，來確保角色不會一下子就離開。

