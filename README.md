# Fintz SDK

Biblioteca python para você interagir com a API da Fintz

## Instalar

```
pip install fintz
```

## Como usar?

```py
from fintz import Fintz

fintz = Fintz('API_KEY')

fintz.bolsa.dres('PETR4', year=2020, quarter=3)
fintz.bolsa.info('PETR4')
fintz.bolsa.busca('PETR4')
fintz.bolsa.eventos('PETR4')
fintz.bolsa.cotacoes('PETR4')
fintz.bolsa.historico('PETR4')
fintz.bolsa.proventos('PETR4')

fintz.titulos.tesouro.info('NTNBP20450515')
fintz.titulos.tesouro.cupons('NTNB20450515')
fintz.titulos.tesouro.busca()
fintz.titulos.tesouro.precos.atual('NTNBP20450515')
fintz.titulos.tesouro.precos.historico('NTNBP20450515')
```
