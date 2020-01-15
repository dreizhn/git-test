
<!Doctype html>
<html>
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
	


<script src="/wp-content/themes/runoob/assets/js/main.min.js?v=1.191"></script>
<script src="//static.runoob.com/assets/libs/hl/run_prettify.js"></script>
</body>
</html>
