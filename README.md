<p align="center">
<a href="https://www.duxravel.com/">
    <img src="https://github.com/duxphp/duxravel/blob/main/resources/image/watermark.png?raw=true" width="100" height="100">
</a>

<p align="center">Duxravel 会员中心</p>

<p align="center">
<a href="https://doc.duxravel.com">中文文档</a>
</p>

<p align="center">
    <a href="https://packagist.org/packages/duxphp/duxravel-member">
        <img src="https://img.shields.io/github/v/release/duxphp/duxravel-member">
    </a>
    <a href="https://packagist.org/packages/duxphp/duxravel-member">
        <img src="https://img.shields.io/packagist/dt/duxphp/duxravel-member.svg?style=flat-square">
    </a>
    <a href="https://packagist.org/packages/duxphp/member">
        <img src="https://img.shields.io/packagist/l/duxphp/duxravel-member.svg?maxAge=2592000&&style=flat-square" alt="Packagist">
    </a>
</p>

## 说明
本模块需配合Duxravel使用

## 应用安装
```
// 正式版
composer require ftlh2005/duxravel-member

// 开发版
composer require ftlh2005/duxravel-member dev-main
```


## 接口授权
请求登录接口后回去 token 在 header 头中的 Authorization 参数带入授权 token 可请求需授权接口
```
请求 headers
名称      	    示例	                说明
Accept	        application/json	返回类型
Content-MD5	    1ED5ED64ED37F4F73E8F018187AF450E	数据签名
Content-Date	1624942695	当前请求时间戳
AccessKey	    123456	后台创建的 SECRET_ID
Authorization	Bearer xxxx	用户授权 token (JWT授权时需要)
```


```
// apifox 请求示例
headers.upsert({
  key: 'Authorization',
  value: 'Bearer ' + token,
});
```

## 接口说明
```
/**
 * 用户登录
 * @params string tel 手机号码
 * @params string password 登录密码
 */
post api/auth/login

/**
 * 用户信息 （授权）
 */
post api/auth/info
```

## 更新日志
```
暂无
```

## 维护者

[@duxphp](https://github.com/duxphp)

## 使用许可

[MIT](LICENSE) © Richard Littauer