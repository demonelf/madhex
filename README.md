创建 Hexo 主题非常容易，您只要在`themes`文件夹内，新增一个任意名称的文件夹，并修改`_config.yml`内的`theme`设定，即可切换主题。一个主题可能会有以下的结构：

| .├── \_config.yml├── languages├── layout├── scripts└── source |
| :--- |


### \_config.yml {#config-yml}

主题的配置文件。修改时会自动更新，无需重启服务器。

### languages {#languages}

语言文件夹。请参见[国际化 \(i18n\)](https://hexo.io/zh-cn/docs/internationalization.html)。

### layout {#layout}

布局文件夹。用于存放主题的模板文件，决定了网站内容的呈现方式，Hexo 内建[Swig](http://paularmstrong.github.com/swig/)模板引擎，您可以另外安装插件来获得[EJS](https://github.com/hexojs/hexo-renderer-ejs)、[Haml](https://github.com/hexojs/hexo-renderer-haml)或[Jade](https://github.com/hexojs/hexo-renderer-jade)支持，Hexo 根据模板文件的扩展名来决定所使用的模板引擎，例如：

| layout.ejs   - 使用 EJSlayout.swig  - 使用 Swig |
| :--- |


您可参考[模板](https://hexo.io/zh-cn/docs/templates.html)以获得更多信息。

### scripts {#scripts}

脚本文件夹。在启动时，Hexo 会载入此文件夹内的 JavaScript 文件，请参见[插件](https://hexo.io/zh-cn/docs/plugins.html)以获得更多信息。

### source {#source}

资源文件夹，除了模板以外的 Asset，例如 CSS、JavaScript 文件等，都应该放在这个文件夹中。文件或文件夹开头名称为`_`（下划线线）或隐藏的文件会被忽略。

如果文件可以被渲染的话，会经过解析然后储存到`public`文件夹，否则会直接拷贝到`public`文件夹。

### 发布 {#发布}

当您完成主题后，可以考虑将它发布到[主题列表](https://hexo.io/themes)，让更多人能够使用您的主题。在发布前建议先进行[主题单元测试](https://github.com/hexojs/hexo-theme-unit-test)，确保每一项功能都能正常使用。发布主题的步骤和[更新文档](https://hexo.io/zh-cn/docs/contributing.html#更新文档)非常类似。

1. Fork
   [hexojs/site](https://github.com/hexojs/site)
2. 把库（repository）复制到电脑上，并安装所依赖的插件。

   | $ git clone [https://github.com/&lt;username&gt;/site.git$](https://github.com/<username>/site.git$) cd site$ npm install |
   | :--- |

3. 编辑`source/_data/themes.yml`，在文件中新增您的主题，例如：

   | - name: landscape  description: A brand new default theme for Hexo.  link: [https://github.com/hexojs/hexo-theme-landscape](https://github.com/hexojs/hexo-theme-landscape)  preview: [http://hexo.io/hexo-theme-landscape](http://hexo.io/hexo-theme-landscape)  tags:    - official    - responsive    - widget    - two\_column    - one\_column |
   | :--- |

4. 在`source/themes/screenshots`新增同名的截图档案，图片必须为 800x500 的 PNG 文件。

5. 推送（push）分支。

6. 建立一个新的合并申请（pull request）并描述改动。

![](/assets/dd878e9f51b55c4bd574df4275cc35c0.jpg)

