# RoboCup2D

Repositório destinado a disseminação de conhecimento sobre a competição 2d de futebol de robôs. 

# O simulador de futebol

O RoboCup Soccer Simulator é uma ferramenta de pesquisa e educação para sistemas multiagentes e inteligência artificial.

- Site oficial da competição https://www.robocup.org/
  
# Preparando o ambiente

O sistema usado para o tutorial foi a distribuição Ubuntu na versão **16.04** encontrado em https://ubuntu.com/

     O sistema foi instalado utilizando o inglês como linguagem nativa.
 
Git para clone dos arquivos encontrado em https://git-scm.com/

# Arquivos necessários

Todos os arquivos necessários para iniciar uma partida de futebol simulada estão disponíveis neste repositório, são eles:

   - **agentbase** (Um time de exemplo para o RoboCup Soccer 2D Simulator)
   - **librcsc** (Uma biblioteca básica para desenvolver um time de futebol simulado e ferramentas relacionadas para o RoboCup Soccer 2D Simulator)
   - **rcssmonitor** (Um monitor usado para visualizar a simulação enquanto ela ocorre)
   - **rcssserver** (Servidor que permite que 11 jogadores robóticos autônomos simulados joguem futebol)

# Instalando os arquivos e dependências

Para fazer os passo seguintes tenha privilégio de administração. 

## librcsc

A librcsc depende das seguintes dependências:

- Boost 1.38 ou posterior https://www.boost.org/

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential libboost-all-dev autoconf automake libtool
```

Para construir a biblioteca, execute comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso as bibliotecas estaram prontas para serem usadas.

## agentbase

A librcsc depende das seguintes dependências:

- Boost 1.38 ou posterior https://www.boost.org/
- librcsc

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential libboost-all-dev
```
Para construir a biblioteca, execute comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso os agentes estaram prontos para serem usados.


