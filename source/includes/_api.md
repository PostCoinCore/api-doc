# API

## add multisig address

создание адреса с несколькими подписями с добавлением в клиент

`addmultisigaddress <nrequired> <'["key","key"]'> [account]`

- *nrequired* – минимальное количество подписей, необходимых для подтверждения транзакции с адреса 
- *key* – публичный ключ адреса, участвующего в подписи исходящих транзакций.

## add redeem script 

добавление адреса с несколькими подписями путём добавления его скрипта.

`addredeemscript <redeemScript> [account]`

## backup wallet  

создание резервной копии wallet.dat 

`backupwallet <destination>`

- *destination* – путь сохранения копии

## check wallet  

проверка целостности данных клиента. 

`checkwallet`

## create raw transaction  

создание исходящей транзакции, готовой для отправки в сеть (RAW формат) 

`createrawtransaction [{"txid":txid,"vout":n},...] {address:amount,...}`

- txid – номер транзакции 
- n – номер выхода транзакции {"txid":txid,"vout":n},... 

используется для ручной подборки транзакций, которые необходимо израсходовать в создаваемой транзакции.

## decode raw transaction 

преобразование формата транзакции из RAW (HEX) в JSON представление

`decoderawtransaction <hex string>`

## decode script 

преобразование формата multiSig скрипта из RAW (HEX) в JSON представление

`decodescript <hex string>`

## dump priv key  

вывести приватный ключ указанного адреса (при его наличии в wallet.dat)

`dumpprivkey <PostCoinaddress>`

## dump wallet   

выгрузить адреса и их ключи в отдельный файл

`dumpwallet <filename>`

## get account    

получить имя записи, установленного для указанного адреса

`getaccount <PostCoinaddress>`

## get account address     

получить адрес, идентифицируемый указанным именем

`getaccountaddress <account>`

## getaddressesbyaccount     

вывести весь список адресов, идентифицируемый указанным именем

`getaddressesbyaccount <account>`

## getbalance     

получить баланс по имеющимся в wallet.dat адресам

`getbalance [account] [minconf=1`

- account – фильтр по адресу. 

## getbestblockhash      

хэш последнего найденного блока в сети

`getbestblockhash `

## getblock hash    

вывести данные о блоке с указанным хэшем

`getblock <hash> [txinfo]`

- txinfo – флаг, указывающий что вместо хэша транзакции необходимо вывести детализированную информацию, принимает значения true или false.

## getblock number    

вывести данные о блоке с указанным номером в цепочке

`getblock <number> [txinfo]`

- txinfo – флаг, указывающий что вместо хэша транзакции необходимо вывести детализированную информацию, принимает значения true или false.

## getblockcount

вывести количество блоков в основной цепочке (исключая нулевой)

`getblockcount`

## getblockhash

вывести хэш блока по его номеру(индексу) в цепочке блоков

`getblockhash <index>`

## getblocktemplate 

вывести данные, необходимые для генерации нового блока

`getblocktemplate [params]`

## getcheckpoint 

вывести данные о последнем чекпоинте (контрольной точке)

`getcheckpoint`

## getconnectioncount  

вывести количество активных подключений клиента в сети

`getconnectioncount`

## getdifficulty   

вывести данные о текущей сложности сети

`getdifficulty `
