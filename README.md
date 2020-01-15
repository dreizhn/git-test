
<!Doctype html>
<html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
  <meta property="qc:admins" content="465267610762567726375" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<title>Git 远程仓库(Github) | 菜鸟教程</title>

  <link rel='dns-prefetch' href='//s.w.org' />
<link rel="canonical" href="http://www.runoob.com/git/git-remote-repo.html" />
<meta name="keywords" content="Git 远程仓库(Github)">
<meta name="description" content="Git 远程仓库(Github) Git 并不像 SVN 那样有个中心服务器。  目前我们使用到的 Git 命令都是在本地执行，如果你想通过 Git 分享你的代码或者与其他开发人员合作。 你就需要将数据放到一台其他开发人员能够连接的服务器上。 本例使用了 Github 作为远程仓库，你可以先阅读我们的 Github 简明教程。 添加远程库 要添加一个新的远程仓库，可以指定一个简单的名字，以便将来引用,命令格式如下：  git remot..">
		
	<link rel="shortcut icon" href="//static.runoob.com/images/favicon.ico" mce_href="//static.runoob.com/images/favicon.ico" type="image/x-icon" >
	<link rel="stylesheet" href="/wp-content/themes/runoob/style.css?v=1.154" type="text/css" media="all" />	
	<link rel="stylesheet" href="//static.runoob.com/assets/font-awesome/4.7.0/css/font-awesome.min.css" media="all" />	
  <!--[if gte IE 9]><!-->
  <script src="//static.runoob.com/assets/jquery/2.0.3/jquery.min.js"></script>
  <!--<![endif]-->
  <!--[if lt IE 9]>
     <script src="//cdn.staticfile.org/jquery/1.9.1/jquery.min.js"></script>
     <script src="//cdn.staticfile.org/html5shiv/r29/html5.min.js"></script>
  <![endif]-->
  <link rel="apple-touch-icon" href="//static.runoob.com/images/icon/mobile-icon.png"/>
  <meta name="apple-mobile-web-app-title" content="菜鸟教程">
</head>
<body>

<!--  头部 -->
<div class="container logo-search">

  <div class="col search row-search-mobile">
    <form action="index.php">
      <input class="placeholder" placeholder="搜索……" name="s" autocomplete="off">
    </form>
  </div>

  <div class="row">
    <div class="col logo">
      <h1><a href="/">菜鸟教程 -- 学的不仅是技术，更是梦想！</a></h1>
    </div>
        <div class="col right-list"> 
    <button class="btn btn-responsive-nav btn-inverse" data-toggle="collapse" data-target=".nav-main-collapse" id="pull" style=""> <i class="fa fa-navicon"></i> </button>
    </div>
        <div class="col search search-desktop last">
      <form action="//www.runoob.com/" target="_blank">
        <input class="placeholder" id="s" name="s" placeholder="搜索……"  autocomplete="off">
      </form>
    </div>
  </div>
</div>


<!-- 导航栏 -->
<!-- 导航栏 -->
<div class="container navigation">
	<div class="row">
		<div class="col nav">
			<ul class="pc-nav">
				<li><a href="//www.runoob.com/">首页</a></li>
				<li><a href="/html/html-tutorial.html">HTML</a></li>
				<li><a href="/css/css-tutorial.html">CSS</a></li>
				<li><a href="/js/js-tutorial.html">JavaScript</a></li>
				<li><a href="/jquery/jquery-tutorial.html">jQuery</a></li>
				<li><a href="/bootstrap/bootstrap-tutorial.html">Bootstrap</a></li>
				<li><a href="/python3/python3-tutorial.html">Python3</a></li>
				<li><a href="/python/python-tutorial.html">Python2</a></li>
				<li><a href="/java/java-tutorial.html">Java</a></li>
				<li><a href="/cprogramming/c-tutorial.html">C</a></li>
				<li><a href="/cplusplus/cpp-tutorial.html">C++</a></li>
				<li><a href="/csharp/csharp-tutorial.html">C#</a></li>
				<li><a href="/sql/sql-tutorial.html">SQL</a></li>
				<li><a href="/mysql/mysql-tutorial.html">MySQL</a></li>
				<li><a href="/php/php-tutorial.html">PHP</a></li>
				
				<li><a href="/browser-history">本地书签</a></li>
				<!--
					<li><a style="font-weight:bold;" href="https://www.runoob.com/linux/linux-cloud-server.html" target="_blank" onclick="_hmt.push(['_trackEvent', 'aliyun', 'click', 'aliyun'])"  title="kkb">云服务器</a></li>
			
				<li><a href="/w3cnote/knowledge-start.html" style="font-weight: bold;" onclick="_hmt.push(['_trackEvent', '星球', 'click', 'start'])" title="我的圈子">我的圈子</a></li>				
				<li><a href="javascript:;" class="runoob-pop">登录</a></li>
				-->
      		</ul>
			<ul class="mobile-nav">
				<li><a href="//www.runoob.com/">首页</a></li>
				<li><a href="/html/html-tutorial.html">HTML</a></li>
				<li><a href="/css/css-tutorial.html">CSS</a></li>
				<li><a href="/js/js-tutorial.html">JS</a></li>
				<li><a href="/browser-history">本地书签</a></li>
				<a href="javascript:void(0)" class="search-reveal">Search</a> 
			</ul>
			
		</div>
	</div>
</div><!--  内容  -->
<div class="container main">
	<!-- 中间 -->
	<div class="row">
	
<div class="col left-column">
	<div class="tab">Git 教程	<a data-cate="169" href="javascript:void(0);" title="夜间模式"  id="moon"><i class="fa fa-moon-o" aria-hidden="true" style="font-size: 1.4em;float: right;margin: 4px 6px 0;"></i></a>
	<a data-cate="169" style="display:none;" href="javascript:void(0);" title="日间模式"  id="sun" ><i class="fa fa-sun-o" aria-hidden="true" style="font-size: 1.4em;float: right;margin: 4px 6px 0;"></i></a>
	</div>
	<div class="sidebar-box gallery-list">
		<div class="design" id="leftcolumn">
						<a target="_top" title="Git 教程"  href="/git/git-tutorial.html" >
			Git 教程			</a>
						<a target="_top" title="Git 安装配置"  href="/git/git-install-setup.html" >
			Git 安装配置			</a>
						<a target="_top" title="Git 工作流程"  href="/git/git-workflow.html" >
			Git 工作流程			</a>
			<a target="_top" title="Git 工作区、暂存区和版本库" href="git-workspace-index-repo.html"> Git 工作区、暂存区和版本库 </a>			<a target="_top" title="Git 创建仓库"  href="/git/git-create-repository.html" >
			Git 创建仓库			</a>
						<a target="_top" title="Git 基本操作"  href="/git/git-basic-operations.html" >
			Git 基本操作			</a>
						<a target="_top" title="Git 分支管理"  href="/git/git-branch.html" >
			Git 分支管理			</a>
						<a target="_top" title="Git 查看提交历史"  href="/git/git-commit-history.html" >
			Git 查看提交历史			</a>
						<a target="_top" title="Git 标签"  href="/git/git-tag.html" >
			Git 标签			</a>
						<a target="_top" title="Git 远程仓库(Github)"  href="/git/git-remote-repo.html" >
			Git Github			</a>
						<a target="_top" title="Git 服务器搭建"  href="/git/git-server.html" >
			Git 服务器搭建			</a>
				
		</div>
	</div>	
</div>	<div class="col middle-column">
		
	
	<div class="article">
			<div class="article-heading-ad" style="display: none;">
		
		</div>
		<div class="previous-next-links">
			<div class="previous-design-link"><i style="font-size:16px;" class="fa fa-arrow-left" aria-hidden="true"></i> <a href="http://www.runoob.com/git/git-tag.html" rel="prev"> Git 标签</a> </div>
			<div class="next-design-link"><a href="http://www.runoob.com/git/git-server.html" rel="next"> Git 服务器搭建</a> <i style="font-size:16px;" class="fa fa-arrow-right" aria-hidden="true"></i></div>
		</div>
		<div class="article-body">
		
			<div class="article-intro" id="content">
			
			<h1>Git 远程仓库(Github)</h1>
<p>Git 并不像 SVN 那样有个中心服务器。 </p>
<p>目前我们使用到的 Git 命令都是在本地执行，如果你想通过 Git 分享你的代码或者与其他开发人员合作。
你就需要将数据放到一台其他开发人员能够连接的服务器上。</p>
<p>本例使用了 Github 作为远程仓库，你可以先阅读我们的 <a target="_blank" href="/w3cnote/git-guide.html" rel="noopener noreferrer">Github 简明教程。</a>
<hr><h2>添加远程库</h2>
<p>要添加一个新的远程仓库，可以指定一个简单的名字，以便将来引用,命令格式如下：</p>
<pre>
git remote add [shortname] [url]
</pre>
<p>本例以 Github 为例作为远程仓库，如果你没有 Github 可以在官网 <a href="https://github.com/" target="_blank" rel="noopener noreferrer">https://github.com/</a>注册。</p>
<p>
</p>
<p>由于你的本地 Git 仓库和 GitHub 仓库之间的传输是通过SSH加密的，所以我们需要配置验证信息：</p>
<p>使用以下命令生成 SSH Key：</p>
<pre>$ ssh-keygen -t rsa -C "youremail@example.com"</pre>

<p>
后面的 <strong>your_email@youremail.com</strong> 改为你在 Github 上注册的邮箱，之后会要求确认路径和输入密码，我们这使用默认的一路回车就行。成功的话会在 ~/ 下生成 .ssh 文件夹，进去，打开 <strong>id_rsa.pub</strong>，复制里面的 <strong>key</strong>。</p>
<p>回到 github 上，进入 Account => Settings（账户配置）。</p>
<p><img src="/wp-content/uploads/2015/03/48840BF0-992F-4CCC-A388-15CB74819D88.jpg"></p>
<p>左边选择 <strong>SSH and GPG keys</strong>，然后点击 <strong>New SSH key</strong> 按钮,title 设置标题，可以随便填，粘贴在你电脑上生成的 key。</p>
<p><img src="/wp-content/uploads/2015/03/106AD534-A38A-47F3-88A3-B7BE3F2FEEF1.jpg"></p>
<p>添加成功后界面如下所示
<p><p>
<img src="/wp-content/uploads/2015/03/EC8F8872-091A-4CAB-90F2-616F34F350A9.jpg"/></p>
<p>为了验证是否成功，输入以下命令：</p>
<pre>
$ ssh -T git@github.com
Hi tianqixin! You've successfully authenticated, but GitHub does not provide shell access.
</pre>
<p>以下命令说明我们已成功连上 Github。</p>
<p>
之后登录后点击" New repository " 如下图所示：</p>
<img src="//www.runoob.com/wp-content/uploads/2015/03/github1.jpg"/>
<p>之后在在Repository name 填入 runoob-git-test(远程仓库名)
，其他保持默认设置，点击"Create repository"按钮，就成功地创建了一个新的Git仓库：</p>
<img src="//www.runoob.com/wp-content/uploads/2015/03/299CF000-7B6E-4BEC-B8C2-D9AEB053307B.jpg"/>
<p>创建成功后，显示如下信息：</p>
<img src="//www.runoob.com/wp-content/uploads/2015/03/1BCB4379-1A25-4C77-BB82-92B3E7185435.jpg"/>
<p>以上信息告诉我们可以从这个仓库克隆出新的仓库，也可以把本地仓库的内容推送到GitHub仓库。</p>


<p>
现在，我们根据 GitHub 的提示，在本地的仓库下运行命令：</p>
<pre>
$ mkdir runoob-git-test                     # 创建测试目录
$ cd runoob-git-test/                       # 进入测试目录
$ echo "# 菜鸟教程 Git 测试" &gt;&gt; README.md     # 创建 README.md 文件并写入内容
$ ls                                        # 查看目录下的文件
README
$ git init                                  # 初始化
$ git add README.md                         # 添加文件
$ git commit -m "添加 README.md 文件"        # 提交并备注信息
[master (root-commit) 0205aab] 添加 README.md 文件
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

# 提交到 Github
$ git remote add origin git@github.com:tianqixin/runoob-git-test.git
$ git push -u origin master
</pre>
<p>以下命令请根据你在Github成功创建新仓库的地方复制，而不是根据我提供的命令，因为我们的Github用户名不一样，仓库名也不一样。</p>
<p>接下来我们返回 Github 创建的仓库，就可以看到文件已上传到 Github上：</p>
<img src="/wp-content/uploads/2015/03/53CA927D-F36F-4A00-AFB2-5EAED05B535E.jpg"/>
<hr><h2>查看当前的远程库</h2>
<p>要查看当前配置有哪些远程仓库，可以用命令：</p>
<pre>git remote</pre>
<h3>实例</h3>
<pre>
$ git remote
origin
$ git remote -v
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (fetch)
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (push)
</pre>
<p>执行时加上 -v 参数，你还可以看到每个别名的实际链接地址。</p>

<hr>
<h2>提取远程仓库</h2>
<p>
Git 有两个命令用来提取远程仓库的更新。</p>
<p>1、从远程仓库下载新分支与数据：</p>
<pre>git fetch</pre>
<p>该命令执行完后需要执行git merge 远程分支到你所在的分支。</p>
<p>2、从远端仓库提取数据并尝试合并到当前分支：</p>
<pre>git merge</pre>
<p>该命令就是在执行 git fetch 之后紧接着执行 git merge 远程分支到你所在的任意分支。</p>
<p>
假设你配置好了一个远程仓库，并且你想要提取更新的数据，你可以首先执行 <strong>git fetch [alias]</strong>
 告诉 Git 去获取它有你没有的数据，然后你可以执行 <strong>git merge [alias]/[branch]</strong> 以将服务器上的任何更新（假设有人这时候推送到服务器了）合并到你的当前分支。
</p>
<p>接下来我们在 Github 上点击" README.md" 并在线修改它:
</p>
<p><img src="/wp-content/uploads/2015/03/C5A6670F-202D-4F2C-8A63-07CEA37BB67A.jpg"></p>
<p>然后我们在本地更新修改。</p>
<pre>
$ git fetch origin
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From github.com:tianqixin/runoob-git-test
   0205aab..febd8ed  master     -&gt; origin/master
</pre>
<p>以上信息"0205aab..febd8ed  master     -> origin/master" 说明 master 分支已被更新，我们可以使用以下命令将更新同步到本地：</p>
<pre>
$ git merge origin/master
Updating 0205aab..febd8ed
Fast-forward
 README.md | 1 +
 1 file changed, 1 insertion(+)
</pre>
<p>查看  README.md  文件内容：</p>
<pre>
$ cat README.md 
# 菜鸟教程 Git 测试
## 第一次修改内容
</pre>
<hr>
<h2>推送到远程仓库</h2>
<p>推送你的新分支与数据到某个远端仓库命令:</p>
<pre>
git push [alias] [branch]
</pre>
<p>以上命令将你的 [branch] 分支推送成为 [alias] 远程仓库上的 [branch] 分支，实例如下。</p>
<pre>
$ touch runoob-test.txt      # 添加文件
$ git add runoob-test.txt 
$ git commit -m "添加到远程"
master 69e702d] 添加到远程
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 runoob-test.txt

$ git push origin master    # 推送到 Github
</pre>
<p>重新回到我们的 Github 仓库，可以看到文件以及提交上来了：</p>

<p><img src="/wp-content/uploads/2015/03/C5A6670F-202D-4F2C-8A63-07CEA37BB67A-1.jpg"></p>
<hr>
<h2>删除远程仓库</h2>
<p>删除远程仓库你可以使用命令：</p>
<pre>git remote rm [别名]</pre>
<h3>实例</h3>
<pre>
$ git remote -v
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (fetch)
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (push)

# 添加仓库 origin2
$ git remote add origin2 git@github.com:tianqixin/runoob-git-test.git

$ git remote -v
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (fetch)
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (push)
origin2&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (fetch)
origin2&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (push)

# 删除仓库 origin2
$ git remote rm origin2
$ git remote -v
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (fetch)
origin&nbsp;&nbsp;&nbsp;&nbsp;git@github.com:tianqixin/runoob-git-test.git (push)
</pre>
<!--
<div style="display:none;">
<hr>
<h2 id="git-coding">使用 CODING 仓库</h2>

<blockquote><p>对于开发者而言 GitHub 已经不陌生了，在平时的开发中将代码托管到 GitHub 上十分方便。但是、国内用户通常会遇到一个问题就是： GitHub 的访问速度太慢。在阿里云和腾讯云的主机上 clone 代码时，如果主机的带宽不够大，clone 代码简直就是龟速。常常还会出现：丢包、失去连接等情况。对于这种情况，如果你想体验飞速的 Git 服务，不妨试着用一下 <a href='https://studio.dev.tencent.com/' target="_blank" rel="noopener noreferrer">腾讯云开发者平台</a>。相对于GitHub，CODING 除了提供免费的 Git 仓库之外，还给我们提供了免费的私有仓库（免费的普通会员提供 10 个私有项目、512M Git 仓库容量）。此外、CODING 还为我们免费提供了，项目管理、任务管理、团队管理、文件管理等功能，十分强大。</p></blockquote>
<p>下面，我是试着来创建一个 CODING 项目，并且将 GitHub 上的代码迁移到 CODING。通常，分为三步：</p>
<ul><li>1、创建 CODING 项目</li><li>2、将 GitHub 代码 Pull 到本地</li><li>3、本地关联 CODING 仓库，Push 代码到 CODING</li></ul><h3>创建 CODING 项目：</h3>
<p>登录 <a href='https://studio.dev.tencent.com/' target="_blank" rel="noopener noreferrer">腾讯云开发者平台</a> 注册账号，然后在项目管理页面中创建项目，这一步不做赘述，按你的需要填写项目名称与描述，选择 License 类型即可，关于 License 的选择可以参考这篇文章：<a target="_blank" href='http://www.ruanyifeng.com/blog/2011/05/how_to_choose_free_software_licenses.html' rel="noopener noreferrer">如何选择开源许可证？</a>。项目创建完成中，在右侧菜单栏中的代码选项卡可以对代码进行相关的管理与操作</p><p>
<img src='//static.runoob.com/images/ad/86879978.jpg' alt='' /></p><p>
<img src='//static.runoob.com/images/ad/84518452.jpg' alt='' /></p>
<h3>将 GitHub 代码 Pull 到本地：</h3>
<p>登录 GitHub 选择你想要导入的仓库并复制仓库地址，在本地执行命令，将 GitHub 仓库代码拉下来：</p><p>
<img src='//static.runoob.com/images/ad/10346579.jpg' alt='' /></p>

<pre>sudo git clone</pre>
<h3>本地关联 CODING 仓库，Push 代码到 CODING：</h3><p>首先我们执行命令：<code>git remote -v</code></p><p>
<img src='//static.runoob.com/images/ad/43989293.jpg' alt='' /></p><p>
可以看到，当前的 git 已经关联了一个远程仓库。</p><p>
因此，接下来我们执行以下命令，来关联 CODING 远程仓库（后面的仓库地址需要替换为你的 CODING 项目的地址！）
第一条命令的作用是删除现有的仓库关联，后面两条命令则是将仓库关联到 CODING 的地址，并且将代码 Push 到 master 分支</p><pre>
sudo git remote rm origin
sudo git remote add origin https://git.coding.net/xxx/xxx.git
sudo git push -u origin master</pre>
<p>之后，我们再次进入 CODING 项目中代码管理的页面，便可以看到我们刚才 Push 上去的代码了。至此、GitHub 上的项目已经完整迁移到了 CODING 平台！</p><p>
<img src='//static.runoob.com/images/ad/18357223.jpg' alt='' /></p>
<h3>CODING 仓库的免密码 Push/Pull</h4><p>代码迁移到 CODING 之后，我们发现，每次 Push/Pull 代码的时候都会提示我们输入用户名和密码。这是因为，我们的项目还没有添加 SSH Key，只能通过用户名/密码验证。
而 CODING 是为我们提供了公钥验证的方式的，进入项目管理，在左侧选项卡中点击"公钥部署"按钮，然后点击右侧的"新建公钥部署"</p><p>
<img src='//static.runoob.com/images/ad/62119861.jpg' alt='' /></p><p>我们将本地的公钥内容粘贴到对应位置，并且给公钥命名一下（查看/生成本机公钥，可以参考这篇博文：<a href='//www.runoob.com/w3cnote/view-ssh-public-key.html' target="_blank" rel="noopener noreferrer">查看本机 ssh 公钥，生成公钥</a>）。勾选"授予推送权限"则可以授予这台机器Push代码的权限。</p><p>
<img src='//static.runoob.com/images/ad/64498917.jpg' alt='' /></p><p>保存好设置后，我们再次尝试。此时，Push/Pull 代码不在需要验证用户名密码。至此，我们的代码便完全托管在了 CODING 平台上，享受他的便捷与飞速吧！</p><p>如有疑问请查阅<a href='https://dev.tencent.com/help/doc/cloud-studio' target="_blank" rel="noopener noreferrer">帮助文档</a></p>
<p>现在 CODING 正在举办一场基于 Cloud Studio 工作空间的【我最喜爱的 Cloud Studio 插件评选大赛】。进入活动官网：<a href="https://studio.qcloud.coding.net/campaign/favorite-plugins/index" rel="noopener noreferrer" target="_blank">https://studio.qcloud.coding.net/campaign/favorite-plugins/index</a>，了解更多活动信息。</p>
</div>-->			<!-- 其他扩展 -->
						
			</div>
			
		</div>
		
		<div class="previous-next-links">
			<div class="previous-design-link"><i style="font-size:16px;" class="fa fa-arrow-left" aria-hidden="true"></i> <a href="http://www.runoob.com/git/git-tag.html" rel="prev"> Git 标签</a> </div>
			<div class="next-design-link"><a href="http://www.runoob.com/git/git-server.html" rel="next"> Git 服务器搭建</a> <i style="font-size:16px;" class="fa fa-arrow-right" aria-hidden="true"></i></div>
		</div>
		<!-- 笔记列表 -->
		<style>
.wrapper {
  /*text-transform: uppercase; */
  background: #ececec;
  color: #555;
  cursor: help;
  font-family: "Gill Sans", Impact, sans-serif;
  font-size: 20px;
  position: relative;
  text-align: center;
  width: 200px;
  -webkit-transform: translateZ(0); /* webkit flicker fix */
  -webkit-font-smoothing: antialiased; /* webkit text rendering fix */
}

.wrapper .tooltip {
  white-space: nowrap;
  font-size: 14px;
  text-align: left;
  background: #96b97d;
  bottom: 100%;
  color: #fff;
  display: block;
  left: -25px;
  margin-bottom: 15px;
  opacity: 0;
  padding: 14px;
  pointer-events: none;
  position: absolute;
  
  -webkit-transform: translateY(10px);
     -moz-transform: translateY(10px);
      -ms-transform: translateY(10px);
       -o-transform: translateY(10px);
          transform: translateY(10px);
  -webkit-transition: all .25s ease-out;
     -moz-transition: all .25s ease-out;
      -ms-transition: all .25s ease-out;
       -o-transition: all .25s ease-out;
          transition: all .25s ease-out;
  -webkit-box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.28);
     -moz-box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.28);
      -ms-box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.28);
       -o-box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.28);
          box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.28);
}
.tooltip a {
	color:#fff;
}
/* This bridges the gap so you can mouse into the tooltip without it disappearing */
.wrapper .tooltip:before {
  bottom: -20px;
  content: " ";
  display: block;
  height: 20px;
  left: 0;
  position: absolute;
  width: 100%;
}  

/* CSS Triangles - see Trevor's post */
.wrapper .tooltip:after {
  border-left: solid transparent 10px;
  border-right: solid transparent 10px;
  border-top: solid #96b97d 10px;
  bottom: -10px;
  content: " ";
  height: 0;
  left: 20%;
  margin-left: -13px;
  position: absolute;
  width: 0;
}
.wrapper .tooltip1 {
	margin-left: 50px;
	padding-top: 0px;
}
/*
.wrapper:hover .tooltip {
  opacity: 1;
  pointer-events: auto;
  -webkit-transform: translateY(0px);
     -moz-transform: translateY(0px);
      -ms-transform: translateY(0px);
       -o-transform: translateY(0px);
          transform: translateY(0px);
}
*/
/* IE can just show/hide with no transition */
.lte8 .wrapper .tooltip {
  display: none;
}

.lte8 .wrapper:hover .tooltip {
  display: block;
}

</style>

<div class="title" id="comments">
	<h2 class="">
    <div class="altblock">
		    	<i style="font-size:28px;margin-top: 8px;" class="fa fa-pencil-square-o" aria-hidden="true"></i>
    	    </div>
    <span class="mw-headline" id="qa_headline">1  篇笔记</span>
	<span class="mw-headline" id="user_add_note" style="float:right;line-height: 62px;padding-right: 14px;"><i class="fa fa-pencil-square-o" aria-hidden="true"></i>  写笔记</span>
    </h2>
</div>

<div id="postcomments"   >
	<ol class="commentlist">
		<li class="comment even thread-even depth-1" id="comment-46547"><span class="comt-f">#1</span><div class="comt-avatar wrapper"><i style="font-size:36px;" class="fa fa-user-circle" aria-hidden="true"></i><div class="tooltip"><p><i class="fa fa-user" aria-hidden="true"></i>&nbsp;&nbsp;&nbsp;leon</p><p><i class="fa fa-envelope" aria-hidden="true"></i>&nbsp;&nbsp;105***6491@qq.co</p><p><i class="fa fa-external-link" aria-hidden="true"></i> <a rel="nofollow" target="_blank" href="https://blog.twofei.com/695/">&nbsp;&nbsp;参考地址</a></p></div><div id="runoobvote-id-46547" data-commid = "46547" class="upvotejs"><a class="upvote"></a> <span class="count">18</span></div></div><div class="comt-main" id="div-comment-46547"><ul><li>执行&nbsp;<code>git fetch origin master</code>&nbsp;时，它的意思是从名为&nbsp;<strong>origin</strong>&nbsp;的远程上拉取名为&nbsp;<strong>master</strong>&nbsp;的分支到本地分支&nbsp;<strong>origin/master</strong>&nbsp;中。既然是拉取代码，当然需要同时指定远程名与分支名，所以分开写。</li><li>执行&nbsp;<code>git merge origin/master</code>&nbsp;时，它的意思是合并名为&nbsp;<strong>origin/master</strong>&nbsp;的分支到当前所在分支。既然是分支的合并，当然就与远程名没有直接的关系，所以没有出现远程名。需要指定的是被合并的分支。</li><li>执行&nbsp;<code>git push origin master</code>&nbsp;时，它的意思是推送本地的&nbsp;<strong>master</strong>&nbsp;分支到远程&nbsp;<strong>origin</strong>，涉及到远程以及分支，当然也得分开写了。</li><li>还可以一次性拉取多个分支的代码：<code>git fetch origin master stable oldstable</code>；</li><li>也还可以一次性合并多个分支的代码：<code>git merge origin/master hotfix-2275 hotfix-2276 hotfix-2290</code>；</li></ul><div class="comt-meta wrapper"><span class="comt-author"><a target="_blank" href="javascript:;">leon</a><div class="tooltip tooltip1"><p><i class="fa fa-user" aria-hidden="true"></i>&nbsp;&nbsp;&nbsp;leon</p><p><i class="fa fa-envelope" aria-hidden="true"></i>&nbsp;&nbsp;105***6491@qq.co</p><p><i class="fa fa-external-link" aria-hidden="true"></i> <a rel="nofollow" target="_blank" href="https://blog.twofei.com/695/">&nbsp;&nbsp;参考地址</a></p></div></span>4个月前 (09-08)</div></div></li><!-- #comment-## -->
	</ol>
	<div class="pagenav">
			</div>
</div>
<div id="respond" class="no_webshot"> 
		<div class="comment-signarea" style="display:none; padding: 20px 20px;"> 
	<h3 class="text-muted" id="share_code" style="color: #799961;"><i class="fa fa-pencil-square-o" aria-hidden="true"></i> 点我分享笔记</h3>
	<!--
	<p style="font-size:14px;">笔记需要是本篇文章的内容扩展！</p><br>
	<p style="font-size:12px;"><a href="//www.runoob.com/tougao" target="_blank">文章投稿，可点击这里</a></p>
	<p style="font-size:14px;"><a href="/w3cnote/runoob-user-test-intro.html#invite" target="_blank">注册邀请码获取方式</a></p>
		<h3 class="text-muted"><i class="fa fa-info-circle" aria-hidden="true"></i> 分享笔记前必须<a href="javascript:;" class="runoob-pop">登录</a>！</h3>
		<p><a href="/w3cnote/runoob-user-test-intro.html#invite" target="_blank">注册邀请码获取方式</a></p>-->
	</div>
		
	<form action="/wp-content/themes/runoob/option/addnote.php" method="post" id="commentform" style="display:none;">
		<div class="comt">
			<div class="comt-title">
				<i style="font-size:36px;" class="fa fa-user-circle" aria-hidden="true"></i>				<p><a id="cancel-comment-reply-link" href="javascript:;">取消</a></p>
			</div>
			<div class="comt-box">
			<div id="mded"></div>
			
				<div class="comt-ctrl">
					<div class="comt-tips"><input type='hidden' name='comment_post_ID' value='11431' id='comment_post_ID' />
<input type='hidden' name='comment_parent' id='comment_parent' value='0' />
</div>
					<button type="submit" name="submit" id="submit" tabindex="5"><i class="fa fa-pencil" aria-hidden="true"></i> 分享笔记</button>
				</div>
			</div>
		
				
					<div class="comt-comterinfo"> 
						<ul id="comment-author-info">
							<li class="form-inline"><label class="hide" for="author">昵称</label><input class="ipt" type="text" name="author" id="author" value="" tabindex="2" placeholder="昵称"><span class="text-muted">昵称 (必填)</span></li>
							<li class="form-inline"><label class="hide" for="email">邮箱</label><input class="ipt" type="text" name="email" id="email" value="" tabindex="3" placeholder="邮箱"><span class="text-muted">邮箱 (必填)</span></li>
							<li class="form-inline"><label class="hide" for="url">引用地址</label><input class="ipt" type="text" name="url" id="url" value="" tabindex="4" placeholder="引用地址"><span class="text-muted">引用地址</span></li>
						</ul>
					</div>
				
			
		</div>

	</form>
	</div>
<script type="text/javascript">
$(function() {
	//初始化编辑器
	
	var editor = new Simditor({
	  textarea: $('#mded'),
	  placeholder: '写笔记...',
	  upload:false,
	 // upload: {url:'/api/comment_upload_file.php',params: null,fileKey: 'upload_file',connectionCount: 1,leaveConfirm: '文件正在上传，您确定离开?'},
	  defaultImage: 'http://www.runoob.com/images/logo.png',
	  codeLanguages: '',
	  autosave: 'editor-content',
	  toolbar: [  'bold','code','ul','ol','image' ]
	});
	editor.on('selectionchanged', function() {
		$(".code-popover").hide();
	});

	// 提交数据
	$("#share_code").click(function() {
		$(".comment-signarea").hide();
		$("#commentform").show();
		
	});
	$("#user_add_note").click(function() {
		$(".comment-signarea").hide();
		$("#commentform").show();
		$('html, body').animate({
       	    scrollTop: $("#respond").offset().top
    	}, 200);
	});

	// 提交笔记
	var commentform=$('#commentform');
	commentform.prepend('<div id="comment-status" style="display:none;" ></div>');
	var statusdiv=$('#comment-status');
	
	commentform.submit(function(e){
		e.preventDefault();
		var noteContent = editor.getValue();
		// console.log(noteContent);
		noteContent = noteContent.replace(/<pre><code>/g,"<pre>");
		noteContent = noteContent.replace(/<\/code><\/pre>/g,"</pre>");
		
		// 系列化表单数据
		var comment_parent = 0;
		var is_user_logged_in = $("#is_user_logged_in").val();
		var comment_post_ID =  11431;
		var _wp_unfiltered_html_comment = $("#_wp_unfiltered_html_comment").val();
		var comment = noteContent;
		var author = $("#author").val();
		var url = $("#url").val();
		var email = $("#email").val();
		if(isBlank(author) && is_user_logged_in==0) {
			statusdiv.html('<p  class="ajax-error">请输入昵称！</p>').show();
		} else if(isBlank(email)  && is_user_logged_in==0) {
			statusdiv.html('<p  class="ajax-error">请输入邮箱！</p>').show();
		} else {
			// var formdata=commentform.serialize() + "&comment=" + noteContent ;
			// 添加状态信息
			statusdiv.html('<p>Processing...</p>').show();
			// 获取表单提交地址
			var formurl=commentform.attr('action');
			
			// 异步提交
			$.ajax({
					type: 'post',
					url: formurl,
					dataType:'json',
					data: {"comment_parent":comment_parent,"comment_post_ID":comment_post_ID, "_wp_unfiltered_html_comment":_wp_unfiltered_html_comment,"comment":comment,"url":url, "email":email,"author":author},
					error: function(XMLHttpRequest, textStatus, errorThrown){
					statusdiv.html('<p class="ajax-error" >数据不完整或表单提交太快了！</p>').show();
				},
				success: function(data, textStatus){
					if(data.errorno=="0") {
						$("#submit").prop('disabled', true);
						statusdiv.html('<p class="ajax-success" >笔记已提交审核，感谢分享笔记！</p>').show();
						alert('笔记已提交审核，感谢分享笔记！');
					}else{
						statusdiv.html('<p class="ajax-error" >'+data.msg+'</p>').show();
					}
					commentform.find('textarea[name=comment]').val('');
				}
			});
			setTimeout(function(){
		        $("#submit").prop('disabled', false);
		    }, 10*1000);
		}
		return false;

	});
	$(".comt-author").click(function() {
		href = $(this).children("a").attr("href");
		if(href.indexOf("/note/")!=-1) {
			var win = window.open(href, '_blank');
  			win.focus();
		}
	});
	$(".comt-author").hover(function(){
		$(this).children(".tooltip").css({ "opacity": 1, "pointer-events": "auto"});
	},function(){
		$(this).children(".tooltip").css({ "opacity": 0, "pointer-events": "auto"});
	});
	$(".wrapper i").hover(function(){
		$(this).siblings(".tooltip").css({ "opacity": 1, "pointer-events": "auto"});
	},function(){
		$(this).siblings(".tooltip").css({ "opacity": 0, "pointer-events": "auto"});
	});
	//Upvote.create('runoobvote-id', {callback: vote_callback});
	var ajaxurl = 'https://www.runoob.com/wp-admin/admin-ajax.php';
	var callback = function(data) {
		//console.log($('#runoobvote-id').upvote('upvoted'));
		//console.log($('#runoobvote-id').upvote('downvoted'));
		//console.log(data);
		_vote_action = data.action;
		console.log(_vote_action);
		id_arr = data.id.split('-');
		um_id= id_arr[2];
		//console.log(um_id);
		
		var re = /^[1-9]+/;
		if (re.test(um_id)) { 
			var ajax_data = {
				_vote_action: _vote_action,
				action: "pinglun_zan",
				um_id: um_id,
				um_action: "ding"
			};
			//console.log(ajax_data);
			$.post(ajaxurl,ajax_data,function(status){
				//console.log("Data: " + data + "nStatus: " + status);
			});
		}
	};
	if($('#comments').length){
		$('.upvotejs').upvote({id: 11431, callback: callback});
		
		$.post(ajaxurl,{"action":"pinglun_zan","postid":11431},function(data){  
			$(data).each(function(key,value) {
				$("#runoobvote-id-" + value.commid + " .upvote").addClass(value.upvotejs_class);
				$("#runoobvote-id-" + value.commid + " .downvote").addClass(value.downvote_class);
				$("#runoobvote-id-" + value.commid + " .count").addClass(value.upvote_count)
			})
		},'json');
	}
	
	
});
function isBlank(str) {
    return (!str || /^\s*$/.test(str));
}


</script>

<link rel="stylesheet" href="https://static.runoob.com/assets/upvotejs/dist/upvotejs/upvotejs.css">
<script src="https://static.runoob.com/assets/upvotejs/dist/upvotejs/upvotejs.vanilla.js"></script>
<script src="https://static.runoob.com/assets/upvotejs/dist/upvotejs/upvotejs.jquery.js"></script>
<link rel="stylesheet" href="/wp-content/themes/runoob/assets/css/qa.css?1.43">
<link rel="stylesheet" type="text/css" href="https://static.runoob.com/assets/simditor/2.3.6/styles/simditor.css" />
<script type="text/javascript" src="https://static.runoob.com/assets/simditor/2.3.6/scripts/module.js"></script>
<script type="text/javascript" src="//static.runoob.com/assets/simditor/2.3.6/scripts/hotkeys.js"></script>
<script type="text/javascript" src="//static.runoob.com/assets/simditor/2.3.6/scripts/uploader.js"></script>
<script type="text/javascript" src="https://static.runoob.com/assets/simditor/2.3.6/scripts/simditor.min.js"></script>
<script type="text/javascript" src="https://static.runoob.com/assets/simditor/2.3.6/scripts/simditor-autosave.js"></script>
		<div class="sidebar-box ">
				</div>
		
	</div>
</div>
	

<!-- 右边栏 -->
<div class="fivecol last right-column">
<!--
	<div class="tab tab-light-blue" style="text-align: center;">关注微信</div>
	<div class="sidebar-box">
		<a href="http://m.runoob.com/" target="_blank"> <img src="http://www.runoob.com/wp-content/themes/w3cschool.cc/assets/img/qrcode.jpg" alt="移动版"> </a>
		<div class="qqinfo">
		 <a target="_blank" href="http://jq.qq.com/?_wv=1027&k=dOwwKN" id="qqhref">
		<img border="0" src="http://pub.idqqimg.com/wpa/images/group.png" alt="菜鸟家族" title="菜鸟家族"></a>
		<span>(群号：<span id="qqid">365967760</span>)</span>
		</div>
		
	</div>
	-->
<style>
.sidebar-tree .double-li {
	width:300px;
}
.sidebar-tree .double-li li {
    width: 44%;
    line-height: 1.5em;
    border-bottom: 1px solid #ccc;
    float: left;
    display: inline;
}
</style>

	
		<div class="sidebar-box re-box re-box-large">
		<div class="sidebar-box recommend-here" style="margin: 0 auto;">
			<a href="javascript:void(0);" style="font-size: 16px; color:#64854c;font-weight:bold;"> <i class="fa fa-list" aria-hidden="true"></i> 分类导航</a>
		</div>
	<div class="sidebar-box sidebar-cate">
		
		<div class="sidebar-tree" >
			<ul><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> HTML / CSS</a><ul class="double-li"><li><a title="HTML 教程" href="//www.runoob.com/html/html-tutorial.html">HTML 教程</a></li><li><a title="HTML5 教程" href="//www.runoob.com/html/html5-intro.html">HTML5 教程</a></li><li><a title="CSS 教程" href="//www.runoob.com/css/css-tutorial.html">CSS 教程</a></li><li><a title="CSS3 教程" href="//www.runoob.com/css3/css3-tutorial.html">CSS3 教程</a></li><li><a title="Bootstrap3 教程" href="//www.runoob.com/bootstrap/bootstrap-tutorial.html">Bootstrap3 教程</a></li><li><a title="Bootstrap4 教程" href="//www.runoob.com/bootstrap4/bootstrap4-tutorial.html">Bootstrap4 教程</a></li><li><a title="Font Awesome 教程" href="//www.runoob.com/font-awesome/fontawesome-tutorial.html">Font Awesome 教程</a></li><li><a title="Foundation 教程" href="//www.runoob.com/foundation/foundation-tutorial.html">Foundation 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> JavaScript</a><ul class="double-li"><li><a title="JavaScript 教程" href="//www.runoob.com/js/js-tutorial.html">JavaScript 教程</a></li><li><a title="HTML DOM 教程" href="//www.runoob.com/htmldom/htmldom-tutorial.html">HTML DOM 教程</a></li><li><a title="jQuery 教程" href="//www.runoob.com/jquery/jquery-tutorial.html">jQuery 教程</a></li><li><a title="AngularJS 教程" href="//www.runoob.com/angularjs/angularjs-tutorial.html">AngularJS 教程</a></li><li><a title="AngularJS2 教程" href="//www.runoob.com/angularjs2/angularjs2-tutorial.html">AngularJS2 教程</a></li><li><a title="Vue.js 教程" href="//www.runoob.com/vue2/vue-tutorial.html">Vue.js 教程</a></li><li><a title="React 教程" href="//www.runoob.com/react/react-tutorial.html">React 教程</a></li><li><a title="TypeScript 教程" href="//www.runoob.com/typescript/ts-tutorial.html">TypeScript 教程</a></li><li><a title="jQuery UI 教程" href="//www.runoob.com/jqueryui/jqueryui-tutorial.html">jQuery UI 教程</a></li><li><a title="jQuery EasyUI 教程" href="//www.runoob.com/jeasyui/jqueryeasyui-tutorial.html">jQuery EasyUI 教程</a></li><li><a title="Node.js 教程" href="//www.runoob.com/nodejs/nodejs-tutorial.html">Node.js 教程</a></li><li><a title="AJAX 教程" href="//www.runoob.com/ajax/ajax-tutorial.html">AJAX 教程</a></li><li><a title="JSON 教程" href="//www.runoob.com/json/json-tutorial.html">JSON 教程</a></li><li><a title="Echarts 教程" href="//www.runoob.com/echarts/echarts-tutorial.html">Echarts 教程</a></li><li><a title="Highcharts 教程" href="//www.runoob.com/highcharts/highcharts-tutorial.html">Highcharts 教程</a></li><li><a title="Google 地图 教程" href="//www.runoob.com/googleapi/google-maps-basic.html">Google 地图 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> 服务端</a><ul class="double-li"><li><a title="Python 教程" href="//www.runoob.com/python3/python3-tutorial.html">Python 教程</a></li><li><a title="Python2.x 教程" href="//www.runoob.com/python/python-tutorial.html">Python2.x 教程</a></li><li><a title="Linux 教程" href="//www.runoob.com/linux/linux-tutorial.html">Linux 教程</a></li><li><a title="Docker 教程" href="//www.runoob.com/docker/docker-tutorial.html">Docker 教程</a></li><li><a title="Ruby 教程" href="//www.runoob.com/ruby/ruby-tutorial.html">Ruby 教程</a></li><li><a title="Java 教程" href="//www.runoob.com/java/java-tutorial.html">Java 教程</a></li><li><a title="C 教程" href="//www.runoob.com/c/c-tutorial.html">C 教程</a></li><li><a title="C++ 教程" href="//www.runoob.com/cplusplus/cpp-tutorial.html">C++ 教程</a></li><li><a title="Perl 教程" href="//www.runoob.com/perl/perl-tutorial.html">Perl 教程</a></li><li><a title="Servlet 教程" href="//www.runoob.com/servlet/servlet-tutorial.html">Servlet 教程</a></li><li><a title="JSP 教程" href="//www.runoob.com/jsp/jsp-tutorial.html">JSP 教程</a></li><li><a title="Lua 教程" href="//www.runoob.com/lua/lua-tutorial.html">Lua 教程</a></li><li><a title="Scala 教程" href="//www.runoob.com/scala/scala-tutorial.html">Scala 教程</a></li><li><a title="Go 教程" href="//www.runoob.com/go/go-tutorial.html">Go 教程</a></li><li><a title="PHP 教程" href="//www.runoob.com/php/php-tutorial.html">PHP 教程</a></li><li><a title="Django 教程" href="//www.runoob.com/django/django-tutorial.html">Django 教程</a></li><li><a title="设计模式" href="//www.runoob.com/design-pattern/design-pattern-tutorial.html">设计模式</a></li><li><a title="正则表达式" href="//www.runoob.com/regexp/regexp-tutorial.html">正则表达式</a></li><li><a title="Maven 教程" href="//www.runoob.com/maven/maven-tutorial.html">Maven 教程</a></li><li><a title="NumPy 教程" href="//www.runoob.com/numpy/numpy-tutorial.html">NumPy 教程</a></li><li><a title="ASP 教程" href="//www.runoob.com/asp/asp-tutorial.html">ASP 教程</a></li><li><a title="AppML 教程" href="//www.runoob.com/appml/appml-tutorial.html">AppML 教程</a></li><li><a title="VBScript 教程" href="//www.runoob.com/vbscript/vbscript-tutorial.html">VBScript 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> 数据库</a><ul class="double-li"><li><a title="SQL 教程" href="//www.runoob.com/sql/sql-tutorial.html">SQL 教程</a></li><li><a title="Mysql 教程" href="//www.runoob.com/mysql/mysql-tutorial.html">Mysql 教程</a></li><li><a title="PostgreSQL 教程" href="//www.runoob.com/postgresql/postgresql-tutorial.html">PostgreSQL 教程</a></li><li><a title="SQLite 教程" href="//www.runoob.com/sqlite/sqlite-tutorial.html">SQLite 教程</a></li><li><a title="MongoDB 教程" href="//www.runoob.com/mongodb/mongodb-tutorial.html">MongoDB 教程</a></li><li><a title="Redis 教程" href="//www.runoob.com/redis/redis-tutorial.html">Redis 教程</a></li><li><a title="Memcached 教程" href="//www.runoob.com/Memcached/Memcached-tutorial.html">Memcached 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> 移动端</a><ul class="double-li"><li><a title="Android 教程" href="//www.runoob.com/w3cnote/android-tutorial-intro.html">Android 教程</a></li><li><a title="Swift 教程" href="//www.runoob.com/swift/swift-tutorial.html">Swift 教程</a></li><li><a title="jQuery Mobile 教程" href="//www.runoob.com/jquerymobile/jquerymobile-tutorial.html">jQuery Mobile 教程</a></li><li><a title="ionic 教程" href="//www.runoob.com/ionic/ionic-tutorial.html">ionic 教程</a></li><li><a title="Kotlin 教程" href="//www.runoob.com/kotlin/kotlin-tutorial.html">Kotlin 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> XML 教程</a><ul class="double-li"><li><a title="XML 教程" href="//www.runoob.com/xml/xml-tutorial.html">XML 教程</a></li><li><a title="DTD 教程" href="//www.runoob.com/dtd/dtd-tutorial.html">DTD 教程</a></li><li><a title="XML DOM 教程" href="//www.runoob.com/dom/dom-tutorial.html">XML DOM 教程</a></li><li><a title="XSLT 教程" href="//www.runoob.com/xsl/xsl-tutorial.html">XSLT 教程</a></li><li><a title="XPath 教程" href="//www.runoob.com/xpath/xpath-tutorial.html">XPath 教程</a></li><li><a title="XQuery 教程" href="//www.runoob.com/xquery/xquery-tutorial.html">XQuery 教程</a></li><li><a title="XLink 教程" href="//www.runoob.com/xlink/xlink-tutorial.html">XLink 教程</a></li><li><a title="XPointer 教程" href="//www.runoob.com/xlink/xlink-tutorial.html">XPointer 教程</a></li><li><a title="XML Schema 教程" href="//www.runoob.com/schema/schema-tutorial.html">XML Schema 教程</a></li><li><a title="XSL-FO 教程" href="//www.runoob.com/xslfo/xslfo-tutorial.html">XSL-FO 教程</a></li><li><a title="SVG 教程" href="//www.runoob.com/svg/svg-tutorial.html">SVG 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> ASP.NET</a><ul class="double-li"><li><a title="ASP.NET 教程" href="//www.runoob.com/aspnet/aspnet-tutorial.html">ASP.NET 教程</a></li><li><a title="C# 教程" href="//www.runoob.com/csharp/csharp-tutorial.html">C# 教程</a></li><li><a title="Web Pages 教程" href="//www.runoob.com/aspnet/webpages-intro.html">Web Pages 教程</a></li><li><a title="Razor 教程" href="//www.runoob.com/aspnet/razor-intro.html">Razor 教程</a></li><li><a title="MVC 教程" href="//www.runoob.com/aspnet/mvc-intro.html">MVC 教程</a></li><li><a title="Web Forms 教程" href="//www.runoob.com/aspnet/aspnet-intro.html">Web Forms 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> Web Service</a><ul class="double-li"><li><a title="Web Service 教程" href="//www.runoob.com/webservices/webservices-tutorial.html">Web Service 教程</a></li><li><a title="WSDL 教程" href="//www.runoob.com/wsdl/wsdl-tutorial.html">WSDL 教程</a></li><li><a title="SOAP 教程" href="//www.runoob.com/soap/soap-tutorial.html">SOAP 教程</a></li><li><a title="RSS 教程" href="//www.runoob.com/rss/rss-tutorial.html">RSS 教程</a></li><li><a title="RDF 教程" href="//www.runoob.com/rdf/rdf-tutorial.html">RDF 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> 开发工具</a><ul class="double-li"><li><a title="Eclipse 教程" href="//www.runoob.com/eclipse/eclipse-tutorial.html">Eclipse 教程</a></li><li><a title="Git 教程" href="//www.runoob.com/git/git-tutorial.html">Git 教程</a></li><li><a title="Svn 教程" href="//www.runoob.com/svn/svn-tutorial.html">Svn 教程</a></li><li><a title="Markdown 教程" href="//www.runoob.com/markdown/md-tutorial.html">Markdown 教程</a></li></ul></li><li style="margin: 0;"><a href="javascript:void(0);" class="tit"> 网站建设</a><ul class="double-li"><li><a title="HTTP 教程" href="//www.runoob.com/http/http-tutorial.html">HTTP 教程</a></li><li><a title="网站建设指南" href="//www.runoob.com/web/web-buildingprimer.html">网站建设指南</a></li><li><a title="浏览器信息" href="//www.runoob.com/browsers/browser-information.html">浏览器信息</a></li><li><a title="网站主机教程" href="//www.runoob.com/hosting/hosting-tutorial.html">网站主机教程</a></li><li><a title="TCP/IP 教程" href="//www.runoob.com/tcpip/tcpip-tutorial.html">TCP/IP 教程</a></li><li><a title="W3C 教程" href="//www.runoob.com/w3c/w3c-tutorial.html">W3C 教程</a></li><li><a title="网站品质" href="//www.runoob.com/quality/quality-tutorial.html">网站品质</a></li></ul></li></ul>			</div>
	
	</div>
	</div>
	<br>
	
	<div class="sidebar-box re-box re-box-large">
		<div class="sidebar-box recommend-here">
			<a href="javascript:void(0);">Advertisement</a>
		</div>
		<div class="re-600160" id="sidebar-right-re">
				<script async src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
		<!-- 侧栏1 -->
		<ins class="adsbygoogle"
		     style="display:inline-block;width:160px;height:600px"
		     data-ad-client="ca-pub-5751451760833794"
		     data-ad-slot="4106274865"></ins>
		<script>
		(adsbygoogle = window.adsbygoogle || []).push({});
		</script>
				</div>
	</div>
</div></div>

</div>

<script>
var aid = 11431;
function coll() {
	$.post( '/wp-content/themes/runoob/option/user/userinfo.php', {aid:aid, action:"collarticle", opt:'add'},function( data ) {
		if(data.error==0) {
			$("#content").find("h1:first").find("a").attr("href","javascript:void(0);");
			$("#content").find("h1:first").find("img").attr("src","http://www.runoob.com/wp-content/themes/runoob/assets/img/coll2.png").css({width:32+"px",height:32+"px"});
		}
		alert(data.msg);
	},'json');
}
</script>


<!-- 反馈对话框开始 -->
<script src="/wp-content/themes/runoob/assets/feedback/stable/2.0/feedback.js?1.0"></script>
<link rel="stylesheet" href="/wp-content/themes/runoob/assets/feedback/stable/2.0/feedback.css?1.0" />
<script type="text/javascript">
$.feedback({
    ajaxURL: '/feedback/runoob_feedback.php',
	html2canvasURL: '/wp-content/themes/runoob/assets/feedback/stable/2.0/html2canvas.js',
	onClose: function () {
         window.location.reload();
    }
});
</script>
<!-- 反馈对话框结束 -->
<button class="feedback-btn feedback-btn-gray">反馈/建议</button>
<!-- 底部 -->


<div id="footer" class="mar-t50">
   <div class="runoob-block">
    <div class="runoob cf">
     <dl>
      <dt>
       在线实例
      </dt>
      <dd>
       &middot;<a target="_blank" href="/html/html-examples.html">HTML 实例</a>
      </dd>
      <dd>
       &middot;<a target="_blank" href="/css/css-examples.html">CSS 实例</a>
      </dd>
      <dd>
       &middot;<a target="_blank" href="/js/js-examples.html">JavaScript 实例</a>
      </dd>
      <dd>
       &middot;<a target="_blank" href="/ajx/ajax-examples.html">Ajax 实例</a>
      </dd>
       <dd>
       &middot;<a target="_blank" href="/jquery/jquery-examples.html">jQuery 实例</a>
      </dd>
      <dd>
       &middot;<a target="_blank" href="/xml/xml-examples.html">XML 实例</a>
      </dd>
      <dd>
       &middot;<a target="_blank" href="/java/java-examples.html">Java 实例</a>
      </dd>
     
     </dl>
     <dl>
      <dt>
      字符集&工具
      </dt>
      <dd>
       &middot; <a target="_blank" href="/charsets/html-charsets.html">HTML 字符集设置</a>
      </dd>
      <dd>
       &middot; <a target="_blank" href="/tags/html-ascii.html">HTML ASCII 字符集</a>
      </dd>
     <dd>
       &middot; <a target="_blank" href="/tags/ref-entities.html">HTML ISO-8859-1</a>
      </dd> 
      <dd>
       &middot; <a target="_blank" href="/tags/html-symbols.html">HTML 实体符号</a>
      </dd>
      <dd>
       &middot; <a target="_blank" href="/tags/html-colorpicker.html">HTML 拾色器</a>
      </dd>
      <dd>
       &middot; <a target="_blank" href="//c.runoob.com/front-end/53">JSON 格式化工具</a>
      </dd>
     </dl>
     <dl>
      <dt>
       最新更新
      </dt>
                   <dd>
       &middot;
      <a href="http://www.runoob.com/json/json-vs-xml.html" title="JSON vs XML">JSON vs XML</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/sql/sql-exists.html" title="SQL EXISTS 运算符">SQL EXISTS 运算符</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/tags/tag-main.html" title="HTML main 标签">HTML main 标签</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/echarts/echarts-sunburst.html" title="ECharts 旭日图">ECharts 旭日图</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/echarts/echarts-events.html" title="ECharts 事件处理">ECharts 事件处理</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/echarts/echarts-visualmap.html" title="ECharts 数据的视觉映射">ECharts 数据的...</a>
      </dd>
              <dd>
       &middot;
      <a href="http://www.runoob.com/echarts/echarts-mediaqueries.html" title="ECharts 响应式">ECharts 响应式</a>
      </dd>
             </dl>
     <dl>
      <dt>
       站点信息
      </dt>
      <dd>
       &middot;
       <a target="_blank" href="//mail.qq.com/cgi-bin/qm_share?t=qm_mailme&amp;email=ssbDyoOAgfLU3crf09venNHd3w" rel="external nofollow">意见反馈</a>
      </dd>
        
      <dd>
       &middot;
      <a class="wxpopup" onclick="popFunction()">合作联系
       <span class="popuptext" id="myPopup">微信(注明来意)：<strong>centos5</strong></span>
      </a>
      </dd> 
      <dd>
       &middot;
      <a target="_blank" href="/disclaimer">免责声明</a>
       </dd>
       <!--
       <dd style="display: block;">
       &middot;
      <a href="javascript:void(0)" onclick="dashangToggle()" style="font-weight:bold;color:#f00;" title="打赏，支持一下">打赏一下</a>
       </dd>
     -->
      <dd>
       &middot;
       <a target="_blank" href="/aboutus">关于我们</a>
       </dd>
      <dd>
       &middot;
      <a target="_blank" href="/archives">文章归档</a>
      </dd>
    
     </dl>
    
     <div class="search-share">
      <div class="app-download">
        <div>
         <strong>关注微信</strong>
        </div>
      </div>
      <div class="share">
            <img width="128" height="128" src="/wp-content/themes/runoob/assets/images/qrcode.png" />
       </div>
     </div>
     
    </div>
   </div>
   <div class="w-1000 copyright">
     Copyright &copy; 2013-2020    <strong><a href="//www.runoob.com/" target="_blank">菜鸟教程</a></strong>&nbsp;
    <strong><a href="//www.runoob.com/" target="_blank">runoob.com</a></strong> All Rights Reserved. 备案号：闽ICP备15012807号-1
   </div>
  </div>
  <div class="fixed-btn">
    <a class="go-top" href="javascript:void(0)" title="返回顶部"> <i class="fa fa-angle-up"></i></a>
    <a class="qrcode"  href="javascript:void(0)" title="关注我们"><i class="fa fa-qrcode"></i></a>
    <a class="writer" style="display:none" href="javascript:void(0)"   title="标记/收藏"><i class="fa fa-star" aria-hidden="true"></i></a>
    <!-- qrcode modal -->
    <div id="bottom-qrcode" class="modal panel-modal hide fade in">
      <h4>微信关注</h4>
      <div class="panel-body"><img alt="微信关注" width="128" height="128" src="/wp-content/themes/runoob/assets/images/qrcode.png"></div> 
    </div>
  </div>

  <div class="hide_box"></div>
    <div class="shang_box">
      <a class="shang_close" href="javascript:void(0)" onclick="dashangToggle()" title="关闭"><img src="//static.runoob.com/images/dashang/close.jpg" alt="取消" /></a>
       
      <div class="shang_tit">
        <p>感谢您的支持，我会继续努力的!</p>
      </div>
      <div class="shang_payimg">
        <img src="//static.runoob.com/images/dashang/weipayimg.png" alt="扫码支持" title="扫一扫" />
      </div>
        <div class="pay_explain">扫码打赏，你说多少就多少</div>
      <div class="shang_payselect">
        <div class="pay_item  checked" data-id="weipay">
          <span class="radiobox"></span>
          <span class="pay_logo"><img src="//static.runoob.com/images/dashang/wechat.jpg" alt="微信" /></span>
        </div>
        <div class="pay_item" data-id="alipay">
          <span class="radiobox"></span>
          <span class="pay_logo"><img src="//static.runoob.com/images/dashang/alipay.jpg" alt="支付宝" /></span>
        </div>
        
      </div>
      <div class="shang_info">
        <p>打开<span id="shang_pay_txt">支付宝</span>扫一扫，即可进行扫码打赏哦</p>
        <p><a href="//c.runoob.com/codedemo/5348" target="_blank"><span style=" font-size: 14px;color: #000;font-weight: bold;">点我查看本站打赏源码！</span></a></p>
      </div>
    </div>
  <div id="testClick"></div>
 <div style="display:none;">
 
 <script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?3eec0b7da6548cf07db3bc477ea905ee";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>
</div>
<script>
window.jsui={
    www: 'https://www.runoob.com',
    uri: 'https://www.runoob.com/wp-content/themes/runoob'
};
</script>
<style>
ol,ul{list-style:none}.cd-switcher a{text-decoration:none;outline:0}.cd-switcher a:hover{text-decoration:underline}a:focus{outline:0;-moz-outline:0}.main_nav{width:300px;height:60px;margin:60px auto 10px auto}.main_nav li{float:left;width:60px;margin-right:10px;font-size:16px;padding:.6em 1em;border-radius:3em;background:#2f889a;text-align:center}.main_nav li a{color:#fff}.errtip{background-color:#fceaea;color:#db5353;padding:8px 15px;font-size:14px;border:1px solid #fc9797;border-radius:5px}.cd-user-modal{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(52,54,66,0.9);z-index:3;overflow-y:auto;cursor:pointer;visibility:hidden;opacity:0;-webkit-transition:opacity .3s 0,visibility 0 .3s;-moz-transition:opacity .3s 0,visibility 0 .3s;transition:opacity .3s 0,visibility 0 .3s}.cd-user-modal.is-visible{visibility:visible;opacity:1;-webkit-transition:opacity .3s 0,visibility 0 0;-moz-transition:opacity .3s 0,visibility 0 0;transition:opacity .3s 0,visibility 0 0}.cd-user-modal.is-visible .cd-user-modal-container{-webkit-transform:translateY(0);-moz-transform:translateY(0);-ms-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}.cd-user-modal-container{position:relative;width:90%;max-width:500px;background:#FFF;margin:3em auto 4em;cursor:auto;border-radius:.25em;-webkit-transform:translateY(-30px);-moz-transform:translateY(-30px);-ms-transform:translateY(-30px);-o-transform:translateY(-30px);transform:translateY(-30px);-webkit-transition-property:-webkit-transform;-moz-transition-property:-moz-transform;transition-property:transform;-webkit-transition-duration:.3s;-moz-transition-duration:.3s;transition-duration:.3s}.cd-user-modal-container .cd-switcher:after{content:"";display:table;clear:both}.cd-user-modal-container .cd-switcher li{width:50%;float:left;text-align:center}.cd-user-modal-container .cd-switcher li:first-child a{border-radius:.25em 0 0 0}.cd-user-modal-container .cd-switcher li:last-child a{border-radius:0 .25em 0 0}.cd-user-modal-container .cd-switcher a{font-size:1.2em;font-weight:bold;display:block;width:100%;height:50px;line-height:50px;background:#e8f1e2;color:#96b880}.cd-user-modal-container .cd-switcher a.selected{background:#FFF;color:#505260}@media only screen and (min-width:600px){.cd-user-modal-container{margin:4em auto}.cd-user-modal-container .cd-switcher a{height:70px;line-height:70px}}.cd-form{padding:1.4em}.cd-form .fieldset{position:relative;margin:1.4em 0}.cd-form .fieldset:first-child{margin-top:0}.cd-form .fieldset:last-child{margin-bottom:0}.cd-form label{font-size:16px;font-size:.875rem}.cd-form label.image-replace{display:inline-block;position:absolute;left:15px;top:50%;bottom:auto;-webkit-transform:translateY(-50%);-moz-transform:translateY(-50%);-ms-transform:translateY(-50%);-o-transform:translateY(-50%);transform:translateY(-50%);height:20px;width:20px;overflow:hidden;text-indent:100%;white-space:nowrap;color:transparent;text-shadow:none;background-repeat:no-repeat;background-position:50% 0}.cd-form label.cd-username{background-image:url("/wp-content/themes/runoob/assets/img/cd-icon-username.svg")}.cd-form label.cd-email{background-image:url("/wp-content/themes/runoob/assets/img/cd-icon-email.svg")}.cd-form label.cd-password{background-image:url("/wp-content/themes/runoob/assets/img/cd-icon-password.svg")}.cd-form input{margin:0;padding:0;border-radius:.25em}.cd-form input.full-width{width:80%}.cd-form input.full-width2{width:94%}.cd-form input.has-padding{padding:12px 20px 12px 50px}.cd-form input.has-border{border:1px solid #d2d8d8;-webkit-appearance:none;-moz-appearance:none;-ms-appearance:none;-o-appearance:none;appearance:none}.cd-form input.has-border:focus{border-color:#98b880;box-shadow:0 0 5px rgba(52,54,66,0.1);outline:0}.cd-form input.has-error{border:1px solid #d76666}.cd-form input[type=password]{padding-right:65px}.cd-form input[type=submit]{padding:16px 0;cursor:pointer;background:#96b97d;color:#FFF;font-weight:bold;border:0;-webkit-appearance:none;-moz-appearance:none;-ms-appearance:none;-o-appearance:none;appearance:none;font-size:1.2em;font-weight:bold}.no-touch .cd-form input[type=submit]:hover,.no-touch .cd-form input[type=submit]:focus{background:#3599ae;outline:0}@media only screen and (min-width:600px){.cd-form{padding:2em}.cd-form .fieldset{margin:2em 0}.cd-form .fieldset:first-child{margin-top:0}.cd-form .fieldset:last-child{margin-bottom:0}.cd-form input.has-padding{padding:16px 20px 16px 50px}.cd-form input[type=submit]{padding:16px 0}}.cd-close-form{display:block;position:absolute;width:40px;height:40px;right:0;top:-40px;background:url("/wp-content/themes/runoob/assets/img/cd-icon-close.svg") no-repeat center center;text-indent:100%;white-space:nowrap;overflow:hidden}@media only screen and (min-width:1170px){}#cd-login,#cd-signup,#cd-reset-password{display:none}#cd-login.is-selected,#cd-signup.is-selected,#cd-reset-password.is-selected{display:block}
</style>
<div class="cd-user-modal"> 
	<div class="cd-user-modal-container">
		<ul class="cd-switcher">
			<li><a href="javascript:;">用户登录</a></li>
			<li><a href="javascript:;">注册新用户</a></li>
		</ul>

		<div id="cd-login"> <!-- 登录表单 -->
			<div class="cd-form">
				<p class="fieldset">
					<label class="image-replace cd-username" for="signin-username">用户名</label>
					<input class="full-width has-padding has-border" id="signin-username" name=username type="text" placeholder="输入用户名">
				</p>

				<p class="fieldset">
					<label class="image-replace cd-password" for="signin-password">密码</label>
					<input class="full-width has-padding has-border" id="signin-password" name="password" type="password"  placeholder="输入密码">
				</p>
				
				<p class="fieldset">
					<input type="checkbox" id="remember-me" checked>
					<label for="remember-me">记住登录状态</label>
          <a href="//www.runoob.com/reset-password" style="float: right;padding-right: 20px;" target="_blank">忘记密码？</a>
				</p>
 				<input type="hidden" name="action" value="signin">
				<p class="fieldset">
					<input class="full-width2" type="submit" value="登 录">
				</p>
        <div class="err-msg"></div>
			</div>
		</div>

		<div id="cd-signup"> <!-- 注册表单 -->
			<div class="cd-form">
				<p class="fieldset">
					<label class="image-replace cd-password" for="verifycode">邀请码</label>
					<input class="full-width has-padding has-border" id="signup-verifycode" name="verifycode" type="text"  placeholder="输入邀请码">
				</p>
				<p class="fieldset">
					<label class="image-replace cd-username" for="signup-username">用户名</label>
					<input class="full-width has-padding has-border" id="signup-username" name="name" type="text" placeholder="输入用户名">
				</p>

				<p class="fieldset">
					<label class="image-replace cd-email" for="signup-email">邮箱</label>
					<input class="full-width has-padding has-border" name="email" id="signup-email" type="email" placeholder="输入mail">
				</p>

				<p class="fieldset">
					<label class="image-replace cd-password" for="signup-password">密码</label>
					<input class="full-width has-padding has-border" id="signup-password" name="password" type="password"  placeholder="输入密码">
				</p>
				<p class="fieldset">
					<label class="image-replace cd-password" for="signup-password2">重复输入密码</label>
					<input class="full-width has-padding has-border" id="signup-password2" name="password2" type="password"  placeholder="重复输入密码">
				</p>
				
				<!-- 
				<p class="fieldset">
					<input type="checkbox" id="accept-terms">
					<label for="accept-terms">我已阅读并同意 <a href="javascript:;">用户协议</a></label>
				</p>
				 -->
				 
				 <input type="hidden" name="action" value="signup">
				<p class="fieldset">
					<input class="full-width2" type="submit" value="注册新用户">
				</p>
				<p class="fieldset">
				  <a href="//www.runoob.com/w3cnote/runoob-user-test-intro.html#invite" target="_blank">如何获取邀请码？</a>
				  </p>
				<div class="err-msg"></div>
			</div>

		</div>

		<a href="javascript:;" class="cd-close-form">关闭</a>
	</div>
</div> 
<script src="/wp-content/themes/runoob/assets/js/main.min.js?v=1.191"></script>
<script src="//static.runoob.com/assets/libs/hl/run_prettify.js"></script>
</body>
</html>
