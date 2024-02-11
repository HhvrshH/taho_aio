# TAHO AIO

Written by: @hvrsh (TG)

Channel: @hashvers (TG)

---

**BAS Automation for swaping via Taho**

**Setup when launching `taho_aio.xml`:**

1. Use Finger Switcher - whether to use fingerprints.
   1. Finger Print Key - if **1** is enabled, you need to enter a key to obtain fingerprints, which can be purchased here - https://fingerprints.bablosoft.com/
3. Threads - number of threads launched simultaneously.
4. Mode - operation mode
   1. Swaps - swaps the native currency in one direction randomly selected from the chosen `Chains` to a randomly selected token from the `tokens_data.json` file. The swap range for each blockchain is specified separately in the `swap_amounts.json` file.
   2. Sizes - cyclic swap (Native->Token Token->Native) in a random network from the selected token to a random token from the list in the `tokens_data.json` file. The swap range for this mode is set in % in `Size Swap Percentage`.
5. Chains - selection of chains in which you want to perform swaps. (Do not select Celo, as there are no working swap routes). Swap only from native token to token.
6. Approves - approval type in `Sizes` mode
   1. Infinity - once for each token.
   2. For each swap - approval only for the swap amount, a new swap means a new approval.
7. Swap Count - range of swap counts.
8. Gas - gas speed inside Taho.
9. Sleep(in sec) - Sleep range. Do not set the lower value too low (below 10 sec.).
10. Gas Trigger - Gas waiter.
11. gasAPI - Can be left blank (if the waiter is working incorrectly, obtain the key from etherscan).
12. Clear DoneList - After successful claim or insufficient balance in all selected networks, private keys are written to the `done_list.txt` file so that the software understands which accounts it has passed and which ones it has not, in case you interrupt its work or the thread terminates with an error. If you need to run all wallets again (for example, a new day) - select Yes.
13. Wallet shuffle - whether to shuffle wallets.
14. Proxy Type - proxy type.


 **Settings in files**

 `bal_checker_targets.json` - the minimum value to consider balance insufficient in the network (can be left at default).

 `private.txt` - private keys.

 `proxy.txt` - proxies, selected line by line.

 `tokens_data.json` - lists of tokens participating in swaps.

 `swap_amounts.json` - swap amount ranges for each network. used in `Swaps` mode.

---

**Автоматизация на БАСе для обменов в кошельке Taho**

**Настройка при запуске `taho_aio.xml`:**

1. Use Finger Switcher - использовать ли отпечатки.
	1. Finger Print Key - в случае включения **1** нужнно вести ключ для получения отпечатков, покупается тут - https://fingerprints.bablosoft.com/
3. Threads - количество потоков запущеных одновременно.
4. Mode  - режим работы
	1. Swaps - свап нативной монеты в одну сторону, рандомно, из выбраных `Chains` в рандомно выбраный токен с файла `tokens_data.json`. Диапазон значений для свапа указывается для каждого блокчейна отдельано в файле `swap_amounts.json`
	2. Sizes - цикличный свап(Нативка->Токен Токен->Нативка) в рандомной сети из выбраных в рандомный токен с списка в файле `tokens_data.json`. Диапазон свапа для этого режима задается в % в `Size Swap Percentage`.
5. Chains - выбор чейнов в которых в хотите сделать свап.(Celo не выбирать, нету рабочих маршрутов для свапа). Свап тольок с нативного токена в токен.
6. Approves - тип апрува в режиме `Sizes`
	1. Infinity - один раз для каждого токена.
	2. For each swap - апрув тольок на величину свапа, новый свап - новый апрув.
7. Swap Count - диапазон количества свапов.
8. Gas - скорось газа внутри Taho.
9. Sleep(in sec) - диапазон Сна. Нижние значение не ставить слишком малое(ниже 10 сек.).
10. Gas Trigger - Ожидатель газа.
11. gasAPI - Можно оставлять пустым(если ожидатель работает некоректно то взять ключ в etherscan).
12. Clear DoneList - После успешного клейма или отсутствия достаточного баланаса во всех выбраных сетях в файл `done_list.txt` записываются приватники, чтобы софт понимал какие аккаунты он прошел а какие нет, в случае если вы прервали его работу или поток завершится с ошибкой. Если нужно прогнать все кошельки заново(новый день к примеру) - выбираем Yes.
13. Wallet shuffle - делать ли перемешивание кошельков.
14. Proxy Type - тип прокси.


 **Настройка в файлах**

 `bal_checker_targets.json` - меньше какого значения считать что не хватает баланса в сети (можно оставить по умлочанию) .

 `private.txt` - приватники.

 `proxy.txt` - прокси, выбираюся построчно.

 `tokens_data.json` - списки с токенами которые будут участвовать в свапах.

 `swap_amounts.json` - диапазоны величины свапов для каждый сети. используется в режиме `Swaps`
 