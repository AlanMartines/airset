# Airset
Engenharia social para ‘receber’ a senha do Wi-Fi

Descobrir ou ‘quebrar’ a chave simétrica de criptografia utilizada em protocolos de autenticação mais modernos, como as variantes do WPA2 (Wi-Fi Protected Access) em redes 802.11 não é uma tarefa tão simples como pode parecer em alguns vídeos do Youtube ou tutoriais na web.

Descobrir a senha do Wi-Fi em APs mais modernos, com suporte a protocolos mais novos e por consequente algoritmos de criptografia mais poderosos, seja por brute-force, ataques de dicionário com Reaver, por exemplo, ou criptoanálise, podem ser bastante morosos. Por estas e outras, que ferramentas como a criada pelo brasileiro Alef Carvalho, o Airset, costumam fazer muito sucesso no universo dos pentests.

Não é objetivo deste post ser um guia sobre como instalar e utilizar o Airset no Linux. A ideia aqui, é apenas deixar os principais passos para experimentar as técnicas de engenharia social propostas pela ferramenta. Você pode obter maiores informações nos links citados acima.

### Usando Airset no Kali Linux
### Repositórios para airset – Se necessário

```sh
deb http://old.kali.org/kali sana main non-free contrib
deb http://old.kali.org/kali moto main non-free contrib
```

### Clonando repositório do Airset

```sh
git clone https://github.com/AlanMartines/airset
```

### Ajustando permissionamento

```sh
sudo chmod -R 777 airset
```

### Satisfazendo dependências

```sh
sudo apt-get install isc-dhcp-server -y
sudo apt-get install hostapd -y
sudo apt-get install lighttpd -y
sudo apt-get install php-cgi -y
```

### Hands on

```sh
cd airset/
sudo ./airset
```
