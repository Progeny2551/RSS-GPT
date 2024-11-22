# RSS-GPT

[![](https://img.shields.io/github/last-commit/yinan-c/RSS-GPT/main?label=feeds%20refreshed)](https://yinan-c.github.io/RSS-GPT/)
[![](https://img.shields.io/github/license/yinan-c/RSS-GPT)](https://github.com/yinan-c/RSS-GPT/blob/master/LICENSE)

如果想要一个网页端 GUI 来更好地管理 feeds，请关注我的最新项目：[RSSBrew](https://github.com/yinan-c/RSSBrew)，一个开源自托管的 RSS-GPT 替代方案，在过滤，自定义 prompt 等方面更加强大。

## 这是什么？

[中文介绍](https://yinan-c.github.io/rss-gpt.html) | [中文教程](https://yinan-c.github.io/rss-gpt-manual-zh.html) | [README](README.md)

使用 GitHub workflow 自动运行一个简单的 Python 脚本，调用 OpenAI API 为 RSS 订阅源生成摘要，然后将新生成的 RSS 订阅源推送到 GitHub Pages。配置简单快速，无需服务器。

### 功能及示例

- 使用 ChatGPT 来总结 RSS 订阅源, 生成关键词，摘要附在原文前面，支持自定义摘要长度，自定义语言。
- 聚合多个 RSS 订阅源，去除重复文章，用单一地址订阅。
- 为 RSS 订阅源添加基于标题，内容，URL 的关键词过滤器。
- 在 GitHub 仓库和 GitHub Pages 上自托管 RSS 订阅源。

![](https://i.imgur.com/7darABv.jpg)

## 快速部署

- Fork 这个仓库中
- 添加仓库 Secrets
    - U_NAME: 你的 GitHub 用户名
    - U_EMAIL: 你的 GitHub 邮箱
    - WORK_TOKEN: 你的 GitHub 个人访问令牌, 需要有 `repo` 和 `workflow` 权限。在 [GitHub 设置](https://github.com/settings/tokens/new)获取
    - OPENAI_API_KEY(可不填, 只有在使用 AI 摘要功能时需要): 你的 OpenAI API 密钥, 在 [OPENAI 网站](https://platform.openai.com/account/api-keys)获取
- 在仓库设置中启用 GitHub Pages， 选择 deploy from branch，设置目录为 `/docs`.
- 在 `config.ini` 中配置你的RSS订阅源

也可以参考更详细的[中文教程](https://yinan-c.github.io/rss-gpt-manual-zh.html)。

## 脚本的更新

- 由于 OpenAI 在 2023-11-06 发布了新版本的 `openai` 包，[新版本包含了更强大的模型](https://openai.com/blog/new-models-and-developer-products-announced-at-devday)，调用 API 的方式也发生了变化。因此，旧版本的脚本将无法使用最新版本的 `openai` 包，需要更新。否则，你可以在 `requirements.txt` 中设置 `openai==0.27.8` 来使用旧版本。
- 查看 [CHANGELOG-zh.md](CHANGELOG-zh.md) 获取其他最新的更新日志。

### 欢迎贡献!

- 欢迎提交 issue 和 pull request。

## 分享几条本项目处理后的 RSS 订阅源

我自己用此脚本总结的一些 RSS订阅源托管在本项目的[`docs/`子目录](https://github.com/yinan-c/RSS-GPT/tree/main/docs)中以及我的 [GitHub Pages](https://yinan-c.github.io/RSS-GPT/)上找到。欢迎在任何 RSS 阅读器中订阅。

如果有任何问题或有关于 RSS feeds 的建议，欢迎邮件联系我。

如果你觉得本项目有帮助，欢迎 star。也可以考虑捐赠以支持我继续维护本项目以及 cover OpenAI API 的支出。感谢支持。

<a href="https://www.buymeacoffee.com/yinan" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

- https://hub.rss.direct/twitter/user/RICHG6789, https://hub.rss.direct/twitter/user/JLSQ_Ssexy, https://hub.rss.direct/twitter/user/wubu2019, https://hub.rss.direct/twitter/user/hanyan789, https://hub.rss.direct/twitter/user/NTphotographyNT, https://hub.rss.direct/twitter/user/vidacg2, https://hub.rss.direct/twitter/user/mangmang2001, https://hub.rss.direct/twitter/user/duyao_56789, https://hub.rss.direct/twitter/user/MMMenmentan, https://hub.rss.direct/twitter/user/nnian_, https://hub.rss.direct/twitter/user/yonaio6, https://hub.rss.direct/twitter/user/iFluffyPotato, https://hub.rss.direct/twitter/user/luobao1221, https://hub.rss.direct/twitter/user/hailingKH, https://hub.rss.direct/twitter/user/Adaydream617, https://hub.rss.direct/twitter/user/wyysmg, https://hub.rss.direct/twitter/user/0721KaiKinSyou, https://hub.rss.direct/twitter/user/xia0kong25, https://hub.rss.direct/twitter/user/chunmomo0127 -> https://Progeny2551.github.io/RSS-GPT/twitter-1.xml
- https://hub.rss.direct/twitter/user/azhu1997_, https://hub.rss.direct/twitter/user/Jim_Sumire, https://hub.rss.direct/twitter/user/e_bi_maru, https://hub.rss.direct/twitter/user/yimiao1226, https://hub.rss.direct/twitter/user/XianYueZzz, https://hub.rss.direct/twitter/user/luorenlei, https://hub.rss.direct/twitter/user/Eririchyan, https://hub.rss.direct/twitter/user/jelly58207000, https://hub.rss.direct/twitter/user/HEROICAGE2, https://hub.rss.direct/twitter/user/xiaolinjiang555, https://hub.rss.direct/twitter/user/Sanshiya_, https://hub.rss.direct/twitter/user/sakuracyan_, https://hub.rss.direct/twitter/user/mizhu9418, https://hub.rss.direct/twitter/user/lingchuanqian, https://hub.rss.direct/twitter/user/Cutezzz6, https://hub.rss.direct/twitter/user/jingxiaogui, https://hub.rss.direct/twitter/user/SpicygumL, https://hub.rss.direct/twitter/user/chenlun_cat2, https://hub.rss.direct/twitter/user/fairrrrrr777, https://hub.rss.direct/twitter/user/mrjpzy -> https://Progeny2551.github.io/RSS-GPT/twitter-2.xml
- https://hub.rss.direct/twitter/user/NanaModeltt, https://hub.rss.direct/twitter/user/tnalice51, https://hub.rss.direct/twitter/user/MixMico3, https://hub.rss.direct/twitter/user/taozi6901, https://hub.rss.direct/twitter/user/caomei233, https://hub.rss.direct/twitter/user/saosao6677, https://hub.rss.direct/twitter/user/HongKong_Doll, https://hub.rss.direct/twitter/user/caicaizi935, https://hub.rss.direct/twitter/user/mikansu1, https://hub.rss.direct/twitter/user/luchusmart, https://hub.rss.direct/twitter/user/karynaura59016, https://hub.rss.direct/twitter/user/jessicawic20193, https://hub.rss.direct/twitter/user/nu0mijiang, https://hub.rss.direct/twitter/user/misswang9296 -> https://Progeny2551.github.io/RSS-GPT/twitter-3.xml
- https://hub.rss.direct/telegram/channel/yunpanshare, https://hub.rss.direct/telegram/channel/hdhhd21, https://hub.rss.direct/telegram/channel/XiangxiuNB, https://hub.rss.direct/telegram/channel/alyp_TV, https://www.ziyuanhui.cc/feed, https://hub.rss.direct/telegram/channel/yunpanpan, https://hub.rss.direct/telegram/channel/shareAliyun, https://hub.rss.direct/telegram/channel/Aliyun_4K_Movies, https://hub.rss.direct/telegram/channel/Q66Share, https://hub.rss.direct/telegram/channel/dianying4K -> https://Progeny2551.github.io/RSS-GPT/telegram-1.xml
- https://hub.rss.direct/telegram/channel/meitutu, https://hub.rss.direct/telegram/channel/pengyxxxxtg, https://hub.rss.direct/telegram/channel/botmzt, https://hub.rss.direct/telegram/channel/baisi, https://hub.rss.direct/telegram/channel/a7tscc, https://hub.rss.direct/telegram/channel/ziyuanjiatvv, https://hub.rss.direct/telegram/channel/MeiTuKu, https://hub.rss.direct/telegram/channel/xrwfc, https://hub.rss.direct/telegram/channel/ek777777, https://hub.rss.direct/telegram/channel/shudong7 -> https://Progeny2551.github.io/RSS-GPT/telegram-2.xml
- https://hub.rss.direct/pornhub/search/%E9%9C%B2%E5%87%BA, https://hub.rss.direct/pornhub/search/%E7%BE%A4p, https://hub.rss.direct/pornhub/search/%E6%88%B7%E5%A4%96%E3%80%81%E9%87%8E%E5%A4%96%E3%80%81%E9%9D%92%E5%A5%B8, https://hub.rss.direct/pornhub/search/%E6%97%A5%E6%9C%AC, https://hub.rss.direct/pornhub/search/Mr%20Bunny, https://hub.rss.direct/pornhub/search/Melody%20Marks, https://hub.rss.direct/pornhub/search/Swag.Live, https://hub.rss.direct/pornhub/search/%E5%9B%BD%E4%BA%A7 -> https://Progeny2551.github.io/RSS-GPT/pornhub-search.xml
- https://hub.rss.direct/pornhub/model/andmlove, https://hub.rss.direct/pornhub/model/twtutu, https://hub.rss.direct/pornhub/model/loliiiiipop99, https://hub.rss.direct/pornhub/model/Naimi%20Naimi%20, https://hub.rss.direct/pornhub/model/babeneso, https://hub.rss.direct/pornhub/model/Layla%20Ray%20, https://hub.rss.direct/pornhub/model/SSR%20Peach, https://hub.rss.direct/pornhub/model/Qiobnxingcaiii, https://hub.rss.direct/pornhub/model/thelittlejuicer, https://hub.rss.direct/pornhub/model/HongKongDoll, https://hub.rss.direct/pornhub/model/Sweetie%20Fox, https://hub.rss.direct/pornhub/model/BunnyMiffy, https://hub.rss.direct/pornhub/model/daisybabytw, https://hub.rss.direct/pornhub/model/Nuomibaby, https://hub.rss.direct/pornhub/model/Vita%20Won -> https://Progeny2551.github.io/RSS-GPT/pornhub-porn-1.xml
- https://hub.rss.direct/pornhub/model/nan12138, https://hub.rss.direct/pornhub/model/el19870305, https://hub.rss.direct/pornhub/model/wanrous, https://hub.rss.direct/pornhub/model/fortunecutie, https://hub.rss.direct/pornhub/model/hubuyao718, https://hub.rss.direct/pornhub/model/TLMS_SVJ, https://hub.rss.direct/pornhub/model/CandyKissVip, https://hub.rss.direct/pornhub/model/slutsweetheart, https://hub.rss.direct/pornhub/model/SakuraCandy, https://hub.rss.direct/pornhub/model/Nana_taipei, https://hub.rss.direct/pornhub/model/CNstepmom, https://hub.rss.direct/pornhub/model/404HotFound, https://hub.rss.direct/pornhub/model/Chinese%20Bunny, https://hub.rss.direct/pornhub/model/shyblanche, https://hub.rss.direct/pornhub/model/mysaaat -> https://Progeny2551.github.io/RSS-GPT/pornhub-porn-2.xml
