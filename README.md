# Obsidian Sample Plugin
# Obsidian 示例插件

This is a sample plugin for Obsidian (https://obsidian.md).
这是一个 Obsidian (https://obsidian.md) 的示例插件。

This project uses TypeScript to provide type checking and documentation.
该项目使用 TypeScript 来提供类型检查和文档。

The repo depends on the latest plugin API (obsidian.d.ts) in TypeScript Definition format, which contains TSDoc comments describing what it does.
该仓库依赖于最新的插件 API (obsidian.d.ts) 的 TypeScript 定义格式，其中包含描述其功能的 TSDoc 注释。

This sample plugin demonstrates some of the basic functionality the plugin API can do.
这个示例插件演示了插件 API 可以实现的一些基本功能。

- Adds a ribbon icon, which shows a Notice when clicked.
- 添加一个功能区图标，点击时显示通知。
- Adds a command "Open Sample Modal" which opens a Modal.
- 添加一个"打开示例模态框"命令，用于打开模态框。
- Adds a plugin setting tab to the settings page.
- 在设置页面添加一个插件设置选项卡。
- Registers a global click event and output 'click' to the console.
- 注册一个全局点击事件，并在控制台输出 'click'。
- Registers a global interval which logs 'setInterval' to the console.
- 注册一个全局定时器，在控制台记录 'setInterval'。

## First time developing plugins?
## 第一次开发插件？

Quick starting guide for new plugin devs:
新插件开发者的快速入门指南：

- Check if [someone already developed a plugin for what you want](https://obsidian.md/plugins)! There might be an existing plugin similar enough that you can partner up with.
- 检查是否[已经有人开发了你想要的插件](https://obsidian.md/plugins)！可能已经有足够相似的插件，你可以与其合作。
- Make a copy of this repo as a template with the "Use this template" button (login to GitHub if you don't see it).
- 使用"使用此模板"按钮复制此仓库作为模板（如果看不到请登录 GitHub）。
- Clone your repo to a local development folder. For convenience, you can place this folder in your `.obsidian/plugins/your-plugin-name` folder.
- 将你的仓库克隆到本地开发文件夹。为了方便，你可以将此文件夹放在你的 `.obsidian/plugins/your-plugin-name` 文件夹中。
- Install NodeJS, then run `npm i` in the command line under your repo folder.
- 安装 NodeJS，然后在你的仓库文件夹下的命令行中运行 `npm i`。
- Run `npm run dev` to compile your plugin from `main.ts` to `main.js`.
- 运行 `npm run dev` 将你的插件从 `main.ts` 编译为 `main.js`。
- Make changes to `main.ts` (or create new `.ts` files). Those changes should be automatically compiled into `main.js`.
- 对 `main.ts`（或创建新的 `.ts` 文件）进行更改。这些更改应该会自动编译到 `main.js` 中。
- Reload Obsidian to load the new version of your plugin.
- 重新加载 Obsidian 以加载插件的新版本。
- Enable plugin in settings window.
- 在设置窗口中启用插件。
- For updates to the Obsidian API run `npm update` in the command line under your repo folder.
- 要更新 Obsidian API，请在你的仓库文件夹下的命令行中运行 `npm update`。

## Releasing new releases
## 发布新版本

- Update your `manifest.json` with your new version number, such as `1.0.1`, and the minimum Obsidian version required for your latest release.
- 使用新的版本号（如 `1.0.1`）更新你的 `manifest.json`，以及你最新版本所需的最低 Obsidian 版本。
- Update your `versions.json` file with `"new-plugin-version": "minimum-obsidian-version"` so older versions of Obsidian can download an older version of your plugin that's compatible.
- 使用 `"new-plugin-version": "minimum-obsidian-version"` 更新你的 `versions.json` 文件，以便旧版本的 Obsidian 可以下载与其兼容的旧版本插件。
- Create new GitHub release using your new version number as the "Tag version". Use the exact version number, don't include a prefix `v`. See here for an example: https://github.com/obsidianmd/obsidian-sample-plugin/releases
- 使用你的新版本号作为"标签版本"创建新的 GitHub 发布。使用确切的版本号，不要包含前缀 `v`。示例请参见：https://github.com/obsidianmd/obsidian-sample-plugin/releases
- Upload the files `manifest.json`, `main.js`, `styles.css` as binary attachments. Note: The manifest.json file must be in two places, first the root path of your repository and also in the release.
- 上传文件 `manifest.json`、`main.js`、`styles.css` 作为二进制附件。注意：manifest.json 文件必须在两个地方，首先是你的仓库根路径，其次是在发布中。
- Publish the release.
- 发布版本。

> You can simplify the version bump process by running `npm version patch`, `npm version minor` or `npm version major` after updating `minAppVersion` manually in `manifest.json`.
> 你可以通过在 `manifest.json` 中手动更新 `minAppVersion` 后运行 `npm version patch`、`npm version minor` 或 `npm version major` 来简化版本更新过程。
> The command will bump version in `manifest.json` and `package.json`, and add the entry for the new version to `versions.json`
> 该命令将更新 `manifest.json` 和 `package.json` 中的版本，并在 `versions.json` 中添加新版本的条目

## Adding your plugin to the community plugin list
## 将你的插件添加到社区插件列表

- Check the [plugin guidelines](https://docs.obsidian.md/Plugins/Releasing/Plugin+guidelines).
- 查看[插件指南](https://docs.obsidian.md/Plugins/Releasing/Plugin+guidelines)。
- Publish an initial version.
- 发布初始版本。
- Make sure you have a `README.md` file in the root of your repo.
- 确保你的仓库根目录中有 `README.md` 文件。
- Make a pull request at https://github.com/obsidianmd/obsidian-releases to add your plugin.
- 在 https://github.com/obsidianmd/obsidian-releases 提交拉取请求以添加你的插件。

## How to use
## 如何使用

- Clone this repo.
- 克隆此仓库。
- Make sure your NodeJS is at least v16 (`node --version`).
- 确保你的 NodeJS 至少是 v16 版本（`node --version`）。
- `npm i` or `yarn` to install dependencies.
- 运行 `npm i` 或 `yarn` 来安装依赖。
- `npm run dev` to start compilation in watch mode.
- 运行 `npm run dev` 以在监视模式下开始编译。

## Manually installing the plugin
## 手动安装插件

- Copy over `main.js`, `styles.css`, `manifest.json` to your vault `VaultFolder/.obsidian/plugins/your-plugin-id/`.
- 将 `main.js`、`styles.css`、`manifest.json` 复制到你的库 `VaultFolder/.obsidian/plugins/your-plugin-id/`。

## Improve code quality with eslint (optional)
## 使用 eslint 提高代码质量（可选）

- [ESLint](https://eslint.org/) is a tool that analyzes your code to quickly find problems. You can run ESLint against your plugin to find common bugs and ways to improve your code.
- [ESLint](https://eslint.org/) 是一个分析你的代码以快速发现问题的工具。你可以对你的插件运行 ESLint 来发现常见错误和改进代码的方法。
- To use eslint with this project, make sure to install eslint from terminal:
- 要在此项目中使用 eslint，请确保从终端安装 eslint：
  - `npm install -g eslint`
  - `npm install -g eslint`
- To use eslint to analyze this project use this command:
- 要使用 eslint 分析此项目，请使用此命令：
  - `eslint main.ts`
  - `eslint main.ts`
  - eslint will then create a report with suggestions for code improvement by file and line number.
  - eslint 然后会创建一个报告，按文件和行号提供代码改进建议。
- If your source code is in a folder, such as `src`, you can use eslint with this command to analyze all files in that folder:
- 如果你的源代码在一个文件夹中，比如 `src`，你可以使用此命令来分析该文件夹中的所有文件：
  - `eslint .\src\`
  - `eslint .\src\`

## Funding URL
## 资助 URL

You can include funding URLs where people who use your plugin can financially support it.
你可以包含资助 URL，让使用你插件的人可以在经济上支持它。

The simple way is to set the `fundingUrl` field to your link in your `manifest.json` file:
简单的方法是在你的 `manifest.json` 文件中设置 `fundingUrl` 字段为你的链接：

```json
{
    "fundingUrl": "https://buymeacoffee.com"
}
```

If you have multiple URLs, you can also do:
如果你有多个 URL，你也可以这样做：

```json
{
    "fundingUrl": {
        "Buy Me a Coffee": "https://buymeacoffee.com",
        "GitHub Sponsor": "https://github.com/sponsors",
        "Patreon": "https://www.patreon.com/"
    }
}
```

## API Documentation
## API 文档

See https://github.com/obsidianmd/obsidian-api
请参见 https://github.com/obsidianmd/obsidian-api