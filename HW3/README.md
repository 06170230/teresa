# Binary Search Tree - Search.Insert.Delete.Modify功能介紹：
## Search
在二元搜尋樹b中查找x的過程為：

若b是空樹，則搜索失敗，否則：

若x等於b的根節點的數據域之值，則查找成功；否則：

若x小於b的根節點的數據域之值，則搜索左子樹；否則：

查找右子樹。

![Search搜尋過程](https://github.com/Teresakao0421/teresa/blob/master/binary%20tree/binary%20tree/search-流程圖.jpg)

## Insert
向一個二元搜尋樹b中插入一個節點s的算法，過程為：

若b是空樹，則將s所指節點作為根節點插入，否則：

若s->data等於b的根節點的數據域之值，則返回，否則：

若s->data小於b的根節點的數據域之值，則把s所指節點插入到左子樹中，

否則：把s所指節點插入到右子樹中。（新插入節點總是葉子節點）

![Insert搜尋過程](https://github.com/Teresakao0421/teresa/blob/master/binary%20tree/binary%20tree/insert-流程圖.jpg)

## Delete
在二叉查找樹刪去一個結點，分三種情況討論：

若*p結點為葉子結點，即PL（左子樹）和PR（右子樹）均為空樹。由於刪去葉子結點不破壞整棵樹的結構，則只需修改其雙親結點的指針即可。

若*p結點只有左子樹PL或右子樹PR，此時只要令PL或PR直接成為其雙親結點*f的左子樹（當*p是左子樹）或右子樹（當*p是右子樹）即可，作此修改也不破壞二叉查找樹的特性。

若*p結點的左子樹和右子樹均不空。在刪去*p之後，為保持其它元素之間的相對位置不變，可按中序遍歷保持有序進行調整，可以有兩種做法：其一是令*p的左子樹為*f的左/右（依*p是*f的左子樹還是右子樹而定）子樹，*s為*p左子樹的最右下的結點，而*p的右子樹為*s的右子樹；其二是令*p的直接前驅或直接後繼替代*p，然後再從二叉查找樹中刪去它的直接前驅（或直接後繼）。

![Delete搜尋過程](https://github.com/Teresakao0421/teresa/blob/master/binary%20tree/binary%20tree/delete.png)

## Modify
在這個tree當中，我想要將一個新的數字取代其中一個舊的數字，但這樣會打壞原本的BST所以我還要將被破壞的BST平衡回來。

只要符合左邊是小於或等於root，右邊是大於root即可。

![Modify搜尋過程](https://github.com/Teresakao0421/teresa/blob/master/binary%20tree/binary%20tree/modify-流程圖.jpg)