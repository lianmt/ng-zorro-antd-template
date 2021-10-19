# ng-zorro-antd

> 用了一下 angular，本来想搭建一个脚手架 ng-zorro-ant-template，但是一开始搭环境，就各种问题，让我失去了兴趣。初体验非常糟糕。但，还是要硬刚，搞定它。
​
### 安装运行 
```
git clone git@github.com:lianmt/ng-zorro-antd-template.git

cd ng-zorro-antd-template

ng serve
```
​
gitee 仓库
```git
git@gitee.com:lianmt/ng-zorro-antd-template.git
```
### 踩坑
#### 升级 Angular 失败
​
1、
​
根据官网，安装 angular

```bash
npm install -g @angular/cli
```
​
angular/cli 是 @12.2.10，但是 angular 却不是最高版本。
​

但是 ng-zorro 框架，要求 Angular ^12.0.0。
​

于是我要升级 angular。直接安装不成功，要清缓存，mac 缓存又清不了，又一个坑···
​

提示需要升级 npm 到 8.1.0。
​
2、
​

更新 npm，发现 `npm -v` 版本还是没有改变。
​

一查，有两个 npm 版本，安装 nodejs 时，自带一个版本，新安装的 npm 又一个版本。但前者优先级更高。
​

3、
​

没办法，卸载 nodejs，重新下载 nodejs。
​

参考链接：[Mac nodejs卸载、安装](https://www.jianshu.com/p/5ce3b80ee000)
​

4、
​

发现，新下载的 npm 版本，也不是最新版本。
​

而且，angular 出现异常 `ng: command not found`，`npm link @angular/cli` 无效···
​

好麻烦，浪费时间，我不想搞了。
​

angular-cli 应该是一个打包服务，但是却各种问题，连带电脑的环境都出现了问题，一开始用的体验，就非常糟糕，失去了兴趣，弃坑。
​

#### 使用经验
​
1、
​

之前我搭建过，成功跑起来了，但没装 ng-zorro。

之前使用的时候，还有一个低级的问题，起两个 angular，提示端口居然被占用，居然不是动态的···
​

2、
​

angular 的路由，不是抽象出来一个文件管理，而是放在目录树结构里。你新建一个目录，新建一个文件，同时新建一个路由，带着一起的。
​

3、
​

ng-zorro 有一个 ng-alain 框架，我 2018 年用过这个原型模板，功能非常完善，而且还除了商业原型模板，三四百这样。
​

#### 搞定它
​
1、
​

然而，不解决这个问题，心里也不爽，也担心删除 nodejs 会带来其它影响。
​

去他妈的 angular，还是要搞起来。
​

2、
​

again 卸载、重装、清缓存，无果。
​

一怒之下，把根目录的 npm、nodejs 隐藏文件，全删了。当然，要保存在另一个文件夹，避免出错。
​

more，nodejs 卸载、重装、清缓存。
​

ng 居然跑起来了，还是 angular-cli@12.2.10。
​

3、
​

安装 ng-zorro-antd，一切顺利。
​
### 多个仓库
​
发现，gitee 可以直接导入 github 仓库，添加仓库时有这个选项。
​

gitee 还有同步 github 代码的功能。在仓库名称右侧，点击刷新按钮即可。搞定。

![image.png](https://cdn.nlark.com/yuque/0/2021/png/103225/1634640849142-723fa2cf-1656-4da8-a583-f2fb5a948d4e.png#clientId=ubcfb4717-ad77-4&from=paste&height=323&id=u45914c68&margin=%5Bobject%20Object%5D&name=image.png&originHeight=248&originWidth=250&originalType=binary&ratio=1&size=13157&status=done&style=none&taskId=u86cf9371-0a22-439c-a988-fa3559df399&width=326)
### 我的账号


Github：[github.com/lianmt](https://github.com/lianmt)

Gitee：[gitee.com/lianmt](https://gitee.com/lianmt)


## data 

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 12.2.10.

### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
