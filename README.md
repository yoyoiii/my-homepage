
### 主页地址
[柚子不困](https://yoyoiii.github.io/my-hompepage/)


### 特别感谢
[Tomotoes](https://github.com/Tomotoes/HomePage)

### 必备条件

- Nodejs 6.0 以上
- Git 可用



### 功能特性

1. 高度封装了页面中的所有的信息
2. 使用 [WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/) 作为背景
3. 使用 `scss` 作为 `css` 预处理器
4. 使用 `pug` 作为 `html` 预处理器
5. 使用 `gulp` 作为构建工具, 并以配置好构建脚本
6. 令人舒服的动画 , 以及漂亮的 `UI`
7. 响应式，无缝支持移动端
8. 所引用的 `css` 与 `js` 文件总共超不过 `18.5` kb!
9. 延迟响应切换页面事件



### 项目结构

根据项目特点,一共分为两大类 ：
1. `intro` 首屏：炫酷动画
2. `main` 副屏：个人信息



### 高级配置

#### WebGL-Fluid-Simulation

首页使用[WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/)作为背景。

如需关闭，请设置`intro.background: false`。


#### 图标的替换
项目中的图标，全部来自 [阿里巴巴矢量图标库](https://www.iconfont.cn)

替换步骤如下:

1. 请选择好你的图标，添加到项目后，把颜色全部调成白色。
2. 点击 Font Class 方式
3. 复制生成的链接中的内容
4. 替换 文件 `css/common/icon.scss` 中的内容 ，其中 `icon` 选择器中的内容必须保留。
5. 配置 `config.json` 文件中的相应项 `main.ul.*.icon`

```css
.icon {
	display: block;
	width: 1.5em;
	height: 1.5em;
	margin: 0 auto;
	fill: currentColor;
	font-family: 'iconfont' !important;
	font-size: inherit;
	font-style: normal;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
```


### 项目部署

在根目录下执行`npm run build` 后，会将项目文件生成到 `dist` 目录。

然后，你可以将 `dist` 目录部署到你喜欢的服务器托管商。


### GitHub Action

若将页面部署到 `GithubPage` ：

1. 本地生成 `dist` 目录后，执行 `git push origin main`，将修改推到远程。
2. `.github/workflows` 目录下的 `.yml` 文件，会把 `dist` 目录合并到 `gh-pages` 分支，实现自动部署。
3. 此 `GitHub Action` 用到 [peaceiris/actions-gh-pages](https://github.com/peaceiris/actions-gh-pages)，首次部署需要配置权限，详情请见 [First Deployment with GITHUB_TOKEN](https://github.com/peaceiris/actions-gh-pages#%EF%B8%8F-first-deployment-with-github_token)。

