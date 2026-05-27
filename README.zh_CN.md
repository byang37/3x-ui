[English](/README.md) | [فارسی](/README.fa_IR.md) | [العربية](/README.ar_EG.md) | [中文](/README.zh_CN.md) | [Español](/README.es_ES.md) | [Русский](/README.ru_RU.md)

# 3X-UI Fork：流量倍率

这是 3X-UI 的个人 fork。本仓库跟随主仓库更新，README 只介绍相对主仓库额外实现的主要功能。

## 主要新增功能

### 入站流量倍率

本 fork 为入站节点新增了流量倍率功能。

- 在“添加入站”和“修改入站”表单中新增“流量倍率”输入框。
- 默认倍率为 `1`，保持主仓库原有流量统计行为。
- 当倍率设置为 `2` 时，入站上传和下载流量会按实际使用量的 2 倍统计。
- 入站下单个客户端的上传和下载流量也会按倍率统计。
- 客户端剩余流量和是否流量超限的判断使用加权后的流量值。
- 多节点/远程节点同步入站配置时会携带流量倍率。
- 订阅链接本身不变；订阅中展示的流量使用量和剩余流量基于加权后的客户端流量统计。

## 安装本 fork

```bash
bash <(curl -Ls https://raw.githubusercontent.com/byang37/3x-ui/master/install.sh)
```

## 主仓库引用

本 fork 基于以下主仓库：

[MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)
