# waka-readme-stats 代码统计配置

name: Waka Readme

on:
  workflow_dispatch:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'

jobs:
  update-readme:
    name: Update README
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
          # 标签
          SHOW_TOTAL_CODE_TIME: False
          SHOW_PROFILE_VIEWS: False
          # GitHub 数据
          SHOW_SHORT_INFO: False
          # 提交统计
          SHOW_COMMIT: False
          # 一周提交统计
          SHOW_DAYS_OF_WEEK: False
          # 操作系统
          SHOW_OS: False
          # 项目
          SHOW_PROJECTS: False
          # 时区
          SHOW_TIMEZONE: False
          # 编辑器
          SHOW_EDITORS: False
          # 主要编写
          SHOW_LANGUAGE_PER_REPO: False
          # 时间线
          SHOW_LOC_CHART: False
          # 末尾更新日期
          SHOW_UPDATED_DATE: False
          # 语言
          LOCALE: en
