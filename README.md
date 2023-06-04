# Objetivo

Nesse projeto, realizado para a disciplina de Eletrônica para Computação do curso da USP - São Carlos, tem-se como objetivo projetar uma **Fonte de Tensão ajustável** entre **3V e 12V** com capacidade de **100mA** <br> 

# Funcionamento 

A fonte transforma a tensão do fornecedor (127V - 220V) em corrente alternada (AC) que, posteriormente, será convertida numa tensão de corrente contínua que permite o funcionamento dos equipamentos. <bt>
  
![Diagrama](diagrama.jpeg) <br>  

**Transformador:** Converte a tensão recebida (AC) para um valor utilizável em AC.

**Ponte retificadora:** Retifica os pulsos de energia alternada para um sinal contínuo de modo a produzir uma saída polarizada DC.
  
**Filtragem:** Filtra a tensão tornando a corrente contínua.
  
**Regulação:** Regula a saída para obter uma tensão constante.
  
# Etapas 

  1. O processo se inicia com a entrada de um sinal elétrico alternado, em que a DDP será reduzida pelo transformador, dispositivo capaz de "elevar" ou "reduzir" os níveis de tensão entre a entrada e a saída. Essa etapa é essencial para reduziro sinal elétrico recebido para uma voltagem utilizável.<br> 
  
![Transformador](transformador.png) <br> 
  
  2. O próximo estágio é a retificação da enegeria alternada recebida para um sinal contínuo.
  Essa etapa é composta por uma ponte com quatro diodos que só permitem a passagem dos semiciclos positivos do sinal original, sendo essa configuração conhecida como retificador de onda completa. 
  
  ![ponte_de_iodo](pontedeiodo.png) <br  /> ![pontes_gif] (pontes.gif) <br> 
  
# Cálculos 

# Valores 

# Circuito no Falstad 

Link do circuito: https://tinyurl.com/2eja2aah <br> 

# PCB no EAGLE

# Fontes de pesquisa 

Aulas do Professor Simões: https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0180-Eletronica-para-Computacao

# Responsáveis 

Shogo Shima -  <br>
Jesus - <br>
Letícia Jönck - <br>  
Pietra Gullo Salgado Chaves - 14603822 <br>
José Carlos - <br>
