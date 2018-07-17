---
title: kubernetes
date: 2018-07-12 11:44:57
tags:
---
# kubernetes
## <font color="blue">前言</font>
當任一台伺服器流量過頭的時候，希望可以自動擴展；當流量很低迷時，可以自動縮減伺服器。而最重要的是，當一台伺服器掛點後，希望可以自動修復，而且隨時必須保持服務實例的個數。以上很多功能Docker都可以做到，並利用容器來提供服務。這樣的服務型態被稱作CaaS(Container as a Service)<br>
但是Docker不是萬能，在容器/服務個數越來越複雜的情況下，如何管理叢集和服務的生命週期，將會是各家容器編排管理(orchestration)的能力。其中Google的Kubernetes就是一個容器編排管理工具。
## <font color="blue">一、甚麼是kubernetes？</font>
「Kubernetes」一名取自於希臘原文，意即「掌舵手、船長」，8的由來則是"ubernete"八個字母縮寫。kubernetes(k8s)是一個由Google開發並開源的系統，專門用以自動化部屬、彈性擴充及容器應用管理。
## <font color="blue">二、K8S與手動部屬的差別</font>
1.同時部屬多個containers到一台機器上，甚至多台機器<br>
2.管理各個container的狀態。如果提供某個服務的container不小心crash了，kubernetes會偵測到並重啟這個container，確保持續提供服務。<br>
3.將一台機器上所有的containers轉移至另一台機器上。<br>
4.提供機器高度擴張性。kubernetes cluster可以從一台機器，延展到多台機器共同運行。
## <font color="blue">三、Kubernetes的優點</font>
1.可以跑在任何地方Can run anywhere<br>
    kubernetes可以運行在任何地方；不論是私有雲、公有雲(像是AWS、Google Cloud Platform)、或混合雲。<br>
2.高度模組化High modular<br>
    每個服務都被切成一個container，不論是要做修改、擴張、甚至將服務遷移到另外一台機器都可以快速被部屬。<br>
3.活躍的社群Open source & active community<br>
    Kubernetes是開源的，受到社群的關注也非常高。<br>
## <font color="blue">四、Kubernetes的架構</font>
### k8s屬分布式系統，主要元件有：
### 1.Master(server端) -扮演管理叢集的角色，可以透過CLI、API或控制介面等等不同方式與Master溝通進而存取、控制或修改叢集狀態，EX：配置資源、擴充Pob數量。
1.1 API Sever：管理者會將需要做的工作(EX：新增或刪除元件)傳送至API-server，API-server會驗證並處理管理者要求執行的工作，當工作執行完畢之後，叢集的最新狀態就會儲存至etcd。<br>
1.2 Controller Manager：會透過API Server了解目前叢集的狀況，並嘗試把目前狀態調整為管理者想要的狀態<br>
1.3 etcd：kubernetes中的每個組件(API服務器、調度程序、kubelet、控制器管理器等)都是無狀態的，所有狀態都存儲在etcd中，組件之間的通信通常透過etcd進行。Master會透過etcd了解目前叢集的運行狀況，etcd可以是Master的一部份或是獨立被設置在外部，當etcd被設置在外部時，Master會連到etcd取得或更新叢集狀態。<br>
1.4 scheduler：排程作業，scheduler會知道目前Worker Node的狀況，當需要配置Pod時，scheduler會找出最合適的Node並配置Pod。
### 2.Node：簡單說是一台機器，可以是實體機或虛擬機(VM)，而多個運行單位Pod會被配置到Node中運行，而每個Pod中含有一到多個容器。

