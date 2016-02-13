## index.htmlアクセステスト

1. コンテキストルートにindex.jspを配置
2. &lt;mvc:default-servlet-handler&gt;なし
3. &lt;welcome-file-list&gt;はindex.htmlのみ

- index : 1
- index2: 1,2
- index3: 1,3
- index4: 1,2,3

### http://.../&lt;context-root&gt;にアクセスした時に表示されるもの
|      |Tomcat        |JBoss|Glassfish3    |Glassfish4|
|------|--------------|-----|--------------|----------|
|index |index.jsp     | <-  |HomeController| <-       |
|index2|index.jsp     | <-  |HomeController| <-       |
|index3|HomeController| <-  |HomeController| <-       |
|index4|HomeController| <-  |HomeController| <-       |

何の場合も、&lt;context-root&gt;/index.jspにアクセスすれば、index.jspは表示される。
