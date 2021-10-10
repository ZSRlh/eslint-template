# Eslint + Prettier

## Eslint

##### 安装

```bash
npm install --save-dev eslint
npm install --save-dev eslint-plugin-react
npm install --save-dev eslint-plugin-react-hook
npm install --save-dev eslint-plugin-import
```

##### 配置

[Eslint 配置规则](https://eslint.org/docs/rules/)

##### 命令行

使用以下格式运行 eslint：
eslint [options] [file|dir|glob}\*

- --ext：检查代码（自己理解的。。。
- --fix：自动修复问题
  [Eslint 命令行](https://eslint.bootcss.com/docs/user-guide/command-line-interface)

## Prettier

eslint 配置中兼容了代码风格的配置项，可以通过引入 eslint 插件进行配置：

```bash
npm intall --save-dev prettier
npm intall --save-dev eslint-config-prettier
npm intall --save-dev eslint-plugin-prettier
```

引入插件后，在 .eslintrc.json 文件中作如下配置：

```json
{
  // ...
  "plugins": [
    ...
    "prettier"
  ],
  "rules": {
    "prettier/prettier": "error",
    // ...
  }
}
```

## git 提交前自动检查格式

插件：pre-commit

```bash
npm install --save-dev pre-commit
```

package.json 中配置：

```json
{
  "pre-commit": ["lint"], // git commit 时运行 npm run lint
  "scripts": {
    // ...
    "lint": "eslint --ext .js --ext .jsx src" // 检查代码是否符合eslint规则
  }
}
```
