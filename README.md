# Boss-Direct-Hiring-Batch-Communication-Script
## 描述 
Boss直聘批量投递脚本，Boss没有批量投递功能，而且Boss回复率太低 ，为了提高找工作效率而制作，将就能用

## 依赖
  Python 程序  
  Edge 浏览器  
  Edge webdriver：https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/  

## 实现思路
### 首次执行脚本，判断 cookie 文件是否存在  
  不存在 cookie 文件，则先访问登录页面，给用户70秒时间让他们登陆，等时间一到，获取当前页面 cookie 并存储到当前路径中  
  然后继续给用户 300 秒的时间，通过浏览器安装插件提取浏览器可以使用的cookie  
### 再次执行脚本，判断 cookie 文件是否存在  
  存在 cookie 文件，则访问预先配置好的搜索链接 search_url 访问，并获取元素节点执行点击操作  

### 注意
  Edge webdriver 和 Edge 浏览器版本要统一，浏览器地址栏输入 edge://version/ 可以查看浏览器版本  
  执行脚本首先会给用户 70秒（这个可以自己修改时间）登录获取到 cookie 文件的时间   
  执行脚本登陆完成后会再给用户 300秒（这个可以自己修改时间）通过 Edge 浏览器安装 J2TEAM Cookies 插件，并提取浏览器可以使用的 cookie  
  提取浏览器通用 cookie 文件这样做的目的是为了让本机浏览器的 cookie 互通防止登录之后顶掉其他浏览器的登录状态   
  之后在其他浏览器通过 J2TEAM Cookies 插件倒入浏览器通用 cookie 文件，就算是 登录成功  
  搜索链接 search_url 怎么配置，其实很简单，随便打开浏览器登录 Boss 直聘，搜索自己想要投递的职位并复制地址栏的地址粘贴到 Boss批量投递脚本.py 脚本的变量 search_url 中即可  
  



