# RoboCup2D

Repositório destinado a disseminação de conhecimento sobre a competição 2d de futebol de robôs. 

# O simulador de futebol

O _RoboCup Soccer Simulator_ é uma ferramenta de pesquisa e educação para sistemas multiagentes e inteligência artificial.

- Site oficial da competição https://www.robocup.org/
  
# Preparando o ambiente

O sistema usado para o tutorial foi a distribuição Ubuntu na versão **16.04** encontrado em https://ubuntu.com/

- O sistema foi instalado utilizando o inglês como linguagem nativa.
 
Git para clone dos arquivos encontrado em https://git-scm.com/

# Arquivos necessários

Todos os arquivos necessários para iniciar uma partida de futebol simulada estão disponíveis neste repositório, são eles:

   - **agentbase** (Um time de exemplo para o RoboCup Soccer 2D Simulator)
   - **librcsc** (Uma biblioteca básica para desenvolver um time de futebol simulado e ferramentas relacionadas para o RoboCup Soccer 2D Simulator)
   - **rcssmonitor** (Um monitor usado para visualizar a simulação enquanto ela ocorre)
   - **rcssserver** (Servidor que permite que jogadores robóticos autônomos simulados joguem futebol)

# Instalando os arquivos e dependências

Para fazer os passo seguintes tenha privilégio de administração. 

## librcsc

A librcsc necessita das seguintes dependências:

- Boost 1.38 ou posterior https://www.boost.org/

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential libboost-all-dev autoconf automake libtool
```

Para construir a biblioteca, execute os comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso as bibliotecas estarão prontas para serem usadas.

## agentbase

A librcsc necessita das seguintes dependências:

- Boost 1.38 ou posterior https://www.boost.org/
- librcsc

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential libboost-all-dev
```
Para preparar os agentes, execute os comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso os agentes estarão prontos para serem usados.

## rcssserver

O rcssserver necessita das seguintes dependências:

- g++ (which supports C++14)
- autoconf
- automake
- libtool
- flex
- bison
- boost >= 1.44

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential automake autoconf libtool flex bison libboost-all-dev
```

Para preparar o servidor, execute os comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso o servidor já pode ser usado.

## rcssmonitor

O rcssmonitor necessita das seguintes dependências:

- g++
- Qt5

No caso do Ubuntu 16.04, execute os seguintes comandos para instalar um ambiente de desenvolvimento básico:
```
sudo apt update
sudo apt install build-essential qt5-default libfontconfig1-dev libaudio-dev libxt-dev libglib2.0-dev libxi-dev libxrender-dev
```

Para preparar o monitor, execute os comandos da raiz do diretório de origem:
```
./configure
make
sudo make install
```

Após isso o monitor já pode ser usado.

# Iniciando uma partida

Após a instalação de todas as dependências acima uma partida pode ser iniciada.

### Start no monitor e servidor

No diretório raiz execute o seguinte comando:
```
rcsoccersim
```

O monitor deve ser iniciado mostrando 22 agentes na parte superior da tela. Este terminal deve permanecer aberto pois através dele a comunicação com o servidor é feita.

### Carregando os agentes

No diretório src encontrado em /agentbase/src execute o seguinte o seguinte comando:
```
./start.sh -t "NOME DO TIME"
```

Observe que um dos times será carregado. Este terminal deve permanecer aberto pois através dele a comunicação com o servidor é feita.

Abra novamente um terminal no diretório src encontrado em /agentbase/src e execute o seguinte comando:
```
./start.sh -t "NOME DO TIME"
```

Observe que o segundo times será carregado. Este terminal deve permanecer aberto pois através dele a comunicação com o servidor é feita.

## Iniciando a partida

Após as configurações acima é possível dar o ponta pé inicial na partida. 

No menu superior do monitor vá em **Reference** e selecione **Kick Off**.

A partida será iniciada.

# Referências

O artigo sobre a Base HELIOS utilizado para a criação da **agentbase**:

- Hidehisa Akiyama, Tomoharu Nakashima, HELIOS Base: An Open Source Package for the RoboCup Soccer 2D Simulation, In Sven Behnke, Manuela Veloso, Arnoud Visser, and Rong Xiong editors, RoboCup2013: Robot World XVII, Lecture Notes in Artificial Intelligence, Springer Verlag, Berlin, 2014. http://dx.doi.org/10.1007/978-3-662-44468-9_46

Trabalhos relacionados:

- Hidehisa Akiyama, Daisuke Katagami, Katsumi Nitta, Team Formation Construction Using a GUI Tool in the RoboCup Soccer Simulation, SCIS & ISIS, 2006, Volume 2006, SCIS & ISIS 2006, Session ID TH-D2-5, Pages 80-85, Released September 12, 2008, https://doi.org/10.14864/softscis.2006.0.80.0
- Hidehisa Akiyama, Daisuke Katagami, Katsumi Nitta, Training of Agent Positioning using Human's Instruction, Journal of Advanced Computational Intelligence and Intelligent Informatics, Vol. 11 No.8, pp.998--1006, 2007-10-20. https://doi.org/10.20965/jaciii.2007.p0998
- Hidehisa Akiyama, Itsuki Noda, Multi-Agent Positioning Mechanism in the Dynamic Environment, In Ubbo Visser, Fernando Ribeiro, Takeshi Ohashi, and Frank Dellaert, editors, RoboCup 2007: Robot Soccer World Cup XI Lecture Notes in Artificial Intelligence, vol. 5001, Springer, pp.377-384, July 2008. https://doi.org/10.1007/978-3-540-68847-1_38
