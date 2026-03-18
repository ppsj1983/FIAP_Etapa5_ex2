# FIAP - Faculdade de Informática e Administração Paulista

<br>

# Trabalho Etapa 5 exercicio 2 
## *Cap 1 - FarmTech na Era da Cloud Computing*

## Nome do grupo

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/paulo-pereira-de-souza-junior-mba-msc-0b497825/">Paulo Pereira de Souza Junior</a>

## 📜  Análise exploratória
A base crop_yield apresenta a seguinte estrutura de informações:
- Cultura: o nome da safra para a qual o rendimento está sendo medido.
- Precipitação (mm dia 1): a quantidade de chuva em milímetros por dia.
- Umidade específica a 2 metros (g/kg): a quantidade de vapor de água no ar por quilograma de ar seco a uma altura de 2 metros acima do solo.
- Umidade relativa a 2 metros (%): a quantidade de vapor de água no ar como uma porcentagem da quantidade máxima de vapor de água que pode ser mantida a uma determinada temperatura e pressão.
- Temperatura a 2 metros (ºC): a temperatura em graus Celsius a uma altura de 2 metros acima do solo.
- Rendimento: a quantidade de rendimento em toneladas por hectare.

<p align="center">
<img width="384" height="96" alt="Image" src="https://github.com/user-attachments/assets/aa80a9eb-71d0-4932-9fdf-c2595e412823" /></a></p>

Podemos observar na coluna Crop a quantificação de 4 tipos de colheitas com 39 registros, sendo:
*Crop*
- Cocoa, beans       39
- Oil palm fruit     39
- Rice, paddy        39
- Rubber, natural    3
<p align="center">
<img width="147" height="75" alt="Image" src="https://github.com/user-attachments/assets/766d63e6-feb4-477b-974b-4db6d2652f8c" /></a></p>

Tratando-se do tipo da dado, identificamos informações classificadas como object, float64 e int64. Definição por coluna, a seguir:
- Crop                                  [object] 
- Precipitation (mm day-1)              [float64]
- Specific Humidity at 2 Meters (g/kg)  [float64]
- Relative Humidity at 2 Meters (%)     [float64]
- Temperature at 2 Meters (C)           [float64]
- Yield                                 [int64] 

<p align="center">
<img width="197" height="115" alt="Image" src="https://github.com/user-attachments/assets/04c1f381-68e2-494a-90b1-39f8ccd2d25a" /></a></p>

No resumo, as médias observadas indicam similaridade entre as variáveis climatológicas. Entretanto, a variável Yield apresenta variação entre as colheitas avaliadas, evidenciando que as condições climatológicas exercem efeitos distintos conforme o tipo de colheita.
- Precipitation (mm day-1) [float64] media = 2486,49
- Specific Humidity at 2 Meters (g/kg) [float64] media = 18,20
- Relative Humidity at 2 Meters (%) [float64] media = 84,73
- Temperature at 2 Meters (C) [float64] media = 26,18

- Yield [int64] Cocoa, beans media = 8883,1
- Yield [int64] Oil palm fruit media = 175804,6
- Yield [int64] Rice, paddy media = 32099,66
- Yield [int64] Rubber, natural media = 7824,89

<p align="center">
<img width="392" height="90" alt="Image" src="https://github.com/user-attachments/assets/ac0e6c30-ec7f-4d96-b3e5-9d1f47072d6d" /></a></p>

Utilizando os algoritmos KNN, SVM e Random Forrest, identificamos que todos os modelos ficaram acima de 88%, com destaque para o Random Forest com 92%
<p align="center">
<img width="343" height="248" alt="Image" src="https://github.com/user-attachments/assets/d441f531-c01d-43ba-83f7-2cd5d5c5322c" /></a></p>

Utilizando o Randomized Search para encontrar os melhores hiperparâmetros para cada modelo, observamos uma queda no desempenho do Random Forest para 87%, o algoritmo atingiu 85% de acuracia
<p align="center">
<img width="1107" height="306" alt="Image" src="https://github.com/user-attachments/assets/9d844186-365a-4817-89d6-d0f4ba13e51b" /></a></p>

## 🗃 Histórico de lançamentos

* 0.1.0 - 10/11/2025
    *

## 📋 Licença

