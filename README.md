
# Air Quality Analysis and Forecasting

Technologies : Python, Pandas, NumPy, Scikit-learn, Statsmodels, PyTorch


Ce projet vise à analyser et prévoir des indicateurs de qualité de l’air à partir du **Air Quality Dataset (UCI Machine Learning Repository)(https://archive.ics.uci.edu/dataset/360/air+quality)**.  
Le dataset contient environ **9 000 observations** issues de capteurs environnementaux mesurant plusieurs polluants atmosphériques (CO, NOx, benzène, etc.).

Les données ont été prétraitées avec **Python (Pandas, NumPy)** : nettoyage des valeurs invalides, interpolation linéaire des données manquantes et construction de variables temporelles (heure, jour, mois) ainsi que de variables retardées afin de capturer les dépendances temporelles.

Plusieurs approches de modélisation ont ensuite été comparées pour la prévision de séries temporelles environnementales :

- modèles statistiques : **ARMA / SARIMA / SARIMAX**
- modèles de machine learning : **Random Forest, Boosting, Bagging**
- réseaux de neurones : **MLP, LSTM, GRU**

Les performances ont été évaluées à l’aide des métriques **RMSE** et **MSE** sur un jeu de test (40 % des données).

Résultats principaux :

- **SARIMA : RMSE ≈ 30**
- **GRU : MSE ≈ 1500**

Les résultats montrent que les **modèles statistiques restent très performants sur des séries temporelles de taille modérée**, tandis que les modèles deep learning nécessitent généralement davantage de données pour surpasser les approches classiques.
