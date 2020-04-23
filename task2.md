# Beautiful Soup库入门
+ 学习beautifulsoup基础知识。
+ 使用beautifulsoup解析HTML页面。
Beautiful Soup 是一个HTML/XML 的解析器，主要用于解析和提取 HTML/XML 数据。
它基于HTML DOM 的，会载入整个文档，解析整个DOM树，因此时间和内存开销都会大很多，所以性能要低于lxml。  

BeautifulSoup 用来解析 HTML 比较简单，API非常人性化，支持CSS选择器、Python标准库中的HTML解析器，也支持 lxml 的 XML解析器。  

虽然说BeautifulSoup4 简单容易比较上手，但是匹配效率还是远远不如正则以及xpath的，一般不推荐使用，推荐正则的使用。  

第一步：pip install beautifulsoup4 ，万事开头难，先安装 beautifulsoup4，安装成功后就完成了第一步。  

第二步：导入from bs4 import BeautifulSoup  

第三步：创建 Beautiful Soup对象 soup = BeautifulSoup(html，’html.parser’)  
# 学习xpath
+ 学习目标：学习xpath，使用lxml+xpath提取内容。
+ Xpath常用的路径表达式：
XPath即为XML路径语言（XML Path Language），它是一种用来确定XML文档中某部分位置的语言。  
在XPath中，有七种类型的节点：元素、属性、文本、命名空间、处理指令、注释以及文档（根）节点。  
XML文档是被作为节点树来对待的。  
XPath使用路径表达式在XML文档中选取节点。节点是通过沿着路径选取的。  
+ 使用lxml解析
