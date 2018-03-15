# Информация о PostCoin API

[![Release](https://img.shields.io/github/release/PostCoinCore/postcoin.svg)](https://github.com/PostCoinCore/postcoin/releases/latest)

Добро пожаловать в официальную документацию PostCoin API! Вы можете использовать API для доступа к PostCoin API BlockChain.

Вы можете просмотреть код примеров и результаты выполнения справа в теиной области. 

Для соединения с api используйте следующую ссылку: <code>http://127.0.0.1:<rpc_port></code>

Список параметров, используемых в командной строке клиента, можно вывести используя команду PostCoind help

Оригинальное описание каждого параметра можно получить командой PostCoind help <параметр>

В консоли GUI-клиента для этого используется команда help и help <параметр> соответственно.

## Общие положения и переменные 
`< >` обязательное поле с сохранением пунктуации 

`[ ]` необязательное поле 

`|` разделитель, используемый для указания команды на выбор account, label имя для адреса/адресов в клиенте, указываемое пользователем для упрощения идентификации 

minconf минимальное количество подтверждений для транзакций, целое число >=0

## Specification

- Mining: PoS
- Ticker: POST
- Block Time: 60 sec
- Minimum Stake Age: 12 hours
- Maximum Stake Age: 14 days
- Stake Rate: 2% Fixed
- Initial Supply: 30.000.000 POST
- Supply after burning the leftover coins from Free Distribution: ~15.081.003 POST
