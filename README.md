# getFamaFrenchFactors

This programme gets data for Fama French factors from the Kenneth French library and returns it as a Pandas dataframe.

## Installation

Run the following to install:

```python
pip install getFamaFrenchFactors
```

## Usage
Factors can be extracted in monthly ('m') and annual ('a') frequencies. **The default frequency is monthly.**

```python
import getFamaFrenchFactors as gff

# Get the Fama French 3 factor model (monthly data)
df_ff3_monthly = gff.famaFrench3Factor(frequency='m') 

# Get the Fama French 3 factor model (annual data)
df_ff3_annual = gff.famaFrench3Factor(frequency='a')
```

Other options:

* Momentum factor: momentumFactor()
* Carhart 4 factor: carhart4Factor()
* Fama French 5 factor: famaFrench5Factor()

## Specifics of factors
The Fama French 3 factor model includes the:
* Market Risk Premium (MRP)
* Size Premium (i.e., Small minus Big) (SMB)
* Value Premium (i.e., High Book-to-Market minus Low Book-to-Market)
* The Risk-free rate (RF)

The Momentum factor returns the momentum factor only, as "MOM"

The Carhart 4 factor returns Fama French 3 Factor and Momentum.

The Fama French 5 factor returns:
* Market Risk Premium (MRP)
* Size Premium (i.e., Small minus Big) (SMB)
* Value Premium (i.e., High Book-to-Market minus Low Book-to-Market)
* Operating Profitability (i.e. Robust minus Weak) (RMW)
* Conservative minus Aggressive Investments (CMA)
* The Risk-free rate (RF)
