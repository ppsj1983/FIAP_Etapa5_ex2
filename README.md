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

Para fins de simulação, analisou-se a dispersão da variável Yield em relação à Precipitation (mm day). Observou-se que a colheita do tipo *Oil palm fruit* apresenta valores superiores quando comparada às demais plantações.
<p align="center">
<img width="278" height="261" alt="Image" src="https://github.com/user-attachments/assets/f2b8b9dc-7d51-4f60-8ab4-a432804158c0" /></a></p>

O grafico boxplot tambem apresenta desvio superior médio para a colheira  *Oil palm fruit*, dados consolidados variavel Yield
<p align="center">
<img width="441" height="327" alt="Image" src="https://github.com/user-attachments/assets/fc6df31b-344e-4368-83a2-f0ec330e202a" /></a></p>

Para a análise de clusterização, utilizou-se o algoritmo K-Means. Como resultado, a colheita Oil palm fruit apresentou maior distanciamento em relação às demais, sendo alocada no cluster 0. Já as colheitas Cocoa, Beans e Rubber (natural) foram agrupadas no cluster 2, indicando maior proximidade entre si considerando os dados observados.
<p align="center">
<img width="292" height="364" alt="Image" src="https://github.com/user-attachments/assets/784363e0-9ee9-417f-891d-78b80f9210ab" /></a></p>

## 📜 Predição

Para fins de simulação, utilizou-se a colheita Oil palm fruit, aplicando-se cinco algoritmos de predição: 
- Random Forest Regressor 
- Decision Tree
- Linear Regressor 
- KNN Regressor
- SVM Regressor

Para a projeção e avaliação da assertividade dos modelos, foram adotadas variáveis de entrada fixas nas simulações, a saber: 
- Precipitation (mm day⁻¹) = 2486 
- Specific Humidity at 2 Meters (g/kg) = 84
- Relative Humidity at 2 Meters (%) = 18 
- Temperature at 2 Meters (°C) = 26.
<p align="center">
<img width="315" height="54" alt="Image" src="https://github.com/user-attachments/assets/9d259ddc-ca26-4b16-8de9-f20abc399a52" /></a></p>

Dentre os algoritmos avaliados, o KNN Regressor apresentou o menor desvio, obtendo um valor de R² score igual a 0,39, indicando desempenho superior em relação aos demais modelos testados.
<p align="center">
<img width="346" height="209" alt="Image" src="https://github.com/user-attachments/assets/81dc390d-34c4-41d2-b0d6-6bd7ac437eb2" /></a></p>

## *Cap 1 - Machine Learning hospedada em uma estrutura de computação em nuvem*

## 📜  Configuração de Serviços AWS

Especificações do EC2: Instancia Compartilhada (onde múltiplos usuários da AWS executam suas máquinas virtuais no mesmo hardware físico)

Nome da instância: Família T3 (como a t3.micro) (2 CPUs, 1 GiB de RAM e Desempenho da rede Up to 5 Gigabit)

Amazon Elastic Block Store (EBS): SSD de uso geral (gp3) com 50 gb

## 🗃 Histórico de lançamentos

* 0.1.0 - 18/03/2026
    *

## 📋 Licença

