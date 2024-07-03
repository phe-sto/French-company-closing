# Classification of french companies closing business next year or not

## Why

The number of companies closing business in France is rapidly rising since the
middle of the COVID 19 crisis. Plus 27.7 % in April 2024 over one year, according to Société.com[^1].

This works aims at predicting if a company will be closing business or not based on
its financial data from previous years.

Being able to predict such trend is relevant to many economic actors such as investors,
insurance companies, banks, policy makers, etc.

## How

This datascience project is based on 2 official datasets from french administrations.
The BODACC logging business closures and the INPI registering financial data
from business tribunals all over France.
Both can be downloaded as parquet files from the following links:

- [BODACC "radiations", closure in French](https://www.bodacc.fr/explore/dataset/annonces-commerciales/table/?sort=dateparution&dataChart=eyJxdWVyaWVzIjpbeyJjb25maWciOnsiZGF0YXNldCI6ImFubm9uY2VzLWNvbW1lcmNpYWxlcyIsIm9wdGlvbnMiOnsic29ydCI6ImRhdGVwYXJ1dGlvbiIsInJlZmluZS5wdWJsaWNhdGlvbmF2aXNfZmFjZXR0ZSI6IkJvZGFjYyBBIn19LCJjaGFydHMiOlt7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IkFWRyIsInlBeGlzIjoibnVtZXJvYW5ub25jZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiM2NmMyYTUifV0sInhBeGlzIjoiZGF0ZXBhcnV0aW9uIiwibWF4cG9pbnRzIjoiIiwidGltZXNjYWxlIjoieWVhciIsInNvcnQiOiIifV0sImRpc3BsYXlMZWdlbmQiOnRydWUsImFsaWduTW9udGgiOnRydWV9)
  which is one of the class to predict, the other, being by default, open.
- [INPI Financial data](https://www.data.gouv.fr/fr/datasets/donnees-financieres-detaillees-des-entreprises-format-parquet/)
  containing all the
  potentiel explanatory variables.

> **_Remark:_**  The INPI data are not the raw one they were released. But the one cleaned and transformed by [_Signaux
Faibles_](https://www.data.gouv.fr/fr/organizations/signaux-faibles/).
> Thank to them for their essential work. As the raw data are hundreds of massive, unstructured JSON zipped files, they
> are really hard to work with.

Those data are used to train a machine learning model to predict if a company will be closing business or not.
And the INPI data are used again to predict the financial data of the next year using the trained model.

All the data are, download and processed in the `./data` folder.
Images are stored in the `./images` folder.
The notebooks are is the `./closing.ipynb` file.

[^1]: Baromètre Société.com des défaillances d'entreprises en France - avril
2024, https://www.societe.com//publications/barometre-societe.com-des-defaillances-76681.html?v=41ddd2e1cbd6d25deb007ebd830cd6