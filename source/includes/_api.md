# API

## addmultisigaddress

создание адреса с несколькими подписями с добавлением в клиент

`addmultisigaddress <nrequired> <'["key","key"]'> [account]`

- *nrequired* – минимальное количество подписей, необходимых для подтверждения транзакции с адреса 
- *key* – публичный ключ адреса, участвующего в подписи исходящих транзакций.

## addredeemscript 

добавление адреса с несколькими подписями путём добавления его скрипта.

`addredeemscript <redeemScript> [account]`

## backupwallet  

создание резервной копии wallet.dat 

`backupwallet <destination>`

- *destination* – путь сохранения копии

## checkwallet  

проверка целостности данных клиента. 

`checkwallet`

## createrawtransaction  

создание исходящей транзакции, готовой для отправки в сеть (RAW формат) 

`createrawtransaction [{"txid":txid,"vout":n},...] {address:amount,...}`

- txid – номер транзакции 
- n – номер выхода транзакции {"txid":txid,"vout":n},... 

используется для ручной подборки транзакций, которые необходимо израсходовать в создаваемой транзакции.

## decoderawtransaction 

преобразование формата транзакции из RAW (HEX) в JSON представление

`decoderawtransaction <hex string>`

## decodescript 

преобразование формата multiSig скрипта из RAW (HEX) в JSON представление

`decodescript <hex string>`

## dumpprivkey  

вывести приватный ключ указанного адреса (при его наличии в wallet.dat)

`dumpprivkey <PostCoinaddress>`

## dumpwallet   

выгрузить адреса и их ключи в отдельный файл

`dumpwallet <filename>`

## getaccount    

получить имя записи, установленного для указанного адреса

`getaccount <PostCoinaddress>`
