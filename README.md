# Simulação do sistema solar

## Descrição
Esse projeto busca simular o funcionamento do nosso sistema solar e suas órbitas através do cálculo da interação gravitacional entre cada corpo.
As trajetórias foram simplificadas de forma a descrever movimentos circulares em função da simplificação dos cálculos referentes.

## Requisitos
Para executar esse projeto, será necessário possuir o [Python](https://www.python.org/) e o [pip](https://pip.pypa.io/en/stable/)
## Instalação
- Clone o repositório
```
$ git clone https://github.com/gustavorspires/trabalho-de-fisica-brocolis.git
$ cd trabalho-de-fisica-brocolis
```
- Ative a venv
```
$ source .venv/bin/activate
```
- Instale as dependências e execute o programa
```
$ pip install -r requirements.txt
$ python3 sistemaSolar.py
```
## Cálculos
### Força gravitacional
Foi utilizada a Lei Universal da Gravitação de Newton

$$ \vec{F_g} = \frac{Gm_2m_1}{||\vec{r_2} - \vec{r_1}||^2}(r_2 - r_1)$$  

São somadas as forças gravitacionais de um corpo com todos os outros para adquirir a força resultante ativa nele.

### Aceleração

$$ \vec{a} = \frac{\vec{F_r}}{m} $$

### Posição
Foi utilizada o método de Integração de Verlet para o cálculo da trajetória dos astros:

$$\vec r(t+\Delta t) = 2\vec r(t) - \vec r(t-\Delta t) + \vec a(t)\Delta t^2 $$

### Velocidade inicial
O versor da velocidade inicial dos astros é sempre calculado como o vetor perpendicular no sentido horário, o modulo é dado por:

$$ mv^2 = \frac{GMm}{d^2} \therefore v = \sqrt{\frac{GM}{d^2}} $$



