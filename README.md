# 使用 Python 绕过 CAPTCHA

[![Promo](https://github.com/bright-cn/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://www.bright.cn/)

本指南将介绍在 Python 中绕过 CAPTCHA 的顶级技术与最佳工具：

- [CAPTCHA：定义与类型](#captcha定义与类型)
- [文本型 CAPTCHA](#文本型-captcha)
- [图片型 CAPTCHA](#图片型-captcha)
- [音频型 CAPTCHA](#音频型-captcha)
- [拼图型 CAPTCHA](#拼图型-captcha)
- [是否可以使用 Python 自动化 CAPTCHA？](#是否可以使用-python-自动化-captcha)
- [评估 Python 的 CAPTCHA 绕过方案](#评估-python-的-captcha-绕过方案)
- [Python 中绕过 CAPTCHA：前 5 种方法](#python-中绕过-captcha前-5-种方法)
- [1. Web Unlocker 的 CAPTCHA Solver](#1-web-unlocker-的-captcha-solver)
- [2. 搭配 Stealth 插件的 Playwright Extra](#2-搭配-stealth-插件的-playwright-extra)
- [3. AntiCaptcha](#3-anticaptcha)
- [4. 使用 Stealth 库的 Selenium](#4-使用-stealth-库的-selenium)
- [5. 2Captcha](#5-2captcha)
- [最佳 Python CAPTCHA 解决方案](#最佳-python-captcha-解决方案)

## CAPTCHA：定义与类型

CAPTCHA（Completely Automated Public Turing test to tell Computers and Humans Apart）是一种用于区分人类用户与机器人的挑战。它要求执行对人类容易、对自动化软件困难的任务。

随着 AI 的发展，CAPTCHA 为保持有效性变得越来越复杂。

下面是当下最常见的 CAPTCHA 类型。

### 文本型 CAPTCHA

文本型 CAPTCHA 会展示一串扭曲的字母与数字，用户需识别并输入。虽然曾被广泛使用，但机器人对其的识别能力越来越强，因此其流行度有所下降。

### 图片型 CAPTCHA

图片型 CAPTCHA 要求用户在图片网格中选择特定对象，例如红绿灯、自行车或公交车。此类 CAPTCHA 的知名提供商是 [reCAPTCHA](https://www.google.com/recaptcha/about/)。

### 音频型 CAPTCHA

音频型 CAPTCHA 为视障用户提供可访问性选项。它提供一段失真的语音音频，用户需正确转写。

### 拼图型 CAPTCHA

拼图型 CAPTCHA 要求用户完成简单任务，例如将图片拖拽到正确位置或解答简单逻辑题。

![Puzzle-CAPTCHA-example](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Puzzle-CAPTCHA-example-1.png)

常见提供商包括 [AWS WAF CAPTCHA](https://docs.aws.amazon.com/waf/latest/developerguide/waf-captcha-and-challenge.html) 与 [hCaptcha](https://www.hcaptcha.com/)。

## 是否可以使用 Python 自动化 CAPTCHA？

CAPTCHA 天生就是让自动化变得困难，Python 中并不存在“一步到位”的简单方案。但可以从两条路径入手：

- 避免触发 CAPTCHA：在受控浏览器中模拟人类行为，使用更接近真实用户的指纹，从而降低触发 CAPTCHA 的概率。
- 使用解题服务：借助使用 AI、自动化工具或人工求解的付费服务自动解决 CAPTCHA。

要实现上述方法，您需要合适的 Python CAPTCHA 解决或绕过方案。

## 评估 Python 的 CAPTCHA 绕过方案

在比较市面上主流的 Python CAPTCHA 绕过/解决服务时，建议关注以下要素：

- 能力范围：方案提供的功能与特性
- 工具性质：开源或商用
- 稳定性（Uptime）：服务可用性保证
- 成功率：解决 CAPTCHA 的成功比例
- 绕过策略：是避免触发、直接解题，或两者兼有
- 支持的提供商：可处理的 CAPTCHA 提供商列表
- Trustpilot 评分：用户评价的平均分
- 定价：Python CAPTCHA 方案的费用

## Python 中绕过 CAPTCHA：前 5 种方法

下面基于上述标准，筛选并排序了 5 个在 Python 中绕过 CAPTCHA 的顶级方案。

### 1. Web Unlocker 的 CAPTCHA Solver

![Bright Data's CAPTCHA Solver page](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Bright-Datas-CAPTCHA-Solver-page-1024x493.png)

[CAPTCHA Solver](https://www.bright.cn/products/web-unlocker/captcha-solver) 是 Bright Data 推出的强大工具，可绕过多家提供商的 CAPTCHA。它通过模拟人类行为与浏览器指纹，并使用 AI 算法来解决挑战。

功能特性：

- IP 轮换：动态更换 IP 以避免检测
- 自动重试：通过自动重试确保请求成功
- JavaScript 渲染：处理需要执行 JS 的动态站点
- 全球覆盖：访问全球各地的本地化内容
- 高可扩展性：可处理大规模数据抓取
- 引荐来源头（Referrer）：模拟来自可信站点的流量
- Cookie 处理：通过管理 Cookie 预防封锁

作为 Web Unlocker 的一部分，CAPTCHA Solver 可与任意 HTTP 客户端或浏览器自动化工具配合使用（支持 Python 与其他编程语言）。选择它的理由包括：

- 99% 成功率：可靠的 CAPTCHA 绕过能力，接近满分的准确度
- 支持多种 CAPTCHA 类型：reCAPTCHA、hCaptcha、FunCaptcha、Cloudflare Turnstile、AWS WAF CAPTCHA 等
- 灵活的 API 集成：兼容任意 HTTP 客户端
- 透明定价：提供免费试用，之后 $3/CPM（每次请求 $0.003）

凭借 99.9% 的高可用性与先进的反封策略，Bright Data 能够保障合规、顺畅、不中断的网页抓取。

### 2. 搭配 Stealth 插件的 Playwright Extra

![Playwright stealth plugin](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Playwright-stealth-plugin-1024x442.png)

Playwright Extra 是对 Playwright 的增强版本，支持插件机制，从而实现更好的反检测能力。Python 版的 [playwright-stealth](https://pypi.org/project/playwright-stealth/) 插件有助于让自动化浏览器更像真人使用，降低被 CAPTCHA 与反爬系统识别的概率。

该方案受 [Puppeteer Extra Stealth 插件](/blog/how-tos/avoid-bot-detection-with-playwright-stealth) 启发，通过调整浏览器设置来模拟真实用户行为，帮助绕过 CAPTCHA 与机器人检测。可参考我们的教程：[如何使用 Playwright Stealth 避免机器人检测](/blog/how-tos/avoid-bot-detection-with-playwright-stealth)。

分步教程可见：[如何使用 Playwright 绕过 CAPTCHA](/blog/web-data/bypass-captchas-with-playwright)。

关键特性：

- 能力范围：完整的浏览器自动化、支持 JS 与 Python、反检测、E2E 测试、插件与调试工具
- 工具性质：开源
- 成功率：不定，取决于目标站点防护强度
- 绕过策略：用户行为仿真与真实指纹
- 支持的 CAPTCHA 类型：基础防爬类 CAPTCHA
- 定价：免费

Playwright Extra + Stealth 是开源领域中强有力的 CAPTCHA 避免与浏览器自动化组合。

### 3. AntiCaptcha

![Image of the AntiCaptcha service](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Image-of-the-AntiCaptcha-service-1-1024x478.png)

AntiCaptcha 自 2007 年起提供基于 API 的 CAPTCHA 解题服务，并支持浏览器插件集成，兼容 Selenium、Puppeteer 等自动化工具。

其 CAPTCHA 由人工解题，准确度较高。Python 用户可通过 [python-anticaptcha](https://pypi.org/project/python-anticaptcha/) 集成，但该库最近一次更新在 2022 年。无免费试用，且未披露官方成功率。

#### 关键特性：

- 能力范围：API 解题、浏览器插件集成、详细报表
- 工具性质：商用 API，支持 PHP、Python、Java、C#、JavaScript、Go、Ruby
- 稳定性：99.99%
- 成功率：未披露
- 绕过策略：人工解题
- 支持的 CAPTCHA 类型：图片 CAPTCHA、reCAPTCHA v2/v3、reCAPTCHA Enterprise、hCaptcha、GeeTest、Arkose Labs、Cloudflare Turnstile
- Trustpilot 评分：4.8/5
- 定价：$0.50/CPM — $2/CPM

对于需要人工介入的复杂挑战，AntiCaptcha 是值得信赖的选择。

### 4. 使用 Stealth 库的 Selenium

![Selenium stealth library](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Selenium-stealth-library-1024x342.png)

Selenium 是广泛使用的浏览器自动化工具，适用于测试与抓取。它提供强大的 API 来模拟人类交互。但由于默认配置较为明显，常被反爬系统识别。

为此可使用 [selenium-stealth](https://pypi.org/project/selenium-stealth/) Python 包，优化 Chrome 设置以降低被检测概率，从而提升自动化成功率，尤其在涉及 CAPTCHA 的场景。

关键特性：

- 能力范围：完整浏览器自动化、反检测、支持 E2E 测试
- 工具性质：开源
- 成功率：取决于站点检测手段
- 绕过策略：用户仿真与真实指纹
- 支持的 CAPTCHA 类型：基础防爬类 CAPTCHA
- 定价：免费

Selenium Stealth 是在自动化交互时减少触发 CAPTCHA 的有效工具。

### 5. 2Captcha

![Image of the 2Captcha service](https://github.com/bright-cn/bypass-captcha-with-python/blob/main/images/Image-of-the-2Captcha-service-1024x493.png)

2Captcha 通过将挑战分发给人工解题者来实时求解，支持多种 CAPTCHA 类型，并提供多语言官方库，Python 通过 [2captcha-python](https://pypi.org/project/2captcha-python/) 集成。

注意事项：

- 无免费试用，测试需至少充值 $1
- 在 Trustpilot 上存在部分负面评价
- 未披露成功率与可用性

关键特性：

- 能力范围：人工解题 API
- 工具性质：面向 Python、PHP、Java、C++、C#、Go、Ruby 的付费 API
- 成功率与稳定性：未披露
- 绕过策略：人工解题
- 支持的 CAPTCHA 类型：reCAPTCHA、Cloudflare Turnstile、Amazon CAPTCHA、数学 CAPTCHA、音频 CAPTCHA 等
- Trustpilot 评分：4.0/5
- 定价：$0.50/CPM — $50/CPM

2Captcha 被广泛使用，但在购买前应考虑其缺乏免费试用与口碑不一的问题。

## 最佳 Python CAPTCHA 解决方案

下表汇总了各主流 Python CAPTCHA 方案的核心差异：

|     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 服务 | 功能特性 | 支持语言 | 稳定性 | 成功率 | 避免触发 CAPTCHA | 直接解题 | 评价分数 | 免费试用 | 定价 |
| Bright Data CAPTCHA Solver | 非常多 | 任意 | 99.9% | 99.9% | ✔️ | ✔️ | 4.5/5 | ✔️ | $3/CPM |
| Playwright Stealth | 很多 | Python、JavaScript | — | 未知 | ✔️ | ❌ | — | — | 免费 |
| AntiCaptcha | 较少 | Python、PHP、Java、C#、JavaScript、Go、Ruby | 99.99% | 未披露 | ❌ | ✔️ | 4.8/5 | ❌ | $0.50/CPM — $2/CPM |
| Selenium Stealth | 很多 | Python | — | 未知 | ✔️ | ❌ | — | — | 免费 |
| 2Captcha | 几乎没有 | Python、PHP、Java、C++、C#、Go、Ruby | 未披露 | 未披露 | ❌ | ✔️ | 4.0/5 | ❌ | $0.50/CPM — $50/CPM |

## 结论

正如本指南所示，[Web Unlocker](https://www.bright.cn/products/web-unlocker) 是从任意网页获取无 CAPTCHA 的 HTML 的优秀解锁 API。该抓取 API 处理浏览器指纹、提供自动重试，并结合代理在每次请求时轮换出口 IP，同时为您解决 CAPTCHA。

立即注册，开启免费试用。
