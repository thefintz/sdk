# Fintz SDK

![Build](https://github.com/thefintz/sdk/actions/workflows/build.yml/badge.svg)
![Pypi version](https://img.shields.io/pypi/v/fintz?color=%2334D058&label=pypi%20package)
![Python versions](https://img.shields.io/pypi/pyversions/fintz.svg?color=%2334D058)

Biblioteca python para você interagir com a API da Fintz

## Sobre

A fintz é uma API feita para você não ter que se preocupar com dados do mercado
financeiro. É fácil de usar e você pode começar a construir ferramentas e
serviços rapidamente.

Para mais informações, entre em contato conosco pelo nosso [site][1].

## Instalar

A instalação é super simples, basta usar `pip`:

```
pip install fintz
```

## Como usar?

Estamos sempre trabalhando para melhorar a usabilidade do SDK. Queremos deixar
bem intuitivo para qualquer pessoa. Desde desenvolvedores com experiência até
pessoas com baixo conhecimento na área de programação.

Aqui vão alguns exemplos de métodos que temos implementados:

```py
from fintz import Fintz

fintz = Fintz()  # usa uma chave padrão limitada

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

Se você estiver recebendo erros do tipo `429 Too Many Requests`, significa que
a chave padrão está sendo muito utilizada e você deverá entrar em contato
conosco para conseguir uma chave nova com limites maiores. Para entrar em
contato, use o formulário em nosso [site][1].

Quando tiver a chave nova, basta usar o SDK da seguinte forma:

```py
from fintz import Fintz

fintz = Fintz('SUA_CHAVE_AQUI')
```

## Desenvolvimento

Para desenvolver, decidimos usar o [Poetry][2], pois facilita bastante na hora
de realizarmos o build e de enviar para o [pypi][3]. Sendo assim, se quiser
realizar modificações no código, basta:

```
git clone git@github.com:thefintz/sdk.git
poetry install
```

E é isso!

[1]: https://fintz.com.br/
[2]: https://python-poetry.org/
[3]: https://pypi.org/
