# Caleidoscópio Digital

## Sobre o Projeto
Este projeto representa meu primeiro script no mundo das animações digitais, explorando como conceitos matemáticos simples podem se transformar em padrões visuais. Utilizando Python e bibliotecas como Matplotlib e NumPy, criei três animações distintas que simulam efeitos visuais inspirados em caleidoscópios.

## Objetivo
Demonstrar como equações matemáticas podem gerar arte visual animada, servindo como um projeto introdutório à programação criativa e visualização de dados dinâmicos.

## Fundamentos Matemáticos
### Funções Principais Utilizadas:

1. Funções Trigonométricas (seno e cosseno):

```python
np.sin() e np.cos()
```

- Criam padrões ondulatórios periódicos
- Controlam o movimento e oscilação das formas
- Geram interferências visuais quando combinadas

2. Coordenadas Polares:

```python
R = np.sqrt(X² + Y²)  # Distância do centro
θ = np.arctan2(Y, X)  # Ângulo em relação ao centro
```

- Permitem criar padrões radiais e circulares
- Facilitam animações concêntricas

3. Combinação Não-Linear:

```python
combined = np.tanh(layer1 * 0.8 + layer2 * 0.6)
```

- Suaviza e limita os valores entre -1 e 1
- Cria transições mais orgânicas

4. Máscaras e Gradientes:

```python
mask = np.exp(-(R - np.pi*0.7)² / 2)
```

- Controlam a intensidade dos efeitos
- Criam bordas suaves e transições

## Animações

1. Ondas Concêntricas
Foco: Simplicidade e fluidez

Técnicas:
- Combinação linear de 4 padrões de onda
- Máscara circular definida
- Paleta de cores HSV uniforme

Equação Principal:

```python
combined = pattern1*0.4 + pattern2*0.3 + pattern3*0.2 + pattern4*0.3
```

2. Ondas Intensas
Foco: Complexidade e caos controlado

Diferenças principais:
- Combinação não-linear (tanh + sin)
- Múltiplos mapas de cores por região (6 setores)
- Distorção de onda aplicada aos padrões
- Máscara com borda gaussiana (suave)

Característica única: Efeito de pulso radial que varia com o tempo

```python
pulse = np.sin(R * 3 - t * 5) * 0.3 + 0.7
```

3. Padrões Geométricos
Foco: Estrutura e simetria

Diferenças principais:
- Padrão hexagonal explícito
- Sistema de coordenadas rotacionado
- Anéis concêntricos pulsantes
- Gradiente de cor baseado em posição radial

Inovação: Rotação de coordenadas para criar movimento orgânico

```python
X_rot = X*cos(ângulo) - Y*sin(ângulo)
Y_rot = X*sin(ângulo) + Y*cos(ângulo)
```

## Como Executar

```bash
# No Google Colab ou Jupyter Notebook
1. Execute todas as células em sequência
2. Os GIFs serão gerados automaticamente
3. Salve as imagens clicando com botão direito

# Parâmetros ajustáveis:
- num_frames: Controla a suavidade da animação
- num_waves: Número de ondas concêntricas
- Velocidade: Ajuste os multiplicadores de tempo (t)
```

## Tecnologias Utilizadas
- Python 3.x
- NumPy: Cálculos matemáticos vetorizados
- Matplotlib: Geração de gráficos e animações
- PIL/ImageIO: Exportação para GIF
- Google Colab: Ambiente de execução
