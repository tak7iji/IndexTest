## index.htmlアクセステスト

1. コンテキストルートにindex.jspを配置
2. <mvc:default-servlet-handler>なし
3. <welcome-file-list>はindex.htmlのみ

- index : 1
- index2: 1,2
- index3: 1,3
- index4: 1,2,3

      |Tomcat        |JBoss|Glassfish3    |Glassfish4
index |index.jsp     | <-  |HomeController| <-
index2|index.jsp     | <-  |HomeController| <-
index3|HomeController| <-  |HomeController| <-
index4|HomeController| <-  |HomeController| <-
