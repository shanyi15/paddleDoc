# Overview

_______

# Progress and todo list
## P1 4-16 update

**1. Fluid 文档上线官网**

Progress: 已上线，deadlink和图片、表格问题已修复，目前主要在推的几个小工作：（1）merge翻译稿 （2）新手入门的案例代码，调bug-ing

- [x] [Merged] Update release doc	https://github.com/PaddlePaddle/Paddle/pull/9729 -typhoonzero
- [ ] add rnn en doc https://github.com/PaddlePaddle/Paddle/pull/9809 -Superjomn 
- [ ] fix quick start for fluid https://github.com/PaddlePaddle/Paddle/pull/9820 -add rnn en doc 

**Former work**

- [x] [Merged] Add fluid doc support  https://github.com/PaddlePaddle/PaddlePaddle.org/pull/447 -Thuan
- [x] [Merged] Build Sphinx tree for fluid directory https://github.com/PaddlePaddle/Paddle/pull/9403 -weixing
- [x] Reclassify doc/fluid menu https://github.com/PaddlePaddle/Paddle/issues/9031 -shanyi @ranqiu
  - [x] [Merged]change the dir of docs https://github.com/PaddlePaddle/Paddle/pull/9104 -ranqiu
- [x] Primary/Second screen of fluid doc https://github.com/PaddlePaddle/Paddle/issues/9275 -shanyi @ranqiu
- [x] [Merged]Build basic sphinx doctree for doc/fluid https://github.com/PaddlePaddle/Paddle/pull/9236 -weixing
- [x] Record links of all .md files in the fluid directory https://github.com/PaddlePaddle/Paddle/issues/8976 -weixing
- [ ] Create new structure for fluid documentation https://github.com/PaddlePaddle/Paddle/issues/8587 -shanyi

**2.	fluid使用文档优化**
- [x] Request Opinion: move paddle.v2.dataset to paddle.dataset https://github.com/PaddlePaddle/Paddle/issues/8902 -shanyi @luotao
  - [x] 将fluid的api doc移动到doc/fluid/目录下 https://github.com/PaddlePaddle/Paddle/pull/9532 -weixing
- [x] Add title for kernel_hint_design.md & kernel_selection.md https://github.com/PaddlePaddle/Paddle/pull/9788 -weixing
- [x] Fix links error for github images https://github.com/PaddlePaddle/Paddle/pull/9641 -weixing
- [x] Upload fluid image sources to github https://github.com/PaddlePaddle/Paddle/pull/9633 -weixing
- [x] Fix table display errors for `.md` files  https://github.com/PaddlePaddle/Paddle/pull/9603 -weixing
- [x] Fix some dead links for fluid documents (cn version) https://github.com/PaddlePaddle/Paddle/pull/9561 -weixing
- [x] Adjust some contents in write_docs_en.rst for Contribue Documentation https://github.com/PaddlePaddle/Paddle/pull/9147 -weixing
- [x] Update index_en.rst https://github.com/PaddlePaddle/Paddle/pull/9257 -shanyi
- [x] Repair deadlink of sequence_tagging_for_ner https://github.com/PaddlePaddle/models/pull/749 -shanyi
- [x] repair image link in rnn.md https://github.com/PaddlePaddle/Paddle/pull/9272 -shanyi
- [x] Update index_en.rst https://github.com/PaddlePaddle/Paddle/pull/9241 -shanyi
- [x] repair image problem of en distributed training https://github.com/PaddlePaddle/Paddle/pull/9235 -shanyi
- [x] Repair deadlink of fluid doc https://github.com/PaddlePaddle/Paddle/pull/9226 -shanyi



**3.	API文档优化**
- [ ] Remove `dense_vector` from v2 api documents https://github.com/PaddlePaddle/Paddle/pull/9896 -weixing
- [x] API文档优化issue建立 
  https://github.com/PaddlePaddle/Paddle/issues?q=is%3Aissue+is%3Aopen+label%3Adocumentation+label%3Apythonapi -ranqiu
- [x] [Merged] 建立API 文档标准 https://github.com/PaddlePaddle/Paddle/pull/8927 -ranqiu
- [ ]  API doc display problem  https://github.com/PaddlePaddle/Paddle/issues/9059 -ranqiu
- [ ] API文档参数显示错误 https://github.com/PaddlePaddle/Paddle/issues/9055 -shanyi

**4.	文档翻译**
目的：翻译中/英文版使用文档，方便中/英文用户阅读
进展：v2+models文档翻译认领已启动，目前正在翻译中（v2有4篇没人认领，认领的已全部上交初稿，models全部认领，预计4月20日前完成），预计4月30日前翻译初稿完成。
V2 文档（认领： 20/24 完成：20/24）
https://shimo.im/sheet/PqK407VYm80Ju3dw
模型库 （认领：16/16  完成：13/16）
https://shimo.im/sheet/6XTZnRQEUS0uC1Ut 

**5.	文档构建&预览**
- [ ] Regenerate initializer.rst and add MSRAInitializer to initializer.__all__ https://github.com/PaddlePaddle/Paddle/pull/9870 -weixing
- [x] Exception occurred when constructing documentation https://github.com/PaddlePaddle/Paddle/issues/9006 -weixing 
  - [x] [Merged] The sphinx version is specified as 1.5.6 in the Dockerfile https://github.com/PaddlePaddle/Paddle/pull/9093 -weixing
- [x] Fix some outdated contents in Contribute Documentation https://github.com/PaddlePaddle/Paddle/issues/8993 -weixing
  - [x] [Merged]Fixed some outdated contents in Contribute Documentations https://github.com/PaddlePaddle/Paddle/pull/9016 -weixing
- [x] API预览工具错误 https://github.com/PaddlePaddle/PaddlePaddle.org/issues/442 -ranqiu
- [x] API doc display problem https://github.com/PaddlePaddle/Paddle/issues/9059 -ranqiu @cs2be
  - [x] [Merged]Fix issue of Paddle API documentation not updating on website https://github.com/PaddlePaddle/PaddlePaddle.org/pull/443 -cs2be
- [x]  [Merged] 修复build_doc https://github.com/PaddlePaddle/Paddle/pull/9233 
- [x]  [Merged] 移动fluid api doc目录，修复构建.sh https://github.com/PaddlePaddle/Paddle/pull/9532 -weixing


**6.	PaddlePaddle.org**
- [ ] the location of some of the triangle of drop list in the left navigator is incorrect https://github.com/PaddlePaddle/PaddlePaddle.org/issues/451
- [ ] The right anchor 's level and their position https://github.com/PaddlePaddle/PaddlePaddle.org/issues/464
- [ ] doc search function problem https://github.com/PaddlePaddle/PaddlePaddle.org/issues/454
- [x] move the version selector drop down menu a little bit to the right https://github.com/PaddlePaddle/PaddlePaddle.org/issues/432 
-shanyi @daming-lu
  - [x] [Merged]Align Versions to Right https://github.com/PaddlePaddle/PaddlePaddle.org/pull/436  -daminglu
- [x] Formula doesn't show correctly  https://github.com/PaddlePaddle/PaddlePaddle.org/issues/445 -shanyi
  - [x] Rewrite formula in MathJax so that it can be rendered correctly.https://github.com/PaddlePaddle/book/pull/505 -daminglu
- [ ] Type paddlepaddle.org or click the top left corner "PaddlePaddle" jump to the [dev] mainpage https://github.com/PaddlePaddle/PaddlePaddle.org/issues/431 -shanyi
- [ ] API link problem of v 0.11.0/0.10.0/0.9.0 https://github.com/PaddlePaddle/PaddlePaddle.org/issues/428 -shanyi
- [ ] Delete the left navigation bar in "Mobile" https://github.com/PaddlePaddle/PaddlePaddle.org/issues/388 shanyi
- [ ] API documentation left navigation expand to 3rd level links https://github.com/PaddlePaddle/PaddlePaddle.org/issues/384 -shanyi
- [ ] Change the way of selecting versions https://github.com/PaddlePaddle/PaddlePaddle.org/issues/381

**7.	日常文档修复**
- [ ] Repair doc format problem https://github.com/PaddlePaddle/Paddle/issues/8733 -shanyi
- [ ] Repair the indent format problem https://github.com/PaddlePaddle/PaddlePaddle.org/issues/435- shanyi @daming-lu
- [ ] Repair the page anchor location problem https://github.com/PaddlePaddle/PaddlePaddle.org/issues/434 -shanyi @daming-lu
- [ ] Blank space between paragraph should be narrower https://github.com/PaddlePaddle/PaddlePaddle.org/issues/417 -shanyi
- [ ] Format problem of documentation https://github.com/PaddlePaddle/Paddle/issues/8274 -shanyi
