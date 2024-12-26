- 添加更多列
    - `public/css/lrr.css`
    - `public/js/index.js`
    - `public/js/index_datatables.js`
    - `templates/index.html.tt2`
- 添加评分及评论插件，右键档案使用
    - `lib/LANraragi/Plugin/Metadata/Comment.pm`
      - 新出的`Summary`字段应该指的是自带的元数据，那就与此字段不冲突
    - `lib/LANraragi/Plugin/Metadata/Rating.pm`
      - 有人在进行类似的工作
- 略微调整EHentai插件搜索逻辑
    - `lib/LANraragi/Plugin/Metadata/EHentai.pm`
- 添加插件
    - [为缺少source标签的档案添加Ehentai元数据](https://github.com/chu-shen/LANraragi-scripts#%E4%B8%BA%E7%BC%BA%E5%B0%91source%E6%A0%87%E7%AD%BE%E7%9A%84%E6%A1%A3%E6%A1%88%E6%B7%BB%E5%8A%A0ehentai%E5%85%83%E6%95%B0%E6%8D%AE)：`lib/LANraragi/Plugin/Scripts/addEhentaiMetadata.pm`
    - 根据档案名查找重复档案并保存至`DuplicateArchives`分类：`lib/LANraragi/Plugin/Scripts/DuplicateFinder.pm`


[<img src="https://img.shields.io/docker/pulls/difegue/lanraragi.svg">](https://hub.docker.com/r/difegue/lanraragi/)
[<img src="https://img.shields.io/github/downloads/difegue/lanraragi/total.svg">](https://github.com/Difegue/LANraragi/releases)
[<img src="https://img.shields.io/github/release/difegue/lanraragi.svg?label=latest%20release">](https://github.com/Difegue/LANraragi/releases/latest)
[<img src="https://img.shields.io/homebrew/v/lanraragi.svg">](https://formulae.brew.sh/formula/lanraragi)
[<img src="https://img.shields.io/website/https/lrr.tvc-16.science.svg?label=demo%20website&up_message=online">](https://lrr.tvc-16.science/)
[<img src="https://github.com/Difegue/LANraragi/actions/workflows/push-continuous-integration.yml/badge.svg">](https://github.com/Difegue/LANraragi/actions)
[<img src="https://img.shields.io/discord/612709831744290847">](https://discord.gg/aRQxtbg)


<img src="public/favicon.ico" width="128">  
  
LANraragi
===========

Open source server for archival of comics/manga, running on Mojolicious + Redis.

#### 💬 Talk with other fellow LANraragi Users on [Discord](https://discord.gg/aRQxtbg) or [GitHub Discussions](https://github.com/Difegue/LANraragi/discussions)  

####  [📄 Documentation](https://sugoi.gitbook.io/lanraragi/v/dev) | [⏬ Download](https://github.com/Difegue/LANraragi/releases/latest) | [🎞 Demo](https://lrr.tvc-16.science) | [🪟🌃 Windows Nightlies](https://nightly.link/Difegue/LANraragi/workflows/push-continous-delivery/dev) | [💵 Sponsor Development](https://ko-fi.com/T6T2UP5N)  

## Screenshots  
 
|Main Page, Thumbnail View | Main Page, List View |
|---|---|
| [![archive_thumb](./tools/_screenshots/archive_thumb.png)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/archive_thumb.png) | [![archive_list](./tools/_screenshots/archive_list.png)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/archive_list.png) |

|Archive Reader | Reader with overlay |
|---|---|
| [![reader](./tools/_screenshots/reader.jpg)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/reader.jpg) | [![reader_overlay](./tools/_screenshots/reader_overlay.jpg)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/reader_overlay.jpg) |


|Configuration | Plugin Configuration |
|---|---|
| [![cfg](./tools/_screenshots/cfg.png)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/cfg.png) | [![cfg_plugin](./tools/_screenshots/cfg_plugin.png)](https://raw.githubusercontent.com/Difegue/LANraragi/dev/tools/_screenshots/cfg_plugin.png) |

## Features  

* Stores your comics in archive format. (zip/rar/targz/lzma/7z/xz/cbz/cbr/pdf supported, barebones support for epub)  

* Read archives directly from your web browser: the server reads from within compressed files using temporary folders.

* Read your archives in dedicated reader software using the built-in OPDS Catalog (now with PSE support!)

* Use the Client API to interact with LANraragi from other programs (Available for [many platforms!](https://sugoi.gitbook.io/lanraragi/v/dev/advanced-usage/external-readers))

* Two different user interfaces : compact archive list with thumbnails-on-hover, or thumbnail view.

* Choose from 5 preinstalled responsive library styles, or add your own with CSS.  

* Full Tag support with Namespaces: Add your own or import them from other sources using Plugins.  

* Store archives in either arbitary or dynamic Categories to sort your Library easily

* Import metadata using Plugins automatically when archives are added to LANraragi.

* Download archives from the Internet directly to the server, while using the aforementioned automatic metadata import

* Backup your database as JSON to carry your tags over to another LANraragi instance.

## Make a PR, get stickers™  

Merged PRs to this repo(or $5+ donations) are eligible to get a dumb sticker pack [shipped on the house.](https://forms.office.com/Pages/ResponsePage.aspx?id=DQSIkWdsW0yxEjajBLZtrQAAAAAAAAAAAAN__osxt25URTdTUTVBVFRCTjlYWFJLMlEzRTJPUEhEVy4u)  
