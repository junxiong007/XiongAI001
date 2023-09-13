# XiongAI001
铂熊AI金融科技，统计局爬虫1框架，突破解Ajax
使用driver做窗口自动化操作，
目前已经可以爬取完整数据并存储本地
有时间会再写完整的循环遍历框架  整合自动化

#from jqdata import *
%matplotlib inline 

from selenium import webdriver
import re
import requests
import time
import json
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import datetime
import warnings
import talib
import os
from numba import *
import numpy as np
import matplotlib as mpl
import statsmodels.api as sm
from bs4 import BeautifulSoup

warnings.filterwarnings('ignore')

plt.style.use('seaborn-whitegrid')
plt.rcParams['font.sans-serif'] = ['SimHei']  # 中文字体设置-黑体
plt.rcParams['axes.unicode_minus'] = False  # 解决保存图像是负号'-'显示为方块的问题

pd.set_option('display.width', 21250)
pd.set_option('display.max_columns', 21250)



from selenium import webdriver
url="https://data.stats.gov.cn/easyquery.htm?cn=A01&zb=A020914&sj=202308"
browser = webdriver.Chrome()
browser.get(url)
#browser.execute_script('window.scrollTo(0, document.body.scrollHeight)')
browser.find_element_by_xpath('//button[@id="details-button"]').click()
#browser.find_element_by_xpath('//a[@id="proceed-link"]').click()
browser.find_element_by_id('proceed-link').click()
data=browser.page_source
data


建议简单方法，使用pd.read_html()
进一步写出遍历框架和解析
融和
保存本地文件
df1.to_excel(r'C:\Users\熊俊\Desktop\铂熊AI数据库\统计局\统计局粗钢数据.xlsx')
整合框架
browser.quit()
