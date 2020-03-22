# HTTP方法与状态码

## http方法

- get post 为主
- get
  1.  User-Agent 你的请求一般都是代理发出的，当你使用浏览器时你的代理变为浏览器，你用客户端代理是客户端，通过修改这个可以进行身份的伪装，服务端可以根据这个进行一定的反爬
  2. get 请求全部放在head里

- post
  1. post 先发送头部，然后发送一个body，里面包含其他内容

- 请求码

  1. 切换协议

  2. 成功
  3. 请求转移，重定向     douban.com -> www.douban.com
  4. 客户端错误 
  5. 服务器错误

## http header

- accept    我想要什么数据
- cookie   
- user-agent       代理
- referer(referrer)  防盗链接（可能转链接时添加声明）
- content-type 内容格式，txt/json/img and so on      我给你的是什么数据