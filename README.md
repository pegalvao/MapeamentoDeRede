# N  -mapscan

Utilizando Nmap e NSE scripts para mapear as vulnerabilidades da rede

*Identificar possíveis vulnerabilidades no meu sistema
*Identificar se meuIP está sendo usado devidamente ou se há invasores externos




Primeiramente será necessário coletar o ip da minha própria máquina, como estou utilizando o Linux é só utilizar o comando :

```
hostname - I
```
*Obs: substitua o xxx.xxx.xxxx pelo seu próprio endereço de Ip para não gerar nenhum problema*

O primeiro script utilizado será o script safe que por não explorar nenhuma falha e segurança nem travar nenhum serviço utilizado é menos propenso de gerar situações adversas, mesmo assim ele consegue descobrir dados gerais da rede

```
(nmap script -f --script safe xxx.xxx.xxxx)

```
![!\[Alt text\](image.png)](Prints/image.png)


Com isso obtemos o nome de domínio da rede e outras informações









## Referências: 
[NMAP](https://nmap.org/man/pt_BR/man-sudobriefoptions.html)

[NSE](https://nmap.org/book/nse-usage.html)