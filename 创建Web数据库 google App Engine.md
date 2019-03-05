## [创建Web数据库](https://appinventorapi.com/program-an-api-python/ "创建Web数据库")

**TinyWebDB** 是一个**App Inventor**组件，它使您的Android应用程序能访问Web。您可以使用TinyWebDB访问Web数据源（data source API）或将应用程序的数据持久存储在Web数据库中。这里向您展示如何实现后者 - **设置Web数据库**，并使用**Google**的免费[App Engine service](https://en.wikipedia.org/wiki/Google_App_Engine) 服务在云中进行设置。使用此处提供的示例代码，您可以在几分钟内设置一个位于Google服务器上的Web数据库，您无需成为程序员即可做到。

请注意，App Inventor还提供了TinyDB组件。TinyDB是直接在手机上存储数据，使用起来更简单。只有在手机和应用程序之间需要共享数据时才需要TinyWebDB（例如，社交应用程序，多人游戏）。

默认情况下，TinyWebDB组件将数据存储在App Inventor提供的测试服务上，[http://appinvtinywebdb.appspot.com/](//appinvtinywebdb.appspot.com/) 。此服务有助于测试，但它由所有App Inventor用户共享，并且限制为1000个条目。如果您使用它，您的数据最终将被覆盖。

对于除测试之外的任何其他内容，您将需要创建不与其App Inventor应用程序和开发者共享的自定义Web服务。您无需成为程序员也可以这样做 - 只需按照以下说明操作，您就可以在几分钟内获得自己的服务。

要创建自己的Web服务，请按照以下说明操作：

-   从[http://code.google.com/appengine/](http://code.google.com/appengine/)下载App Engine for Python 。确保并下载适用于Python的**App Engine SDK**。安装后，单击其图标运行 _GoogleAppEngineLauncher_。
-   下载 [sample web database code](http://sites.google.com/site/appinventor/sample-tinywebdb-services/appinventordb.zip?attredirects=0&d=1)。它是一个zip文件，包含自定义Web database service 的 source code。
-   解压缩下载的zip文件。它将建出一个名为**appinventordb**的文件夹。您可以根据需要重命名。
-   在**GoogleAppEngineLauncher** (Launcher: 发射台) 中，选择**File | Add Existing Application** 浏览以设置您刚刚解压缩的appinventordb文件夹的路径。然后单击“运行”按钮。这将启动在本地计算机上运行的测试Web服务。
-   您可以通过打开浏览器并输入“localhost：8080”作为URL来测试服务。您将看到Web服务的网页界面。此服务的最终目标是与使用App Inventor创建的移动应用程序进行通信。但是该服务为服务提供了一个网页界面，以帮助程序员进行调试。您可以手动调用get和store操作，查看现有条目，还可以删除单个条目
-   您的应用尚未在网络上，因此App Inventor应用尚无法访问。要实现这一目标，您需要将其上传到Google的App Engine服务器。
-   在GoogleAppEngineLauncher中，选择信息中心。输入您的Google帐户信息，您将进入App Engine信息中心。
-   选择创建应用程序。您需要指定全局唯一的应用程序标识符。记住应用程序标识符，稍后您将需要它。为您的应用程序提供名称，然后单击“创建应用程序”以进 如果您的标识符是唯一的，那么您现在在Google服务器上有一个新的空白应用。
-   在本地计算机上打开文本编辑器，然后在解压缩的appinventordb文件夹中打开app.yaml文件。修改第一行，以便应用程序与您在Google上设置的应用程序标识符匹配。
-   在GoogleAppEngineLauncher中，选择“部署”，然后按照部署应用程序的步骤操作。
-   测试您的应用是否在网络上运行。在浏览器中输入myapp.appspot.com，仅将您的应用程序标识替换为“myapp”。该应用程序应与在本地测试服务器上运行时的外观相同。只有现在，它才能上网，您可以从App Inventor for Android应用程序访问它。

**App Inventor客户端应用程序**

拥有“符合App-Inventor标准”的Web数据库后，您可以创建访问它的App Inventor应用程序。对于刚刚创建的示例，请执行以下操作：

-   将TinyWebDB组件拖入组件设计器。
-   将ServiceURL属性从默认的[http://appinvtinywebdb.appspot.com/](http://appinvtinywebdb.appspot.com/)修改为您的服务的URL。
-   任何StoreValue操作（块）都将在您的服务中存储数据，任何GetValue操作都将从您的服务中检索。

以下是一些存储和检索数据的块：

[![](https://appinventormash.files.wordpress.com/2010/07/appinventordbclient.png?w=468&h=316 "appinventordbClient")](https://appinventormash.files.wordpress.com/2010/07/appinventordbclient.png)


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk1Nzk0NTQ1NSwxNzk5MzMxODg5LDczMD
k5ODExNl19
-->