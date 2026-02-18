---
layout: ../../layouts/MarkdownPostLayout.astro
title: "反检测selenium代码"
pubDate: 2026-02-18
description: "使用selenium时的规避检测代码"
author: "KEee"
image:
  url: "https://docs.astro.build/assets/rose.webp"
  alt: "The Astro logo on a dark background with a pink glow."
tags: ["python","爬虫","selenium"]
---

# 使用现规避检测的完整代码
```
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
import time

def create_driver_with_stealth():
    """创建具有反检测功能的Chrome驱动"""
    options = Options()
    
    # 基础反检测设置
    options.add_argument('--disable-blink-features=AutomationControlled')
    options.add_experimental_option("excludeSwitches", ["enable-automation"])
    options.add_experimental_option('useAutomationExtension', False)
    
    # 窗口和性能设置
    options.add_argument("--no-sandbox")
    options.add_argument("--disable-dev-shm-usage")
    options.add_argument("--disable-setuid-sandbox")
    options.add_argument("--disable-web-security")
    options.add_argument("--allow-running-insecure-content")
    
    # 用户代理伪装
    options.add_argument("--user-agent=Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36")
    
    # 禁用自动化标志
    options.add_experimental_option("prefs", { 
        "profile.default_content_setting_values.notifications": 2,
        "profile.default_content_settings.popups": 0,
        "profile.managed_default_content_settings.images": 1
    })
    
    driver = webdriver.Chrome(options=options)
    
    # 执行脚本来隐藏webdriver属性
    driver.execute_script("Object.defineProperty(navigator, 'webdriver', {get: () => undefined});")
    
    return driver

# 创建带反检测功能的浏览器实例
browser = create_driver_with_stealth()
```
