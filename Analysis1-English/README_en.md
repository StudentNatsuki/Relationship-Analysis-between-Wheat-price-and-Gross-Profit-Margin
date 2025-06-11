{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "8a916fc6-ae9d-4bad-9238-022f9fc98575",
   "metadata": {},
   "source": [
    "# Gross Profit Margin Panel Regression (Japan: Bakery & Restaurant)\n",
    "\n",
    "## 📌 Objective\n",
    "Analyze how government wheat prices impact gross profit margins using firm-level quarterly panel data (2015–2025), comparing bakery vs. restaurant industries.\n",
    "\n",
    "## 📊 Data\n",
    "- Companies: 3 bakery, 3 restaurant firms\n",
    "- Source: IRBank, MAFF, Statistics Bureau of Japan\n",
    "- Period: 2015Q1–2025Q4\n",
    "\n",
    "## 🔧 Methods\n",
    "- Fixed-effects panel regression (`PanelOLS`)\n",
    "- Lagged variables, spline components, interaction terms\n",
    "- Driscoll-Kraay robust standard errors\n",
    "\n",
    "## 🧾 Key Findings\n",
    "- Government wheat prices significantly affect margins\n",
    "- Sensitivity differs by industry\n",
    "- Residuals pass normality & independence checks\n",
    "\n",
    "## ▶️ How to Run\n",
    "```bash\n",
    "pip install -r requirements.txt\n",
    "jupyter notebook code.ipynb\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "135d989a-cdda-4d36-9201-bd50a5d79c37",
   "metadata": {},
   "outputs": [],
   "source": []
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
