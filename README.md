# 汉化补丁下载

[0.1.0 测试版下载](https://github.com/JasonWei512/Shantae-and-the-Seven-Sirens-Chinese-Retranslation-Project/releases/download/0.1.0/localization.pak.zip) | [国内镜像](http://github.strcpy.cn/JasonWei512/Shantae-and-the-Seven-Sirens-Chinese-Retranslation-Project/releases/download/0.1.0/localization.pak.zip)

解压后覆盖 ```游戏目录/data/localization.pak```。

通关后凭印象对着文本盲翻的，尚未润色，尚未在游戏内测试过。

# 概述

[![生成汉化补丁](https://github.com/JasonWei512/Shantae-and-the-Seven-Sirens-Chinese-Retranslation-Project/workflows/%E7%94%9F%E6%88%90%E6%B1%89%E5%8C%96%E8%A1%A5%E4%B8%81%E3%80%80%E3%80%80/badge.svg)](https://github.com/JasonWei512/Shantae-and-the-Seven-Sirens-Chinese-Retranslation-Project/actions?query=workflow%3A%E7%94%9F%E6%88%90%E6%B1%89%E5%8C%96%E8%A1%A5%E4%B8%81%E3%80%80%E3%80%80)

Shantae and the Seven Sirens 的中文机翻过于严重，计划重翻一遍。

To WayForward: A big part of Shantae and the Seven Sirens' Chinese translation looks like 
machine translation. And there're some garbled texts like 🖾 (maybe because of the Chinese font used). So I plan to retranslate it.

# 说明

游戏的文本位于 ```游戏目录/data/localization.pak``` 中。文件为二进制，每条文本以UTF8编码，之间用全零字节隔开。

文本对象中的各成员说明：
- Text：该条文本的内容
- OriginalText（可选）：英文原文文本
- StartAddress：这条文本的首个字节在 ```localization.pak``` 中的起始位置（从零开始数，用十进制表示）
- EndAddress：这条文本可用的最后一个字节的位置，即下一条文本首个字节的前两个字节的位置（为了让两条文本之间最少有一个零字节隔开，否则游戏中文本会出重复的Bug）
- MaxLength：这条文本以UTF8编码后允许的最大字节数（即：EndAddress - StartAddress + 1）