![image](https://hackmd.io/_uploads/BkiXGKc7gx.png)


### Column 與 Row 的基本用法

* 預設情況下，Compose 會將多個 `Text` 元件堆疊在一起。
* 使用 `Column` 可垂直排列元件，使用 `Row` 則可水平排列元件。
* 功能相當於 XML 中的 `LinearLayout`。
* Compose 對巢狀結構的處理更有效率，不需擔心效能問題。

---

### Column / Row 的主軸與交叉軸

* 每個 Column 或 Row 有「主軸」與「交叉軸」概念。
* Column 的主軸為垂直方向，交叉軸為水平方向。
* Row 的主軸為水平方向，交叉軸為垂直方向。
* 主軸使用 `Arrangement` 控制，交叉軸使用 `Alignment` 控制。

---

### 對齊方式：Alignment 與 Arrangement

* Column 使用 `horizontalAlignment` 對齊交叉軸（橫向）。
* Column 使用 `verticalArrangement` 控制主軸（縱向）項目的排列。
* Row 則反之，使用 `verticalAlignment` 和 `horizontalArrangement`。
* Arrangement 可選值包含：

  * `Top`, `Bottom`, `Center`, `SpaceBetween`, `SpaceEvenly`, `SpaceAround`
* Alignment 可選值包含：

  * `Start`, `CenterHorizontally`, `End`, `CenterVertically` 等

---

### 使用 Modifier 修改外觀與大小

* 使用 `Modifier` 可以設定元件背景、尺寸、位置等屬性。
* `background(Color.Green)` 可設定背景顏色幫助視覺化布局。
* `fillMaxSize()` 會填滿整個可用空間。
* 若未設定尺寸，元件只會佔用其所需的最小空間，對齊效果可能不明顯。

---

### 尺寸設定：百分比與固定 dp

* `fillMaxWidth()`, `fillMaxHeight()` 可分別設定寬度與高度填滿。
* `fillMaxSize(fraction = 0.5f)` 可設定填滿指定比例空間。
* `width(200.dp)`、`height(300.dp)` 可設定固定尺寸。
* 可混合使用百分比與 dp 設定，例如寬度為 dp、高度為百分比。

---

### 使用示範：排列與間距

* `Arrangement.SpaceBetween`：首尾項目貼邊，中間平均分配空隙。
* `Arrangement.SpaceEvenly`：所有項目之間與外部的間距相等。
* `Arrangement.SpaceAround`：項目周圍有間距，邊緣間距為中間的一半。

---

### 其他補充

* `Modifier` 是 Compose 中非常重要的工具，可作用於任何 Composable。
* 更進階的 Modifier 使用會在後續影片中介紹。

---
* Jetpack Compose：Google 推出的現代化 Android UI 工具包，使用 Kotlin 建立 UI。
* Composable：Jetpack Compose 中可組合的 UI 元件，使用 `@Composable` 標註的函式。
* Column：垂直排列 Composables 的容器，類似 XML 中的 LinearLayout（垂直方向）。
* Row：水平排列 Composables 的容器，類似 XML 中的 LinearLayout（水平方向）。
* Modifier：Compose 中用來修飾 Composable 外觀與行為的工具，可調整大小、位置、背景等。
* fillMaxSize：使 Composable 填滿可用空間的 Modifier 函式。
* fillMaxWidth：使 Composable 填滿水平方向空間的 Modifier 函式。
* fillMaxHeight：使 Composable 填滿垂直方向空間的 Modifier 函式。
* width：設定 Composable 寬度的 Modifier 函式。
* height：設定 Composable 高度的 Modifier 函式。
* dp：密度無關像素單位，常用於設定寬高值。
* background：為 Composable 設定背景顏色的 Modifier 函式。
* verticalArrangement：定義 Column 內 Composables 垂直方向的排列方式。
* horizontalAlignment：定義 Column 內 Composables 水平方向的對齊方式。
* horizontalArrangement：定義 Row 內 Composables 水平方向的排列方式。
* verticalAlignment：定義 Row 內 Composables 垂直方向的對齊方式。
* Arrangement.Top：將 Composables 對齊至上方。
* Arrangement.Bottom：將 Composables 對齊至下方。
* Arrangement.Center：將 Composables 對齊至中間。
* Arrangement.SpaceBetween：在 Composables 之間平均分配空間（不含首尾）。
* Arrangement.SpaceAround：在 Composables 周圍平均分配空間（首尾有一半空間）。
* Arrangement.SpaceEvenly：在 Composables 間與首尾分配等量空間。
* Alignment.Start：將 Composables 靠左對齊。
* Alignment.End：將 Composables 靠右對齊。
* Alignment.CenterHorizontally：水平方向置中對齊。
* Alignment.CenterVertically：垂直方向置中對齊。
* setContent：在 Activity 中設定畫面內容的函式，取代過去的 `setContentView`。
* ConstraintLayout：傳統 XML 中常用的佈局方式，Compose 中也有對應版本。
* Layout Nesting：佈局巢狀結構，Compose 可更有效率處理巢狀。
* View：舊有 Android UI 元件的基礎類別，在 Compose 中已由 Composable 取代。
* Preview：使用 `@Preview` 註解預覽 Composable 外觀。
* Cross Axis：與主軸相對的軸線，在 Column 是水平，在 Row 是垂直。
* Main Axis：排放 Composables 的主要方向，Column 為垂直、Row 為水平。
* State：管理 UI 狀態的方式，Compose 使用可觀察的 State 管理。
* LazyColumn：可捲動的 Column，類似 RecyclerView 的功能。
* LazyRow：可捲動的 Row，用於水平捲動列表。
* Box：可重疊放置 Composables 的容器，類似 FrameLayout。
* Surface：提供 Material 樣式外觀的容器元件。
* MaterialTheme：Material Design 主題設定的入口。
* Text：顯示文字的基本 Composable。
* Color：Compose 中表示顏色的類別。
* Padding：用來設置內距的 Modifier 函式。
* Margin：Compose 沒有 margin，使用 Spacer 或排列策略實現。
* Spacer：在 Composables 之間創建空白區域的元件。
* Size Modifier：Modifier 函式之一，用於設定寬高。
* percentage size：使用 `fillMaxWidth` 或 `fillMaxHeight` 並搭配浮點數設定百分比大小。
* dp extension：Kotlin 擴充屬性，用於將數值轉為 dp 單位（如 200.dp）。
* arrangement 與 alignment 差異：arrangement 控制主軸排列、alignment 控制交叉軸對齊。
* Compose Preview Tooling：Android Studio 中即時預覽 Compose 畫面工具。
* Activity：Android UI 的基本元件之一，Compose UI 仍掛載於 Activity。
* Recomposition：UI 根據狀態變化重新繪製的行為。
* UI Tree：Compose 中的元件階層結構，替代傳統 View Tree。
* recomposition scope：Compose 自動追蹤狀態並重組的作用範圍。
* remember：Compose 中用於在重組時保留狀態的函式。
