# Permutation-Entropy

Permutation Entropy (PE) is a robust nonparametric technique, which relies upon the notions of entropy and symbolic dynamics, provides a basis for the analysis of nonlinear time series and permits a way of describing the underlying dynamic state of the system in probability distribution form. It has been applied extensively across various fields and generalized to higher-dimensional data structures to analyze image texture (e.g., [Azami *et al.* (2019))](https://doi.org/10.1016/j.image.2019.04.013). PE was introduced by Christoph Bandt and Bernd Pompe in their 2002 seminal paper ["Permutation Entropy: A Natural Complexity Measure for Time Series"](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.88.174102) as a as a metric that takes time causality into account by comparing time related observations–ordinal patterns in a time series. The process of simbolizing a time series is based on the method of delay time coordinates introduced in [Takens (1981)](https://link.springer.com/chapter/10.1007/BFb0091924). In economics, the notion of PE was introduced by [Matilla-García and Ruiz Marín (2008)](https://doi.org/10.1016/j.jeconom.2007.12.005) to develope a new nonparametric test for independence.

Unlike econometric reductionist models (e.g., moving average-autoregressive ARMA representations and ARIMA models), PE can be applied to any type of time series (regular, chaotic, noisy, experimental or reality based) and is characterized by its conceptual simplicity and computational speed. It has been used for anomaly detection (see e.g. [Garland *et al.* (2018)](https://www.mdpi.com/1099-4300/20/12/931) and [Juarez Garcia *et al.* (2022))](https://www.ece.ufl.edu/wp-content/uploads/sites/63/2022/05/Detecting-High-Risk-Anomalies-in-Aircraft-Dynamics-Through-Entropic-Analysis-of-Time-Series-Data.pdf) and generalized to two-dimensional data such as images (e.g., [Ribeiro *et al.* (2012)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0040689)). Other applications of PE in the economics literature are ["Structural breaks and the time-varying levels of weak-form efficiency in crude oil markets: Evidence from the Hurst exponent and Shannon entropy methods](https://doi.org/10.1016/j.inteco.2014.10.001) by Mensi et al., and ["Permutation Entropy and Information Recovery in Nonlinear Dynamic Economic Time Series"](https://doi.org/10.3390/econometrics7010010) by Henry and Judge.

In our [study](https://doi.org/10.3390/econometrics7010010), published in the _Econometrics_ journal, my coauthor [George Judge](https://are.berkeley.edu/users/george-g-judge) and I estimated the PE using a rolling-window approach and the high-frequency Dow Jones Industrial Average (DJIA) time-series over the period 1901-2016 to gain deeper insights into the dynamics of this complex economic system. Our method uncovers hidden patterns by analyzing the ordinal relationships between individual values within the non-linear time-series and reveals the underlying probability distribution of these patterns. This, in turn, allowed us to quantify the degree of complexity inherent in the DJIA system's behavior. 

The following figure displays the normalized PE rolling estimates series for an embedding dimension 𝐷=5 of daily DJIA nominal returns. This result provides some insight into the broad trends in the U.S. fiscal policy. The turmoil in the U.S. stock market and collapse of stock prices during the Depression at the end of 1929 is apparent in the figure. It is important to note an increase in the temporary uncertainty (rise in PE and complexity) and the steady demand for manufactured products during World War I. The PE over time reveals important volatility that corresponds to U.S. fiscal policy. The sharp increase in PE or equivalently the decrease in informational content of the series during the 1980s may be linked to deregulation during the Reagan administration. These diagnostics suggest potential questions that require rigorous analysis in order to posit a causal link. However, the value of examining the partitioned sequencing within the DJIA continuously compounded return series is immediately apparent in suggesting worthwhile questions for economic analysis.

![pe](https://github.com/mhenryo/Permutation-Entropy/assets/8084654/702097e1-cb63-40ad-ac4b-65130162f7dc)








<ins>Replication Materials</ins>

The dataset DJIA_1901_to_2016_red.csv contains the time-series used in our study for the period January 5, 1901 to December 30, 2016.

The program pentropy_single_f.gss is a GAUSS program that reproduces the normalized PE result of 0.998 reported on p. 7 of our paper, using a time delay of 1, an embedding dimension of 4, and the DJIA time series. 

The program pentropy_rw_f.gss is a GAUSS program that implements the rolling windows algorithm and reproduces the results reported on pp. 8 and 9 of our paper, including Figure 2, using a time delay of 1, an embedding dimension of 5, and the DJIA time series. 
