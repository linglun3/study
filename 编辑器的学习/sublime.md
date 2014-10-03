<body marginheight="0"><h1>Sublime 安装学习笔记</h1>
<h2>一、什么是sublime</h2>
<p>Sublime Text具有<strong>漂亮的用户界面和强大的功能</strong>，还可自定义键绑定，菜单和工具栏。
Sublime Text 的主要功能包括：
拼写检查，书签，完整的 Python API ， Goto 功能，
即时项目切换，多选择，多窗口等。 Sublime Text 是一个跨平台的编辑器
，同时支持Windows、Linux、Mac OS X等操作系统。

</p>
<p>Sublime Text 2还具有<strong>良好的扩展能力和完全开放的用户自定义配置
与神奇实用的编辑状态恢复功能</strong>。支持强大的多行选择和多行编辑。
强大的快捷命令“可以实时搜索到相应的命令、选项、snippet 和 syntex，
按下回车就可以直接执行，减少了查找的麻烦。即时的文件切换。
随心所欲的跳转到任意文件的任意位置。多重选择功能允许在页面中同时存在多个光标。


</p>
<p>SublimeText 2还有<strong>编辑状态恢复的能力</strong>，即当你修改了一个文件，但没有保存，
这时退出软件，软件不询问用户是否要保存的，因为无论是用户自发退出还是意外崩溃退出，
下次启动软件后，之前的编辑状态都会被完整恢复，就像退出前时一样。

</p>
<h2>二、sublime的插件添加</h2>
<h3>方法一</h3>
<ul>
<li>下载所需要的插件。</li>
<li>解压后，并放入Packages目录中。找到Packages目录的简单方法是在Sublime Text 2 
的Preferences菜单中选择Browse Packages。</li>
<li>重启Sublime Text 2</li>
</ul>
<h3>方法二 通过Package控制插件 <em>Sublime Package Control</em></h3>
<ul>
<li>安装 Package Control 的方法：</li>
<li>打开 Sublime Text 2，按下 Control + ` 调出 Console</li>
<li>将以下代码粘贴进命令行中并回车：<pre><code>import urllib2,os;pf='Package Control.sublime-package';
ipp=sublime.installed_packages_path();
os.makedirs(ipp) if not os.path.exists(ipp) else None;
open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())</code></pre>
</li>
<li>重启 Sublime Text 2，如果在 Preferences -&gt; Package Settings中见到Package Control这一项，就说明安装成功了。</li>
<li>安装好Package Control后，就可以用它来安装其它的插件了。</li>
<li>按下 Shift + Command + P 调出命令面板。</li>
<li>输入 install 调出 Package Control: Install Package 选项，按下回车。</li>
</ul>
<h2>三、SASS插件安装</h2>
<p>SASS是一门<strong>著名的CSS预处理器语言</strong>，而Sublime Text则堪称界面最优雅的编辑器之一。
为ST配置了SASS的插件之后，便可以在ST中很方便的支持SASS的语法高亮以及一键编译。

</p>
<p>但是，SASS需要Ruby环境的支持，因此首先要下载并安装对应版本的<a href="http://rubyinstaller.org/downloads/">Ruby Installer for Windows</a>。
然后在开始菜单中启动Start Command Prompt with Ruby，在弹出的命令行界面中输入:

</p>
<pre><code>  gem install sass</code></pre>
<p>再次打开控制台，选择Package Contrl: Install Package，
依次搜索并回车安装Sass和SASS Build两个插件。
安装成功后，.scss文件就可以正常使用代码高亮国。如果文件名后缀是.css，
也可以在控制台中搜索SASS选择Set Syntax: SASS以切换模式。
可以使用 工具 &gt; 编译 或者快捷键Ctrl + B编译文件，
会自动在当前目录生成一个同名的编译后的CSS文件。

</p>
<p>Edit By Jimmybao
Edit By <a href="http://mahua.jser.me">MaHua</a></p>
</body></html>