# 旧仓库维护说明 / Legacy repository instructions

## 仓库身份 / Repository identity

This checkout is `thomas9190/guanlinli.github.io`, the **legacy website repository**.
It preserves old links at https://thomas9190.github.io/guanlinli.github.io/ and redirects HTML pages to the current website.

- Current website: https://thomas9190.github.io/
- Active source repository: https://github.com/thomas9190/thomas9190.github.io
- Active local checkout on this computer: `D:\Python project\thomas9190.github.io`

## 后续修改应在哪里完成 / Where to make changes

For routine website work (profile, publications, posts, images, styling, navigation, SEO, or new downloadable files), switch to the active repository above and follow its own instructions before editing. Do this even when the initial working directory is this legacy checkout. Verify the destination repository's Git remote before making changes. If the active checkout is missing, locate or clone the active repository rather than treating this one as the current website source.

网站日常更新应在新仓库完成。本仓库只用于旧链接兼容；不要因为当前目录在这里，就把网站内容改到旧仓库。

## 本仓库的维护范围 / Maintenance scope here

- Maintain legacy redirects, compatibility for existing links, and these repository notices here.
- Keep this repository and GitHub Pages available so existing links continue to work.
- Preserve the legacy `baseurl: "/guanlinli.github.io"`, `legacy_redirect_url: "https://thomas9190.github.io"`, and redirect/canonical handling unless the task requires changing the migration setup.
- Static files such as PDFs are served directly from this repository; they do not use the HTML redirect. When a task calls for updating files behind old download links, synchronize the relevant files explicitly.
- Do not copy this legacy redirect configuration into the active website repository.

Direct user instructions to change the legacy repository take precedence over these default routing instructions.
