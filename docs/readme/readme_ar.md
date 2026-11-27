<br />
<img src="../../assets/images/logo-transparent.png" width="80"/>

### TanyunAPI - برمجية مفتوحة المصدر لاستكشاف واختبار واجهات API

[![Website](https://img.shields.io/badge/Website-Visit-blue)](https://github.com/CodeCoreLab/tanyun-api#readme)
[![Repo](https://img.shields.io/badge/Repository-GitHub-brightgreen)](https://github.com/CodeCoreLab/tanyun-api)

> عميل API سطح مكتب مفتوح المصدر ببنية معمارية تطوير ذاتي.

[English](../../readme.md)
| [Українська](./readme_ua.md)
| [Русский](./readme_ru.md)
| [Türkçe](./readme_tr.md)
| [Deutsch](./readme_de.md)
| [Français](./readme_fr.md)
| [Português (BR)](./readme_pt_br.md)
| [한국어](./readme_kr.md)
| [বাংলা](./readme_bn.md)
| [Español](./readme_es.md)
| [Italiano](./readme_it.md)
| [Română](./readme_ro.md)
| [Polski](./readme_pl.md)
| [简体中文](./readme_cn.md)
| [正體中文](./readme_zhtw.md)
| **العربية**
| [日本語](./readme_ja.md)
| [ქართული](./readme_ka.md)
| [Nederlands](./readme_nl.md)
| [فارسی](./readme_fa.md)
| [हिन्दी](./readme_hi.md)

TanyunAPI عميل API سطح مكتب مفتوح المصدر ببنية معمارية تطوير ذاتي، لـ HTTP / gRPC / GraphQL / WebSocket واختبارات التراجع للمجموعات.

يخزن TanyunAPI مجموعات API مباشرة في نظام الملفات المحلي كملفات نصية عادية.

Collaborate on collections with Git or any version control system.

TanyunAPI is offline-first and does not require cloud sync; data stays on your machine by default.

Repository: [CodeCoreLab/tanyun-api](https://github.com/CodeCoreLab/tanyun-api)

![tanyun](../../assets/images/landing-2-dark.png#gh-light-mode-only)
![tanyun](../../assets/images/landing-2-light.png#gh-dark-mode-only) <br /><br />

## Table of Contents

- [Installation](#installation)
- [CLI](#cli)
- [Run with Docker](#run-with-docker)
- [Features](#features)
  - [Run across multiple platforms 🖥️](#run-across-multiple-platforms-%EF%B8%8F)
  - [Collaborate via Git 👩‍💻🧑‍💻](#collaborate-via-git-%E2%80%8D%E2%80%8D)
- [Important Links 📌](#important-links-)
- [Showcase 🎥](#showcase-)
- [Share Testimonials 📣](#share-testimonials-)
- [Publishing to New Package Managers](#publishing-to-new-package-managers)
- [Stay in touch 🌐](#stay-in-touch-)
- [Trademark](#trademark)
- [Contribute 👩‍💻🧑‍💻](#contribute-%E2%80%8D%E2%80%8D)
- [Authors](#authors)
- [License 📄](#license-)

## Installation

探云 API 可通过本仓库 Releases 获取桌面端构建产物（Mac / Windows / Linux），具体安装步骤见发布说明。

```sh
# 克隆源码本地开发
git clone https://github.com/CodeCoreLab/tanyun-api.git
cd tanyun-api
npm install
npm run dev
```

## CLI

The **CLI** lets you run your API collections from the command line, which is ideal for automated testing and CI/CD pipelines. Install it from npm using the package manager of your choice:

```sh
npm install -g @tanyun/cli
```

Navigate to the directory containing your collection and run it:

```sh
# Run every request in the collection
bru run

# Run a single request
bru run request.yml

# Run a folder against a specific environment
bru run folder --env Local
```

For the full command reference, see the CLI help (`tanyun --help`) and repository docs.

## Run with Docker

Official Docker images for the **CLI** let you run API collections in CI/CD pipelines and locally without installing Node.js or npm on the host. Build from `Dockerfile` in this repository; `alpine` and `debian` variants support `linux/amd64` and `linux/arm64`.

```sh
# 本地构建 CLI 镜像
docker build -f packages/bruno-cli/docker/images/alpine/Dockerfile -t tanyun-cli .

# 挂载当前目录运行集合
docker run -v "$(pwd):/collections" tanyun-cli run collections/
```

For Docker image build and CI examples, see `Dockerfile` and `.github/workflows` in this repository.

## Features

### Run across multiple platforms 🖥️

![tanyun](../../assets/images/run-anywhere.png) <br /><br />

### Collaborate via Git 👩‍💻🧑‍💻

Or any version control system of your choice

![tanyun](../../assets/images/version-control.png) <br /><br />

## Important Links 📌

- [Repository](https://github.com/CodeCoreLab/tanyun-api)
- [Releases](https://github.com/CodeCoreLab/tanyun-api/releases)

## Showcase 🎥


## Share Testimonials 📣

If TanyunAPI has helped you at work and your teams, please share feedback via [GitHub Issues](https://github.com/CodeCoreLab/tanyun-api/issues).

## Publishing to New Package Managers

Please see [here](../../publishing.md) for more information.

## Stay in touch 🌐


[Repository](https://github.com/CodeCoreLab/tanyun-api) <br />
[Discord](https://discord.com/invite/KgcZUncpjq) <br />
[Repository](https://github.com/CodeCoreLab/tanyun-api)

## Trademark

**Name**

`TanyunAPI` is a trademark held by [Anoop M D](https://www.helloanoop.com/)

**Logo**

The logo is sourced from [OpenMoji](https://openmoji.org/library/emoji-1F436/). License: CC [BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

## Contribute 👩‍💻🧑‍💻

I am happy that you are looking to improve TanyunAPI. Please check out the [contributing guide](../../contributing.md)

Even if you are not able to make contributions via code, please don't hesitate to file bugs and feature requests that needs to be implemented to solve your use case.

## Authors

<div align="center">
    <a href="https://github.com/CodeCoreLab/tanyun-api/graphs/contributors">
        <img src="https://contrib.rocks/image?repo=CodeCoreLab/tanyun-api" />
    </a>
</div>

## License 📄

[MIT](../../license.md)
