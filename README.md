
**Project Name**: Predicting Daily Asset Returns with Deep Learning

**Author**: Michael Honaker

**Description**:

I created this project to explore the application of deep learning and recurrent neural networks as an asset investment strategy.

A large stock market dataset is publicly available on Kaggle (link)[https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs] which contains daily price and volume data for all US-based stocks and ETFs trading on NYSE, NASDAQ, and NYSE MKT.

The objective is to use the available data for any particular asset to train a recurrent neural network that can predict future returns. Moreover, this is a regression task where the input is the price and volume data of the asset for the past N days, and the target is the log return of the asset for the next day. The log return was chosen for a handul of reasons, some of which include time additivity and the normality assumption in modeling.

For model evaluation, I set up a simulation to iteratively predict log returns for each day in the test set, shifting the input by one day at each step to predict on the most up-to-date, accurate data. The predicted log returns are used in a Fractional Kelly Criterion-based position strategy on the asset prior to market open. Capital growth is computed for each day based on both the predictive fractional asset allocation strategy as well as with a naive buy-and-hold style allocation.

To view the code and results, you can open the Jupyter Notebook committed in this repository, or you can follow this (link)[https://colab.research.google.com/drive/1KodMIZAwviWLI6sPxXipOqOw9B8gAvxY?usp=sharing] to my live Google Colab.
