# sit-robot-book
上海应用技术大学机器人爱好者协会自建教程网站，已配置github action，大家只要push新文章，action将自动部署到我们的教程网站
[https://sit-robot.github.io/](https://sit-robot.github.io/)

## 使用步骤
本书基于mdbook编写，本机需配置Rust环境。

### 安装 Rust 环境
[https://rustup.rs/](https://rustup.rs/)

### 换源

### 安装 mdbook
```bash
cargo install mdbook
```

### 安装 mdbook-mdbook-mermaid
由于书中使用了mdbook-mermaid流程图，故需安装插件
```bash
cargo install mdbook-mermaid
```

### 预览图书
```bash
mdbook serve
```
打开浏览器即可阅读
[http://localhost:3000/](http://localhost:3000/)