# 🎮 OVERCLOCK-FIGHT | LAN HOUSE CASEIRA

<p align="center">
  **Projeto de Infraestrutura de Redes e Montagem de uma LAN House**
</p>

<p align="center">
  🖥️ 8 Computadores Clientes | 🗄️ 1 Servidor | 🌐 Rede Local
</p>

---




## 📌 Sobre o Projeto

O **Overclock-Fight** é um projeto acadêmico que consiste na montagem e configuração de uma LAN House caseira, utilizando equipamentos físicos para implementar uma infraestrutura de rede local.

A estrutura é composta por 8 computadores clientes e 1 computador dedicado ao servidor, conectados por meio de uma rede local (LAN).

O projeto busca demonstrar, na prática, conceitos de infraestrutura de TI, montagem de computadores, configuração de redes, compartilhamento de recursos e administração de sistemas.




## 🎯 Objetivos

- Desenvolver uma infraestrutura de rede local funcional.
- Configurar a comunicação entre os computadores.
- Implementar um servidor para gerenciamento da rede.
- Realizar testes de conectividade.
- Aplicar conceitos de hardware e redes de computadores.
- Documentar todas as etapas de desenvolvimento.




## 🖥️ Estrutura da LAN House



<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/d4bfbb90-1dc8-4cdc-b87a-dbb75a85e08e" />

| Equipamento | Quantidade | Função |
|---|---:|---|
| Computadores clientes | 8 | Acesso dos usuários |
| Servidor | 1 | Gerenciamento de serviços |
| Switch | Conforme montagem | Interligação dos dispositivos |
| Roteador | 1 | Conexão com a rede externa |
| Cabos Ethernet | Conforme necessidade | Comunicação entre equipamentos |






## 🌐 Topologia da Rede
<img width="600" height="800" alt="8d58c6b3-f17b-47a7-a305-bf20a531cd9b" src="https://github.com/user-attachments/assets/4d1fe804-0f68-4942-b71a-395a41facc96" />


A rede utiliza uma estrutura física em estrela, na qual os computadores são conectados a um equipamento central responsável pela interligação dos dispositivos.

```text
             INTERNET
                 |
             ROTEADOR
                 |
               SWITCH
       __________|__________
      |    |    |    |      |
     PC1  PC2  PC3  PC4   SERVIDOR
      |
   Demais computadores
   PC5, PC6, PC7 e PC8
```




## ⚙️ Configuração da Rede

Nesta seção serão documentadas as configurações utilizadas:

- Endereçamento IPv4.
- Máscara de sub-rede.
- Gateway padrão.
- Servidor DNS.
- Configuração DHCP ou IP estático.
- Testes de comunicação entre os computadores.





## 🔐 Segurança

Algumas medidas consideradas no projeto:

- Organização dos dispositivos na rede.
- Controle de acesso aos computadores.
- Proteção por senhas.
- Configuração de firewall.
- Atualização dos sistemas operacionais.




## 🧪 Testes Realizados
<img width="600" height="800" alt="cf63337f-aa2d-4a90-ba18-0c4e0fea5d81" src="https://github.com/user-attachments/assets/ae383588-6f1a-47df-901b-e52f48a99608" />

- Teste de conectividade utilizando `ping`.
- Verificação dos endereços IP.
- Comunicação entre computadores clientes.
- Verificação da conexão com o servidor.
- Teste de acesso à internet.





## 📚 Conhecimentos Aplicados

- Hardware e montagem de computadores.
- Redes de computadores.
- Infraestrutura de TI.
- Sistemas operacionais.
- Administração de servidores.
- Cabeamento de rede.
- Diagnóstico e resolução de problemas.




## 💻 Aplicativos utilizados

Urban Terror https://www.urbanterror.info/home/

Timer Café   https://www.fad-softwares.com.br/

Driver Booster https://www.iobit.com/pt/driver-booster.php





## 👥 Organização dos Grupos

O projeto OVERCLOCK-FIGHT foi dividido em 4 grupos de trabalho, com o objetivo de organizar as atividades, distribuir responsabilidades e facilitar o desenvolvimento da LAN House.
<p align="center">

GRUPO 1: Gabriel, Rafaela , jamile , Milena , Gabriela

GRUPO 2: Reinaldo, Gustavo, Ricardo, Jhonatan, Miguel

GRUPO 3: Jhonatan, Eduardo, Mhateus, Victor, Felipe Dodo

GRUPO 4: Giovanna, Vinicius, Lucas, Felipe Bispo 
 

 **OVERCLOCK-FIGHT**
  
  Projeto acadêmico de infraestrutura de redes.
</p>

# Configuração de IP Fixo no Windows 11 para Lan House

Tutorial rápido para configurar o endereço IP fixo dos computadores de uma lan house usando o painel clássico de conexões de rede do Windows 11.

## Estrutura da rede

| Equipamento | Endereço IP |
|---|---:|
| Roteador | `192.168.0.1` |
| Servidor | `192.168.0.2` |
| PC Cliente 01 | `192.168.0.3` |
| PC Cliente 02 | `192.168.0.4` |
| PC Cliente 03 | `192.168.0.5` |
| PC Cliente 04 | `192.168.0.6` |
| PC Cliente 05 | `192.168.0.7` |
| PC Cliente 06 | `192.168.0.8` |
| PC Cliente 07 | `192.168.0.9` |
| PC Cliente 08 | `192.168.0.10` |

Configuração comum para o servidor e todos os clientes:

```text
Máscara de sub-rede: 255.255.255.0
Gateway padrão:      192.168.0.1
DNS preferencial:    192.168.0.1
DNS alternativo:     deixar em branco
```

> [!IMPORTANT]
> Cada computador deve ter um endereço IP diferente. Nunca configure o mesmo IP em dois equipamentos.

## Passo a passo

### 1. Abrir as conexões de rede

1. Pressione `Windows + R`.
2. Digite o comando:

```text
ncpa.cpl
```

3. Pressione `Enter`.

### 2. Abrir as propriedades da rede

1. Localize a conexão utilizada pelo computador, normalmente chamada **Ethernet**.
2. Clique com o botão direito sobre **Ethernet**.
3. Clique em **Propriedades**.

### 3. Desativar o IPv6

1. Localize **Protocolo IP Versão 6 (TCP/IPv6)**.
2. Desmarque a caixa dessa opção.

> Nesta configuração da lan house, será utilizado o IPv4.

### 4. Abrir as propriedades do IPv4

1. Selecione **Protocolo IP Versão 4 (TCP/IPv4)**.
2. Clique em **Propriedades**.
3. Marque **Usar o seguinte endereço IP**.

### 5. Configurar o endereço IP

Digite o endereço reservado para o computador. Exemplo para o **PC Cliente 01**:

```text
Endereço IP:         192.168.0.3
Máscara de sub-rede: 255.255.255.0
Gateway padrão:      192.168.0.1
```

Nos demais computadores, altere somente o endereço IP conforme a tabela apresentada no início deste tutorial.

### 6. Configurar o DNS

Marque **Usar os seguintes endereços de servidor DNS** e preencha:

```text
Servidor DNS preferencial: 192.168.0.1
Servidor DNS alternativo:  deixar em branco
```

### 7. Salvar

1. Clique em **OK**.
2. Clique novamente em **OK** ou **Fechar**.
3. Repita o procedimento nos demais computadores, usando o IP correto para cada equipamento.

## Testar a configuração

Abra o **Prompt de Comando** e execute:

```bat
ipconfig
```

Teste a comunicação com o roteador:

```bat
ping 192.168.0.1
```

Teste a comunicação com o servidor:

```bat
ping 192.168.0.2
```

Se aparecer uma resposta parecida com esta, a comunicação está funcionando:

```text
Resposta de 192.168.0.1: bytes=32 tempo<1ms TTL=64
```

## Checklist

- [ ] Roteador configurado como `192.168.0.1`
- [ ] Servidor configurado como `192.168.0.2`
- [ ] Clientes configurados de `192.168.0.3` até `192.168.0.10`
- [ ] Máscara configurada como `255.255.255.0`
- [ ] Gateway configurado como `192.168.0.1`
- [ ] DNS preferencial configurado como `192.168.0.1`
- [ ] IPv6 desativado nos computadores desta rede
- [ ] Todos os computadores respondem ao roteador
- [ ] Todos os clientes conseguem se comunicar com o servidor

## Observações

- Faça a configuração utilizando uma conta com permissão de administrador.
- Confirme o IP de cada computador antes de salvar.
- Se a conexão parar de funcionar, verifique o cabo Ethernet, a máscara, o gateway e o DNS.
- Reserve os endereços de `192.168.0.2` até `192.168.0.10` no roteador ou mantenha-os fora da faixa DHCP para evitar conflitos.

---

Material criado para documentar a configuração da rede local de uma lan house com Windows 11.
