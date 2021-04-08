# 文泉书局导出PDF

- 申明：本教程仅供**已购买文泉书局版权内容的用户**参考，请勿用于任何获利途径；

## 项目介绍
本项目介绍如何将[文泉书局](https://wqbook.wqxuetang.com/)中的部分书籍导出为PDF文件，包含了源文件获取、源文件合并、源文件添加书签。本项目通过如何在文泉书局中获取[《系统架构设计师2013至2018年试题分析与解答》](https://wqbook.wqxuetang.com/book/3211900)进行使用步骤的说明（本人已在文泉书局中购买该电子书，**请广大读者尊重书籍版权**）。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/购买凭证.png" width=600 />
    </kbd>
   </div>

# 使用流程
## 查询书籍
通过网址[文泉书局](https://wqbook.wqxuetang.com/)，搜索相关书籍[《系统架构设计师2013至2018年试题分析与解答》](https://wqbook.wqxuetang.com/book/3211900)。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/search.png" width=500 />
    </kbd>
   </div>

# 源文件PDF下载

1、源文件PDF下载可参考项目[文泉书籍PDF下载](https://github.com/Kevin0z0/wenquan-pdf-download)，此项目介绍了如何将书籍进行PDF下载，实现原理：通过请求每一页PDF的图片，然后通过pdf.js转换为PDF文件。

2、使用时候请注意，如果运行工具后，等待很久没有自动翻页，表明工具未开始下载，请点击你想开始下载的页面启动下载即可（比如从第一页下载，就点击页面中的第一页PDF图片即可）。

3、单个PDF默认20页，可在脚本中自行修改，详细的使用教程可自行搜索其他教程。

# 源文件PDF合并
得到PDF源文件后，可通过WPS中的PDF合并工具进行合并。其他合并工具：Adobe acrobat 等。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/pdf合并.png" width=500 />
    </kbd>
   </div>

# PDF添加书签
1、在文泉书籍预览界面，F12后，在NetWork中搜索【目录】，然后复制右侧JSON，运行本项目中的index.html单页面。复制进【InPut JSON】后，自动将转换结果显示在【OutPut JSON】中。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/目录.png" width=500 />
    </kbd>
   </div>

<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/JSON转换.png" width=500 />
    </kbd>
   </div>

2、从[网盘链接，提取码：6666](https://pan.baidu.com/s/1Pr8C2SY4FtLjjv-wqxIlpA)下载工具后，操作步骤可参考[链接](https://www.jianshu.com/p/b7d4bf86f5ff)，其中的目录使用步骤1中的【OutPut JSON】即可。具体步骤如下：

* 点击从网盘链接下载的工具FreePic2Pdf，然后点击更改PDF。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step1.png" width=500 />
    </kbd>
   </div>

* 选择【往PDF挂书签】标签页，然后点击下图中的标号1，选择需要添加书签目录的PDF文件后。点击下图中的标号2，加载接口存放的文件夹（跟步骤1同文件夹）。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step2.png" width=500 />
    </kbd>
   </div>

* 然后依次点击下图箭头所示按钮。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step3.png" width=500 />
    </kbd>
   </div>

第一个为【编辑接口文件】按钮，如果编辑界面中空白，可复制下面代码输入保存（Ctrl+S）即可：
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step4.png" width=500 />
    </kbd>
   </div>

```javascript
[Images]

[Font] 
Language=GBK 
FontSize=7 
Margin=0.5

[Bkmk] 
File=FreePic2Pdf_bkmk.txt 
AddAsText=0 
ShowBkmk=1 
ShowAll=1 
BasePage=1

[Main] 
ContentsPage= 
TextPage=

```

第二个为【编辑书签（文本）】按钮，点击后，输入上面步骤1中的【OutPut JSON】即可，然后Ctrl+S保存。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step5.png" width=500 />
    </kbd>
   </div>

第三个为【编辑书签（树形）】按钮，可对书签最终的树形结构进行编辑，如果不需要编辑可不使用该功能。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step6.png" width=500 />
    </kbd>
   </div>

* 最后点击开始即可完成添加书签目录。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/step7.png" width=500 />
    </kbd>
   </div>


3、最终PDF如下。
<div align="center">
  <kbd><img src="https://raw.githubusercontent.com/xxlllq/PDFBooks/main/image/result.png" width=500 />
    </kbd>
   </div>
