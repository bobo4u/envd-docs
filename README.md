<div align="center">
<h1>envd-docs</h1>
</div>

<p align=center>
<a href="https://discord.gg/KqswhpVgdU"><img alt="discord invitation link" src="https://img.shields.io/discord/974584200327991326?label=discord&style=social"></a>
<a href="https://app.netlify.com/sites/envd/deploys"><img alt="netlify status" src="https://api.netlify.com/api/v1/badges/535ba0bd-b9fa-43b4-a8b2-ce2fbfa3a424/deploy-status"></a>
</p>
This website is built using [VitePress](https://vitepress.vuejs.org/), Vite & Vue Powered Static Site Generator.

### Installation

```shell
# npm i -g pnpm 这条命令安装以后，pnpm一直安装有问题
npm i pnpm -g
pnpm i
```

### Local Development

```shell
# dev en-US docs
pnpm dev
# dev zh-CN docs
pnpm dev:zh
# 阿里云主机并暴露5173端口供web访问
pnpm dev:zh --host 172.25.16.119
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```shell
# build en-US docs
pnpm build
# build zh-CN docs
pnpm build:zh
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Tips

Recommended to read the following part before you start to contribute the docs.

- Chinese docs is under `/docs-zh`
- VitePress Markdown features [VitePress Markdown](https://vitepress.vuejs.org/guide/markdown.html)
- When you add new file to the docs, please add config of sidebar menu in `/docs/vitepress/config/sidebar.ts`
- We have enabled [AutoCorrect](https://github.com/huacnlee/autocorrect) to improve copywriting, correct spaces, words, punctuations between CJK. If your PR encounter this kind of problems, please check your PR's check result and fix them.

### Custom title for code block

This feature will be offfical supported in the future.
as a workaround, you can use the following syntax:
```vue

<custom-title title="index.ts">

Your codeblock

</custom-title>

```

### Blog

If you want to write a blog, the following things you need to do
- Add new post under `docs/blog` or `docs-zh/blog` then just wirte the Markdown file.
- Add new item to `/docs/.vitepress/config/sidebar.ts` or `/docs-zh/.vitepress/config/sidebar.ts` `/blog/`.
