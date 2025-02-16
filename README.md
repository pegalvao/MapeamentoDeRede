# Nmapscan

Utilizando Nmap e NSE scripts para mapear as vulnerabilidades da rede

**Identificar possíveis vulnerabilidades no meu sistema**\
**Identificar se meu IP está sendo usado devidamente ou se há invasores externos**


Primeiramente será necessário coletar o ip da minha própria máquina, como estou utilizando o Linux é só utilizar o comando :

```
hostname - I
```
**Obs: Substitua o xxx.xxx.xxxx pelo seu próprio endereço de Ip para não gerar nenhum problema**

O primeiro script utilizado será o script safe que por não explorar nenhuma falha e segurança nem travar nenhum serviço utilizado é menos propenso de gerar situações adversas, mesmo assim ele consegue descobrir dados gerais da rede

```
sudo nmap -f --script safe xxx.xxx.xxxx

```
![!\[Alt text\](image.png)](Prints/image.png)


Com isso obtemos o nome de domínio da rede e outras informações.

O segundo script será o vuln que detecta algumas vulnerabilidades no sistema

```
sudo nmap -f --script vuln xxx.xxx.xxxx

```
![!\[Alt text\](image.png)](Prints/image2.png)


O terceiro script será o default or safe que vai rodar a os scripts da varredura padrão, da varredura safe que já utilizei no começo do escaneamento e os scripts que se enquadram nas duas categorias.

```
sudo nmap -f --script "default or safe" xxx.xxx.xxxx

```
![!\[Alt text\](image.png)](Prints/image3.png)

A diferença é que com o default foi possível obter o servidor DHCP que nos forneceu o endereço de Ip, a submáscara da rede, o IP do roteador e DNS

O quarto script será o "malware" que vai identificar se meu aparelho está infectado com malwares e se há backdoors escondidos na rede.

```
nmap -v --script "malware" xxx.xxx.xxxx

```

![!\[Alt text\](image.png)](Prints/image4.png)

Nessa varredura não achado nenhum tipo de malware ou backdoor.

## Referências: 
NMAP: https://nmap.org/man/pt_BR/man-briefoptions.html

NSE :https://nmap.org/book/nse-usage.html