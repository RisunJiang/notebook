---


---

<h2 id="创建web数据库"><a href="https://appinventorapi.com/program-an-api-python/" title="创建Web数据库">创建Web数据库</a></h2>
<p><strong>TinyWebDB</strong> 是一个<strong>App Inventor</strong>组件，它使您的Android应用程序能访问Web。您可以使用TinyWebDB访问Web数据源（data source API）或将应用程序的数据持久存储在Web数据库中。这里向您展示如何实现后者 - <strong>设置Web数据库</strong>，并使用<strong>Google</strong>的免费<a href="https://en.wikipedia.org/wiki/Google_App_Engine">App Engine service</a> 服务在云中进行设置。使用此处提供的示例代码，您可以在几分钟内设置一个位于Google服务器上的Web数据库，您无需成为程序员即可做到。</p>
<p>请注意，App Inventor还提供了TinyDB组件。TinyDB是直接在手机上存储数据，使用起来更简单。只有在手机和应用程序之间需要共享数据时才需要TinyWebDB（例如，社交应用程序，多人游戏）。</p>
<p>默认情况下，TinyWebDB组件将数据存储在App Inventor提供的测试服务上，<a href="//appinvtinywebdb.appspot.com/">http://appinvtinywebdb.appspot.com/</a> 。此服务有助于测试，但它由所有App Inventor用户共享，并且限制为1000个条目。如果您使用它，您的数据最终将被覆盖。</p>
<p>对于除测试之外的任何其他内容，您将需要创建不与其App Inventor应用程序和开发者共享的自定义Web服务。您无需成为程序员也可以这样做 - 只需按照以下说明操作，您就可以在几分钟内获得自己的服务。</p>
<p>要创建自己的Web服务，请按照以下说明操作：</p>
<ul>
<li>从<a href="http://code.google.com/appengine/">http://code.google.com/appengine/</a>下载App Engine for Python 。确保并下载适用于Python的<strong>App Engine SDK</strong>。安装后，单击其图标运行 <em>GoogleAppEngineLauncher</em>。</li>
<li>下载 <a href="http://sites.google.com/site/appinventor/sample-tinywebdb-services/appinventordb.zip?attredirects=0&amp;d=1">sample web database code</a>。它是一个zip文件，包含自定义Web database service 的 source code。</li>
<li>解压缩下载的zip文件。它将建出一个名为<strong>appinventordb</strong>的文件夹。您可以根据需要重命名。</li>
<li>在<strong>GoogleAppEngineLauncher</strong> (Launcher: 发射台) 中，选择<strong>File | Add Existing Application</strong> 浏览以设置您刚刚解压缩的 <strong>appinventordb</strong> 文件夹的路径。然后单击 <strong>Run</strong> 按钮。这样将启动在本地计算机上运行的测试Web服务。</li>
<li>您可以通过打开浏览器并输入“<strong>localhost:8080</strong>” 作为URL来测试服务。您将看到Web服务的网页界面。此服务的最终目标是与采用App Inventor创建的移动应用程序进行通信。但是该服务同时也提供了一个网页界面，以帮助程序员进行调试。您可以手动调用get和store操作，查看现有条目，还可以删除单个条目。</li>
<li>您的应用尚未在网络上，因此App Inventor应用尚无法访问。要实现这一目标，您需要将其 <strong>上传</strong> 到Google的 <strong>App Engine servers</strong> 上。</li>
<li>在 <strong>GoogleAppEngineLauncher</strong> 中，选择 <strong>Dashboard</strong>。输入您的 <strong>Google帐户</strong> 信息，您将进入<strong>App Engine dashboard</strong>。</li>
<li>选择 <strong>Create an Application</strong> 创建应用程序。您需要指定全局唯一的<strong>Application Identifer</strong> (应用程序标识符)。记住Application Identifer，稍后您将需要它。为您的应用程序提供名称，然后单击 <strong>Create Application to submit</strong>(提交创建应用程序） 如果您的标识符是唯一的，那么您现在在Google服务器上有一个新的空白应用。</li>
<li>在本地计算机上打开文本编辑器，然后在解压缩的 appinventordb 文件夹中打开 <strong>app.yaml</strong> 文件。修改第一行，以便应用程序与您在Google上设置的应用<strong>Application Identifer</strong> 匹配。</li>
<li>在GoogleAppEngineLauncher中，选择 <strong>Deploy</strong>(部署)，然后按照部署应用程序的步骤操作。</li>
<li>测试您的应用是否在网络上运行。在浏览器中输入 <strong><em>myapp</em>.appspot.com</strong>，仅用您的Application Identifer 替换 “<em>myapp</em>”。该应用程序应与您在本地测试服务器上运行时的外观相同。只到现在，它才能真的上网了，您可以通过你的 <strong>App Inventor for Android</strong> 应用程序访问它了。</li>
</ul>
<p><strong>App Inventor客户端应用程序</strong></p>
<p>拥有“App-Inventor-compliant” (App-Inventor兼容) 的Web数据库后，您就可以创建访问它的 App Inventor应用程序了。对于刚刚创建的示例，请执行以下操作：</p>
<ul>
<li>将TinyWebDB组件拖入组件设计器。</li>
<li>将ServiceURL属性从默认的<a href="http://appinvtinywebdb.appspot.com/">http://appinvtinywebdb.appspot.com/</a>修改为您的服务的URL。</li>
<li>所以 <strong>StoreValue</strong> 的操作（块）都将在您的服务中存储数据，任何 <strong>GetValue</strong>操作都将从您的服务中提取数据。</li>
</ul>
<p>以下是一些存储和提取数据的块：</p>
<p><a href="https://appinventormash.files.wordpress.com/2010/07/appinventordbclient.png"><img src="https://appinventormash.files.wordpress.com/2010/07/appinventordbclient.png?w=468&amp;h=316" alt="" title="appinventordbClient"></a></p>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjMzNDc5NTQ0XX0=
-->