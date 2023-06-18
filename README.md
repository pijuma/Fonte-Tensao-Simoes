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

  1. O processo se inicia com a entrada de um sinal elétrico alternado, em que a DDP será reduzida pelo transformador. Essa etapa é essencial para reduzir o sinal elétrico recebido para uma voltagem utilizável.<br> 
  O transformador é um dispositivo composto por duas bobinas acopladas a um núcleo magnético, que nesse projeto é usado no intuito de reduzir a tensão da tomada para uma que seja utilizável de forma segura pela fonte. Sendo seu funcionamento relacionado ao princípio de indução eltromagnética, no qual a bobina primária ligada na tomada cria um campo magnético que induz uma corrente na bobina secundária. E, como as bobinas possuem quantidades diferentes de espiras, as correntes e voltagens serão diferente de cada lado, para que a potência seja constante. 
  $$Ve.Ns = Vs.Ne$$
Portanto, para transformar a voltagem de entrada (Ve) na voltagem de saída (Vs), considerando Ve > Vs, temos que a quantidade de voltas da entrada tem que ser maior que a da saída. <br><br>
![Transformador](transformador.png) <br> 
  
  2. O próximo estágio é a retificação da enegeria alternada recebida para um sinal contínuo.
  Essa etapa é composta por uma ponte com quatro diodos que só permitem a passagem dos semiciclos positivos do sinal original, sendo essa configuração conhecida como retificador de onda completa. 
  A ponte retificadora é composta por quatro diodos colocados em pares alternados que transformam tanto a seção positiva quanto negativa da corrente AC em uma tensão polarizada DC. 
  
  ![ponte_de_iodo](pontedeiodo.png)    ![pontes_gif](pontes.gif) <br> 
  
  3. No processo que sucede é feita a filtragem por um capacitor que carrega rapidamente e descarrega lentamente, de forma que o ruído residual, também conhecido como RIPPLE, seja o menor possível, fazendo com que o sinal pulsante fique o mais próximo possível de um sinal linear de corrente contínua. <br><br>
  ![Filtragem](filtragem.png) <br> 
  
  4. Por último teremos a regulação. Nessa etapa, iremos utilizar um regulador, dispositivo que funciona de forma a linearizar o máximo possível a saída da fonte na tensão desejada, retirando o RIPPLE ainda deixado pelo capacitor na etapa anterior. Dessa forma, por mais que entre uma tensão pulsante ou com o valor superior ao desejado, na entrada do regulador, esse irá apresentar em sua saída uma tensão de valor constante e fixo.<br>
  Para o projeto, o regulador será composto por um resistor e um diodo zener, conectado ao contrário, em que o resistor irá reduzir a corrente que chega no diodo, para não danificá-lo, que, após uma tensão zener aplicada, irá permitir apenas este valor de tensão passar, barrando o excedente e oferecendo uma corrente contníua.<br>
  Para o projeto os valores escolhidos para o diodo Zener, classificado por sua tensão de ruptura e potência máxima, foram de 13V e 1W, de acordo com a especificação do trabalho. <br><br>
  
  ![Zener](zener.png) 
  ![Saida](saida.png) <br><br>
  
# Cálculos 

# Valores 

| Quantidade | Componente | Valor uni. | Valor Tot|
|--------------|------------|-------|--------|
| 06 | Diodo Retificador 10A10 | 0,99 | 5,94 |
| 02 | Capacitor 560μF25V | 0,95 | 1,90 |
| 04 | Diodo Zener 13V 1W 1N4743 | 0,23 | 0,92 |
| 10 | Resistor 1K 5% 14W | 0,04 | 0,4 |
| 10 | Resistor 1K8 5% 2W | 0,04 | 0,4 |  
| 04 | Resistor 2K 5% 14W | 0, 05 | 0,2 |
| 04 | Transistor npn 2N2222 | 0,5 | 2,00 |    
| 01 | Potenciômetro linear 5K | 1,99 | 1,99 |
| 03 | Led 5mm vermelho | 0,15 | 0,45 |
|**Total:** | | | **38,20** |

  
# Circuito no Falstad 

![circuito](https://github.com/pijuma/Fonte-Tensao-Simoes/blob/main/circuito.jpg) <br> 

Link do circuito: https://tinyurl.com/2eja2aah <br> 

# PCB no EAGLE

# Fontes de pesquisa 

Aulas do Professor Simões: https://gitlab.com/simoesusp/disciplinas/-/tree/master/SSC0180-Eletronica-para-Computacao
https://electronicsclub.info/powersupplies.htm 
<br>
# Responsáveis 

Shogo Shima - 12675145 <br>
Jesus Sena Fernandes - <br>
Letícia Raddatz Jönck - 14589066<br>  
Pietra Gullo Salgado Chaves - 14603822<br>
José Carlos - <br>
