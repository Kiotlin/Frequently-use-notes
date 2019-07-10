## 科大博客提供 Google Fonts 加速

原文链接：[科大博客提供 Google Fonts 加速](https:://servers.ustclug.org/2014/06/blog-googlefonts-speedup/)

由于 [fonts.googleapis.com](fonts.googleapis.com) 在国内访问不稳定，USTC Blog 某些主题中的字体加载不出来。现在 LUG 提供了 Google Fonts 加速服务，已经把 WordPress 原始代码和用户主题内的 Google 字体和 CSS、JS 文件替换成了 LUG 的代理，以加速字体的显示。

事实上 360 网站卫士已经提供了 Google Fonts 加速服务 [libs.useso.com](libs.useso.com)，但不支持 HTTPS。HTTPS 博客内只能引用 HTTPS 资源，因此不能用他们的服务，只好自建了。我们的做法与他们类似，我们的服务器通过对用户的请求做代理，并修改 HTTP 响应内容中的 URL（例如 fonts.googleapis.com 中会引用 themes.googleusercontent.com 的资源）。感谢 雨路 和 stephen 的建议。

如果您的博客不在科大 LUG 上，也想使用加速服务，请在 WordPress 源码内进行如下替换：
> ajax.googleapis.com => ajax.lug.ustc.edu.cn    

> fonts.googleapis.com => fonts.lug.ustc.edu.cn    

> themes.googleusercontent.com => google-themes.lug.ustc.edu.cn

如果您的科大博客在此修改之后出现无法显示字体的问题，请联系我们：support@blog.ustc.edu.cn。
