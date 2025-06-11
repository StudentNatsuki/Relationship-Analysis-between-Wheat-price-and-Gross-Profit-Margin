{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "01ed12f6-d564-4261-ad62-1c4afa12eb8d",
   "metadata": {},
   "source": [
    "# 製パン・外食業の売上総利益率に対する政府小麦価格の影響分析\r\n",
    "\r\n",
    "## 🎯 分析目的\r\n",
    "政府の小麦売渡価格が、製パン・外食企業の売上総利益率に与える影響を、企業別パネルデータで分析（2015Q1～2025Q4）。\r\n",
    "\r\n",
    "## 📊 データ概要\r\n",
    "- 対象企業：製パン3社、外食3社（上場企業）\r\n",
    "- 出典：IRBank、農林水産省、総務省統計局\r\n",
    "- 変数：売上総利益率、CPI、小麦価格など\r\n",
    "\r\n",
    "## ⚙️ 分析手法\r\n",
    "- 固定効果付きパネル回帰分析（Driscoll-Kraay補正）\r\n",
    "- ラグ変数、スプライン、交差項を利用\r\n",
    "\r\n",
    "## 🧾 主な結果\r\n",
    "- 小麦価格は両業種で有意な影響（帰無仮説1を棄却）\r\n",
    "- 業種ごとに感応度が異なる（帰無仮説2も棄却）\r\n",
    "- 残差の正規性・独立性は概ね満たす\r\n",
    "\r\n",
    "## ▶️ 実行方法\r\n",
    "```bash\r\n",
    "pip install -r requirements.txt\r\n",
    "jupyter notebook code.ipynb\r\n"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "anaconda-panel-2023.05-py310",
   "language": "python",
   "name": "conda-env-anaconda-panel-2023.05-py310-py"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
