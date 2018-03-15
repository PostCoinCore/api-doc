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

## getinfo    

вывести основные данные о клиенте, балансе и состоянии сети

`getinfo`

## getmininginfo     

вывести основные данные о состоянии майнинга в сети

`getmininginfo`

## getnewaddress     

создать и зарегистрировать новый адрес в клиенте

`getnewaddress [account]`

- account – привязать адрес к указанному имени

## getnewpubkey      

создать новый публичный ключ в клиенте 

`getnewpubkey [account]`

account – привязать публичный ключ к указанному имени

## getpeerinfo       

вывести детальную информацию о подключенных клиентах

`getpeerinfo`

## getrawmempool        

информация о транзакциях, ещё не включенных в блок

`getrawmempool`

## getrawtransaction        

вывести транзакцию по её хэшу

`getrawtransaction <txid> [verbose=0]`

- verbose – определяет как её выводить: 0 для вывода в RAW (HEX) формате (по-умолчанию) 1 для вывода в JSON формате

## getreceivedbyaccount         

сумма полученных средств, поступивших на адреса, привязанные к указанному имени

`getreceivedbyaccount <account> [minconf=1]`

## getreceivedbyaddress          

сумма полученных средств, поступивших на указанный адрес

`getreceivedbyaddress <PostCoinaddress> [minconf=1]`

## getstakinginfo          

Возвращает объект, содержащий информацию о stake

`getstakinginfo`

## getsubsidy           

вывести награду согласно запрашиваемого таргета

`getsubsidy [nTarget]`

## gettransaction            

вывести транзакцию по её хэшу в JSON формате

`gettransaction <txid>`

## getwork             

получить данные для майнинга

`getwork [data]`

## getworkex              

получить расширенные данные для майнинга

`getworkex [data, coinbase]`

## help               

вывести помощь по командам, а если указана команда, то расширенная информация по ней

`help [command]`

## importprivkey                

импортировать (зарегистрировать) в клиенте адрес по его приватному ключу для последующего проведения операций со средствами

`importprivkey <PostCoinprivkey> [label]`

## importwallet                 

импортировать все данные, находящиеся в другом файле со структурой wallet.dat

`importwallet <filename>`

## keypoolrefill                  

перезаполнить пул предварительно сгенерённых адресов

`keypoolrefill [new-size]`

- new-size – новый размер пула (по умолчанию 100)

<aside class="warning">
ВАЖНО: после регенерации необходимо создать новую резервную копию кошелька
</aside>

## listaccounts                 

вывести все имена, зарегистрированные в клиенте

`listaccounts [minconf=1]`

## listaddressgroupings                  

вывести все адреса, сгруппированные по зарегистрированным именам

`listaddressgroupings`

## listreceivedbyaccount                   

суммы полученных средств сгрупированные по используемым именам

`listreceivedbyaccount [minconf=1] [includeempty=false]`

## listreceivedbyaddress                   

суммы полученных средств сгрупированные по адресам

`listreceivedbyaddress [minconf=1] [includeempty=false]`

## listsinceblock                    

вывести проведённые клиентом транзакции (начиная с указанного блока, если указан хэш блока)

`listsinceblock [blockhash] [target-confirmations]`

## listtransactions                    

вывести проведённые клиентом транзакции, начиная с начала

`listtransactions [account] [count=10] [from=0]`

- count – количество выводимых транзакций (по умолчанию 10) 
- from – количество первых транзакций, которые пропустить (по умолчанию 0)

## listunspent                    

вывести непотраченные транзакции

`listunspent [minconf=1] [maxconf=9999999] ["address",...]`

- maxconf – максимальное количество выводимых транзакций (по умолчанию 9999999) 
- "address",... – адреса, по которым необходимо произвести отбор (по умолчанию все)

## makekeypair                    

сгенерировать пару публичного и приватного ключа

`makekeypair [prefix]`

- prefix – предустановление префикса публичного ключа

## move                    

перенести средства с одного имени на другое 

`move <fromaccount> <toaccount> <amount> [minconf=1] [comment]`

- fromaccount – откуда переносить 
- toaccount – куда переносить 
- amount – сколько переносить

## repairwallet                     

восстановить потерянные/неверно зарегистрированные/пропущенные данные в wallet.dat

`repairwallet`

<aside class="info">
после вызова команды repairwallet необходим перезапуск клиента
</aside>
