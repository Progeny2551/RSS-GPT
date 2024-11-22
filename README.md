# RSS-GPT

[![](https://img.shields.io/github/last-commit/yinan-c/RSS-GPT/main?label=feeds%20refreshed)](https://yinan-c.github.io/RSS-GPT/)
[![](https://img.shields.io/github/license/yinan-c/RSS-GPT)](https://github.com/yinan-c/RSS-GPT/blob/master/LICENSE)

If you need a web GUI to manage feeds better, check out my latest project: [RSSBrew](https://github.com/yinan-c/RSSBrew), a self-hosted RSS-GPT alternative with more features and customizability, built with Django.

## What is this?

[Configuration Guide](https://yinan-c.github.io/rss-gpt-manual-en.html) | [中文简介](README-zh.md) | [中文教程](https://yinan-c.github.io/rss-gpt-manual-zh.html)

Using GitHub Actions to run a simple Python script repeatedly: Calling OpenAI API to generate summaries for RSS feeds, and push the generated feeds to GitHub Pages. Easy to configure, no server needed.

### Features

- Use ChatGPT to summarize RSS feeds, and attach summaries to the original articles, support custom summary length and target language.
- Aggregate multiple RSS feeds into one, remove duplicate articles, subscribe with a single address.
- Add filters to your own personalized RSS feeds.
- Host your own RSS feeds on GitHub repo and GitHub Pages.

![](https://i.imgur.com/7darABv.jpg)

## Quick configuration guide

- Fork this repo
- Add Repository Secrets
    - U_NAME: your GitHub username
    - U_EMAIL: your GitHub email
    - WORK_TOKEN: your GitHub personal access token with `repo` and `workflow` scope, get it from [GitHub settings](https://github.com/settings/tokens/new)
    - OPENAI_API_KEY(OPTIONAL, only needed when using AI summarization feature): Get it from [OpenAI website](https://platform.openai.com/account/api-keys)
- Enable GitHub Pages in repo settings, choose deploy from branch, and set the directory to `/docs`.
- Configure your RSS feeds in config.ini

You can check out [here](https://yinan-c.github.io/rss-gpt-manual-en.html) for a more detailed configuration guide.

## ChangeLog and updates

- As OpenAI released a new version of `openai` package on Nov 06, 2023.  [More powerful models are coming](https://openai.com/blog/new-models-and-developer-products-announced-at-devday), the way to call API also changed. As a result, the old script will no longer work with the latest version installed, and needs to be updated. Otherwise, you will have to set `openai==0.27.8` in `requirements.txt` to use the old version.
- Check out the [CHANGELOG.md](CHANGELOG.md).

### Contributions are welcome!

- Feel free to submit issues and pull requests.

## Support this project

- If you find it helpful, please star this repo. Please also consider buying me a coffee to help maintain this project and cover the expenses of OpenAI API while hosting the feeds. I appreciate your support.

<a href="https://www.buymeacoffee.com/yinan" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## Example feeds being processed

These feeds on hosted in the [`docs/` subdirectory](https://github.com/yinan-c/RSS-GPT/tree/main/docs) in this repo as well as on my [GitHub Pages](https://yinan-c.github.io/RSS-GPT/). Feel free to subscribe in your favorite RSS reader.

I will consider hosting more feeds in the future. Email me or submit an issue if there are any questions using the script or any suggestions.

- https://hub.rss.direct/twitter/user/RICHG6789, https://hub.rss.direct/twitter/user/JLSQ_Ssexy, https://hub.rss.direct/twitter/user/wubu2019, https://hub.rss.direct/twitter/user/hanyan789, https://hub.rss.direct/twitter/user/NTphotographyNT, https://hub.rss.direct/twitter/user/vidacg2, https://hub.rss.direct/twitter/user/mangmang2001, https://hub.rss.direct/twitter/user/duyao_56789, https://hub.rss.direct/twitter/user/MMMenmentan, https://hub.rss.direct/twitter/user/nnian_, https://hub.rss.direct/twitter/media/yonaio6, https://hub.rss.direct/twitter/media/iFluffyPotato, https://hub.rss.direct/twitter/media/luobao1221, https://hub.rss.direct/twitter/media/hailingKH, https://hub.rss.direct/twitter/media/Adaydream617, https://hub.rss.direct/twitter/media/azhu1997_, https://hub.rss.direct/twitter/user/wyysmg, https://hub.rss.direct/twitter/media/0721KaiKinSyou, https://hub.rss.direct/twitter/media/xia0kong25, https://hub.rss.direct/twitter/media/chunmomo0127, https://hub.rss.direct/twitter/user/azhu1997_, https://hub.rss.direct/twitter/media/Jim_Sumire, https://hub.rss.direct/twitter/media/e_bi_maru, https://hub.rss.direct/twitter/media/yimiao1226, https://hub.rss.direct/twitter/media/XianYueZzz, https://hub.rss.direct/twitter/media/luorenlei, https://hub.rss.direct/twitter/media/Eririchyan, https://hub.rss.direct/twitter/media/jelly58207000, https://hub.rss.direct/twitter/media/HEROICAGE2, https://hub.rss.direct/twitter/media/xiaolinjiang555, https://hub.rss.direct/twitter/media/Sanshiya_, https://hub.rss.direct/twitter/media/sakuracyan_, https://hub.rss.direct/twitter/user/mizhu9418, https://hub.rss.direct/twitter/media/lingchuanqian, https://hub.rss.direct/twitter/media/Cutezzz6, https://hub.rss.direct/twitter/media/jingxiaogui, https://hub.rss.direct/twitter/media/SpicygumL, https://hub.rss.direct/twitter/media/chenlun_cat2, https://hub.rss.direct/twitter/media/fairrrrrr777, https://hub.rss.direct/twitter/user/mrjpzy, https://hub.rss.direct/twitter/media/NanaModeltt, https://hub.rss.direct/twitter/media/tnalice51, https://hub.rss.direct/twitter/media/MixMico3, https://hub.rss.direct/twitter/media/taozi6901, https://hub.rss.direct/twitter/user/caomei233, https://hub.rss.direct/twitter/media/saosao6677, https://hub.rss.direct/twitter/media/HongKong_Doll, https://hub.rss.direct/twitter/user/caicaizi935, https://hub.rss.direct/twitter/media/mikansu1, https://hub.rss.direct/twitter/user/JLSQ_Ssexy, https://hub.rss.direct/twitter/user/luchusmart, https://hub.rss.direct/twitter/user/karynaura59016, https://hub.rss.direct/twitter/user/jessicawic20193, https://hub.rss.direct/twitter/media/nu0mijiang, https://hub.rss.direct/twitter/media/misswang9296 -> https://Progeny2551.github.io/RSS-GPT/twitter-1.xml
- https://hub.rss.direct/telegram/channel/meitutu, https://hub.rss.direct/telegram/channel/pengyxxxxtg, https://hub.rss.direct/telegram/channel/botmzt, https://hub.rss.direct/telegram/channel/baisi, https://hub.rss.direct/telegram/channel/a7tscc, https://hub.rss.direct/telegram/channel/ziyuanjiatvv, https://hub.rss.direct/telegram/channel/MeiTuKu, https://hub.rss.direct/telegram/channel/xrwfc, https://hub.rss.direct/telegram/channel/ek777777, https://hub.rss.direct/telegram/channel/shudong7, https://hub.rss.direct/telegram/channel/yunpanshare, https://hub.rss.direct/telegram/channel/alyp_TV, https://hub.rss.direct/telegram/channel/XiangxiuNB, https://hub.rss.direct/telegram/channel/hdhhd21, https://hub.rss.direct/telegram/channel/shareAliyun, https://hub.rss.direct/telegram/channel/Q66Share, https://hub.rss.direct/telegram/channel/Aliyun_4K_Movies, https://hub.rss.direct/telegram/channel/dianying4K, https://hub.rss.direct/telegram/channel/yunpanpan -> https://Progeny2551.github.io/RSS-GPT/telegram-1.xml
- https://hub.rss.direct/pornhub/search/%E9%9C%B2%E5%87%BA, https://hub.rss.direct/pornhub/search/%E7%BE%A4p, https://hub.rss.direct/pornhub/model/andmlove, https://hub.rss.direct/pornhub/search/%E6%88%B7%E5%A4%96%E3%80%81%E9%87%8E%E5%A4%96%E3%80%81%E9%9D%92%E5%A5%B8, https://hub.rss.direct/pornhub/search/%E6%97%A5%E6%9C%AC, https://hub.rss.direct/pornhub/model/twtutu, https://hub.rss.direct/pornhub/model/loliiiiipop99, https://hub.rss.direct/pornhub/model/Naimi%20Naimi%20, https://hub.rss.direct/pornhub/model/babeneso, https://hub.rss.direct/pornhub/model/Layla%20Ray%20, https://hub.rss.direct/pornhub/model/SSR%20Peach, https://hub.rss.direct/pornhub/model/Qiobnxingcaiii, https://hub.rss.direct/pornhub/model/thelittlejuicer, https://hub.rss.direct/pornhub/model/HongKongDoll, https://hub.rss.direct/pornhub/model/Sweetie%20Fox, https://hub.rss.direct/pornhub/model/BunnyMiffy, https://hub.rss.direct/pornhub/model/daisybabytw, https://hub.rss.direct/pornhub/model/Nuomibaby, https://hub.rss.direct/pornhub/model/Vita%20Won, https://hub.rss.direct/pornhub/model/nan12138, https://hub.rss.direct/pornhub/model/el19870305, https://hub.rss.direct/pornhub/model/wanrous, https://hub.rss.direct/pornhub/model/fortunecutie, https://hub.rss.direct/pornhub/model/hubuyao718, https://hub.rss.direct/pornhub/model/TLMS_SVJ, https://hub.rss.direct/pornhub/search/Mr%20Bunny, https://hub.rss.direct/pornhub/model/CandyKissVip, https://hub.rss.direct/pornhub/model/slutsweetheart, https://hub.rss.direct/pornhub/model/SakuraCandy, https://hub.rss.direct/pornhub/search/Melody%20Marks, https://hub.rss.direct/pornhub/search/Swag.Live, https://hub.rss.direct/pornhub/model/Nana_taipei, https://hub.rss.direct/pornhub/search/%E5%9B%BD%E4%BA%A7, https://hub.rss.direct/pornhub/model/CNstepmom, https://hub.rss.direct/pornhub/model/404HotFound, https://hub.rss.direct/pornhub/model/Chinese%20Bunny, https://hub.rss.direct/pornhub/model/shyblanche, https://hub.rss.direct/pornhub/model/mysaaat -> https://Progeny2551.github.io/RSS-GPT/pornhub-1.xml
