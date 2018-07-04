---
title: css
date: 2018-07-03 11:42:52
tags:
---
# CSS介紹
## <font color="blue">一、甚麼是CSS?</font>
CSS (Cascading Style Sheets) 網頁樣式表，用來定義HTML元素的顯示樣貌。能讓你在 HTML 文件中的元素（element）上套用不同的頁面樣式（style）
## <font color="blue">二、使用CSS優點</font>
1.可以製作個人化的的樣式設定檔案，以統一更新網站內的各網頁變化</br>
2.可獨立存css檔，與html檔分開撰寫，也可直接寫在html檔案內</br>
3.可以設定所有元件(object)的變化，包括文字、圖片、按鈕、視窗等</br>
4.可以建立共同樣式指令，在不同的物件套用相同的樣式設定</br>
## <font color="blue">三、套用方式</font>
1.標記加註式 (in-line)：如果只有一個 HTML 標記需要設定樣式，可在該標記內，加上屬性 style="CSS語法"，就可個別修訂樣式。
```    
實例說明：
<p style="color:red;font-size:80px;">這是inline寫法.</p>
```
2.網頁內嵌式 (embedded)：在 HTML 文件的< head > < /head > 之間，以< style > < /style > 來定義共同樣式，使整個網頁使用同一樣式。
```    
實例說明：
<head>
<style type="test/css">
p {
    color:#11afed;
    margin-left:12px;
}
</style>
</head>
```
3.外部設定式 (external)：由於一個網站由許多網頁所組成，盡量統一樣式，避免眼花繚亂，失去瀏覽的重點。 如果每一網頁均個別做樣式設定，萬一將來做修改時，需花費更多時間，因此可使每個網頁均連結到同一個.css的純文字檔，以設定整個網站的樣式。
```    
實例說明：
<head>
<link rel="stylesheet" type="text/css" href="external.css" />
</head>
```
## <font color="blue">四、了解CSS結構</font>
![CSS](/css/CSS.png)
```
宣告 CSS 樣式的語法：

選擇器 { 
  屬性：設定值； 
  ... 
}
```
### @選擇器（Selector）
在規則的最前頭為 HTML 的元素名。可以透過基本的選擇器去指定要處理的元素（在這個範例中,就是段落元素 p）。若要改變欲影響的元素，只需更改選擇器。
### @宣告（Declaration）
單一個規則，例如 color: red; 指定了這個元素的呈現樣貌。
### @屬性 (Properties)
修改屬性是改變你HTML元素的一種方法，(在這範例中, color 是段落（p）元素的一種屬性)在CSS中, 可以選擇哪些屬性用來影響 rule。
### @屬性值 (Property value)
屬性值就是位於屬性右邊，在冒號（:）之後，從眾多的可能樣式選出一個給予屬性（範例中是從眾多的 color 樣式中選出 red）。
## <font color="blue">五、CSS語法</font>
| 介紹          | 指令           | 詳細設定
| ------------- |:-------------:|:-------------:|
| 邊界      | margin       |margin-top (上邊界)<br>margin-right (右邊界)<br>margin-bottom (下邊界)<br>margin-left (左邊界)|
| 邊框      | borde        |border-style(邊框樣式)<br>border-width(邊框寬度)<br>border-color(邊框顏色)|
| 留白      | padding      |padding-top (上)<br>padding-bottom (下)<br>padding-left (左)<br>padding-right (右) |
| 背景      | background   |background-color(背景顏色)<br>background-image(背景圖案)<br>background-repeat(背景是否重複)<br>background-attachment(背景是否固定在螢幕上)<br>background-position(圖片位置)|
| 顏色      | color        |color:顏色|
| 字體      | font         |font-family(字型)<br>font-size(大小)<br>font-weight(厚度)<br>font-style(是否斜體)<br>font-variant(小型大寫)|
### <font color="blue">注意事項：</font>
#### 1.每一個規則當中，除了選擇器名稱以外，其他都必須被大括號（{}）給包住
#### 2.在每一個宣告裡面，屬性跟屬性值之間必須用冒號(:) 做區分
#### 3.在每一個規則裡面可以包含有許多宣告，但不同的宣告之間必須使用分號 (;) 來區分