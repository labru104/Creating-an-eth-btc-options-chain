This is a project which seeks to recreate ethereum options premia and returns for both buyers and sellers of calls and puts. It is flexible and fairly easy to change

Limitations:

The ethereum-VIX is an annualized estimate of 30-day volatility, so any time shorter or longer than a month from expiration. On our centralized stock market, the CBOE makes up for this shortcoming through having volatility indices from 9 days to 1 year, but in the crypto world all we have is the 30-day (for now).

Speaking of implied volatility, almost all crypto options markets have volatility smiles (volatility for one strike may not be the same as another throughout an options chain). To account for this, I implement a naive function that likely underestimates the volatility smile.
tl;dr: further out of the money the strikes are probably underpriced in this model, at the money and in the money strikes are probably overpriced

Certainly a real life version of the data this chain is trying to recreate exists, but from what I've seen it's quite expensive, so we will just have to make do with what we have.



If you have any ideas or questions, or just want to talk shoot me an email at labrunanicholas@gmail.com

Data sources:

Risk-Free Rate: https://fred.stlouisfed.org/series/DGS10
Eth-VIX: https://t3index.com/indices/bit-vol/ (click "eth" then "all" and download the csv)
Eth-Price: https://etherscan.io/chart/etherprice

To run: Install reqs by typing "" into the command, fix paths to data files to ensure they're pointing to the proper spot you have them stored