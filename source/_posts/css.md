---
title: css
date: 2018-07-03 11:42:52
tags:
---
# CSS介紹
## 一、甚麼是CSS?
CSS (Cascading Style Sheets) 網頁樣式表，用來定義HTML元素的顯示樣貌。能讓你在 HTML 文件中的元素（element）上套用不同的頁面樣式（style）
## 二、使用CSS優點
    ❃可以製作個人化的的樣式設定檔案，以統一更新網站內的各網頁變化
    ❃可獨立存css檔，與html檔分開撰寫，也可直接寫在html檔案內
    ❃可以設定所有元件(object)的變化，包括文字、圖片、按鈕、視窗等
    ❃可以建立共同樣式指令，在不同的物件套用相同的樣式設定
## 三、套用方式
1.標記加註式 (in-line)：如果只有一個 HTML 標記需要設定樣式，可在該標記內，加上屬性 style="CSS語法"，就可個別修訂樣式。

2.網頁內嵌式 (embedded)：在 HTML 文件的< head > < /head > 之間，以< style > < /style > 來定義共同樣式，使整個網頁使用同一樣式。

3.外部設定式 (external)：由於一個網站由許多網頁所組成，盡量統一樣式，避免看得眼花繚亂，失去瀏覽的重點。 而且如果每一網頁均個別做樣式設定，萬一將來做修改時，需要花費更多時間，因此可使每個網頁均連結到同一個 .css 的純文字檔，以設定整個網站的樣式。
## 四、了解CSS結構
![CSS](pic/CSS.png)
### 選擇器（Selector）
    在規則的最前頭為 HTML 的元素名。它將決定你 HTML 裡什麼元素將被接下來的設定影響（在這個範例中,就是段落元素 p）。若要改變欲影響的元素，只需更改選擇器。
### 宣告（Declaration）
    單一個規則，例如 color: red; 指定了這個元素的呈現樣貌。
### 屬性 (Properties)
    修改屬性是改變你HTML元素的一種方法，(在這範例中, color 是段落（p）元素的一種屬性)在CSS中, 可以選擇哪些屬性用來影響 rule。
### 屬性值 (Property value)
    屬性值就是位於屬性右邊，在冒號（:）之後，從眾多的可能樣式選出一個給予屬性（範例中是從眾多的 color 樣式中選出 red）。
### 注意事項：
#### 1.每一個規則當中，除了選擇器名稱以外，其他都必須被大括號（{}）給包住
#### 2.在每一個宣告裡面，屬性跟屬性值之間必須用冒號(:) 做區分
#### 3.在每一個規則裡面可以包含有許多宣告，但不同的宣告之間必須使用分號 (;) 來區分