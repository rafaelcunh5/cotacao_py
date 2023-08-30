# cotacao_py

#É um projeto criado para ver o valor da moeda dólar, euro e bitcoin em reais(moeda brasileira).

#Para ver o valor do dólar deve substituir 'EURBRL' por 'USDBRL', e o bitcoin deve substituir o 'EURBRL' por 'BTCBRL'

import requests
import json

cotacoes = requests.get("https://economia.awesomeapi.com.br/last/USD-BRL,EUR-BRL,BTC-BRL")
cotacoes = cotacoes.json()

cotacao_euro = cotacoes['EURBRL']['bid']
print(cotacao_euro)

#OBS: projeto criado no dia 30/08/2023
