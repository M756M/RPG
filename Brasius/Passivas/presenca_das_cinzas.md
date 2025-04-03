# Sumário

- [Terminologia](#terminologia)
- [Definições](#definições)
- [Condições Especiais](#condições-especiais)
- [Ações de Passiva](#ações-de-passiva)

# Terminologia

- <h6>Alvo: Qualquer ser, animado ou não, que é selecionado pelo usuário para sofrer as consequências de uma ação;<h6>
- <h6>Turno: Período de tempo onde um personagem (jogador ou não) executa suas ações. Cada turno dura, em tempo cronológico, 6 segundos;</h6>
- <h6>Rodada: O tempo que demora para todos os jogadores e inimigos de um combate executarem seus turnos. Cada rodada dura, em tempo cronológico, 1 minuto;<h6>
- <h6>Rodada Relativa: O turno que um personagem executa em toda rodada;<h6>

# Definições

### Mecânicas Básicas

[`Ember Approach`][Stand] possui $3$ grandezas que controlam seu funcionamento:

- $\text{Densidade }\large{[\frac{\text{mg}}{\text{L}}]}$<br>
- $\text{Raio de Dispersão }[\text{m}]$<br>
- $\text{Ganho de Densidade }\large{[\frac{\text{mg}}{\text{L} \cdot \text{min}}]}$<br>

Para que a leitura seja breve, essas grandezas  serão atribuídas aos símbolos $C$, $r$ e $\large{\frac{dC}{dt}}$, respectivamente.

$C$ se refere a densidade das cinzas de [`Ember Approach`][Stand] presentes no ar na `Rodada` atual, enquanto $\large{\frac{dC}{dt}}$ se refere ao quanto de densidade se ganha por `Rodada`.<br>
Já $r$ se refere, essencialmente, ao quão longe as cinzas conseguem se espalhar.

$r$ será usado para definir a distância em que esta passiva tem efeito. Caso um `Alvo` arbitrário esteja a mais que $r$ metros do usuário, essa passiva não possui efeito sobre ele.<br>

$C$ será usada, majoritariamente, como uma moeda de troca para habilidades e técnicas, e como um marco para passivas.<br>

$\large{\frac{dC}{dt}}$ será usado puramente para incrementar $C$ no **início** da `Rodada Relativa` do usuário.

### Relações das grandezas

As grandezas de [`Ember Approach`][Stand] estão relacionadas tanto aos [`Atributos do Stand`][Atributos_Stand] quanto ao número de `Rodadas` passadas desde o início do combate.

Ao ativar o [`Martírio`](#martírio) de [`Ember Approach`][Stand], as grandezas tomam os seguintes valores:

$$C = 250 \cdot (1 + \text{Modificador de Poder})$$
$$\frac{dC}{dt} = 50 \cdot (1 + \text{Modificador de Velocidade})$$
$$r = 15 \cdot (1 + \text{Modificador de Alcance})$$

Esses valores são chamados **grandezas iniciais** e serão indicados, respectivamente, por $C_0$, $\frac{dC}{dt}_0$ e $r_0$.

Como $C$ é acumulado ao decorrer das `Rodadas`, pode-se calcular a quantidade total de $C$ obtida desde o início do combate:
$$C_{total} = C_0 + t \cdot \frac{dC}{dt}_0$$
Onde $t$ é o número de `Rodadas` decorridas desde o início do combate.

# Condições Especiais

### Marcação Flamejante

Aplicada para todos os seres que estão sob a área de efeito dessa passiva.<br>
Qualquer habilidade ou técnica de [`Ember Approach`][Stand] que tenha como `Alvo` um ser afetado por essa condição reduz passivamente a `Classe de Armadura` dele pelo $\text{Modificador de Precisão}$ do usuário.

### Falta de Ar

Aplicada para todos os seres que estão sob a área de efeito dessa passiva durante estágios superiores a [`Martírio`]

### Petrificação Desacelerada

# Ações de Passiva

Ao invocar [`Ember Approach`][Stand], o usuário pode escolher agir em relação a sua [`Presença das Cinzas`]. Ao escolher uma ação, o usuário altera o estado dessa passiva, provocando efeitos que serão listados em suas seções.

### Martírio

Ao agir em [`Martírio`], o usuário cria uma área tridimensional com suas cinzas. Tudo que estiver dentro dessa área fica sob efeito de [`Presença das Cinzas`].

Conforme o martírio do usuário cresce, sua presença adota diferentes naturezas. As naturezas do martírio provocam os seguintes efeitos:

- #### Martírio Funcional
- #### Martírio Acentuado
- #### Martírio Profundo
- #### Martírio Intolerável

### Eutimia

Desativar a barreira

### Perseverança

Parar a barreira

### Efemeridade

Transmutar a barreira

[Stand]: ../Stand/geral.md
[Atributos_Stand]: ../Stand/atributos.md
[Atributos_Personagem]: ../Personagem/atributos.md