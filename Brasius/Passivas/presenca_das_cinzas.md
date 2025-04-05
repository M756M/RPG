# Sumário

- [Terminologia](#terminologia)
- [Descrição Geral](#descrição-geral)
- [Definições](#definições)
- [Condições Especiais](#condições-especiais)
- [Ações de Passiva](#ações-de-passiva)

# Terminologia

- <h6>Alvo: Qualquer ser, animado ou não, que é selecionado pelo usuário para sofrer as consequências de uma ação;<h6>
- <h6>Turno: Período de tempo onde um personagem (jogador ou não) executa suas ações. Cada turno dura, em tempo cronológico, 6 segundos;</h6>
- <h6>Rodada: O tempo que demora para todos os jogadores e inimigos de um combate executarem seus turnos. Cada rodada dura, em tempo cronológico, 1 minuto;<h6>
- <h6>Rodada Relativa: O turno que um personagem executa em toda rodada;<h6>

# Descrição Geral

A ideia simplificada dessa passiva é uma barreira de cinzas que cerca uma determinada área, que é abordada em [`Definições -> Mecânicas Básicas`](#mecânicas-básicas). Essa barreira altera o ambiente em seu interior, cuja intensidade progride de acordo com o passar das `Rodadas`.

A ideia abstrata dssa passiva é, essencialmente, a manifestação física do tormento que o usuário sente em relação aos eventos que decorreram em sua vida. Uma grande característica do usuário é sua filosofia de vida, a qual ele tenta se aderir tanto conscientemente quanto inconscientemente. Portanto, é mais do que justo que, como ser humano, ele falhe em fazer esse processo da maneira mais otimizada. Essa ineficácia pode, eventualmente, fazê-lo duvidar de sua crença ou até mesmo achá-la inadequada.

De acordo com isso, é correto afirmar que o personagem sente uma aflição de intensidade variada. **Portanto, a intensidade da barreira será atribuída ao nome de** `Aflição`.

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

Aplicada para todos os seres que estão sob a `Área de Efeito` dessa passiva durante `Aflições` superiores a `Martírio Opressor`.
Indivíduos com `Falta de Ar` sentem muita dificuldade para respirar, mas não estão necessariamente sufocando.<br>

`Falta de Ar` causa $\text{1d6}$ de dano por `Rodada Relativa` do afetado e diminui seu `Bônus de Teste` perante `Testes de Resistência` de $\text{Fortitude}$ em $-2$

### Petrificação Desacelerada

Aplicada para todos os seres que estão sob a `Área de Efeito` dessa passiva durante `Aflições` superiores a `Martírio Sufocante`.
Indivíduos com `Petrificação Desacelerada` tem partes de seu corpo se petrificando ao decorrer dos turnos, com o ápice da petrificação sendo a `Petrificação Total`.

A cada `Rodada Relativa` do usuário, o estágio de `Petrificação Desacelerada` avança em $1$, com os efeitos listados abaixo:

- **Petrificação Inicial**: O alvo começa a sentir as suas articulações endurecendo, fazendo com que locomoção seja diminuída em $3\text{m}$.
- **Petrificação Parcial**: O alvo sente seu corpo se petrificando, sofrendo desvantagem em testes de $\text{Destreza}$ e $\text{Velocidade}$ em $-2$ e tendo sua locomoção diminuída em $5\text{m}$.
- **Petrificação Total**: O alvo tem seu corpo totalmente petrificado externamente, fazendo com que ele perca $1$ `Rodada Relativa`.

# Ações de Passiva

Ao invocar [`Ember Approach`][Stand], o usuário pode escolher agir em relação a sua `Aflição`. Ao escolher uma ação, o usuário altera o estado dessa passiva, provocando efeitos que serão listados em suas seções.

### Martírio

Ao agir em `Martírio`, o usuário cria uma área tridimensional com suas cinzas. Tudo que estiver dentro dessa área fica sob efeito dessa passiva.

Com o acúmulo de $C$, a `Aflição` do usuário aumenta, afetando o ambiente de diferentes formas:

#### Martírio Funcional

Ocorre quando $C$ atinge $500 \frac{\text{mg}}{\text{L}}$.

Nessa `Aflição`:

- Todos os seres dentro da `Área de Efeito` sofrem `Marcação Flamejante`.
- As Habilidades e Técnicas de Ember Approach podem ser usadas na intensidade `Cinzas Leves`.
- Todos os personagens inimigos dentro da `Área de Efeito` passam a sofrer $\text{Desprevenido}$, exceto o usuário.
- O usuário tem sua Margem de Crítico diminuída em $1$.
- O usuário ganha $+3$ em $\text{Testes}$ de $\text{Furtividade}$.

#### Martírio Asmático

Ocorre quando $C$ atinge $1000 \frac{\text{mg}}{\text{L}}$.

Nessa `Aflição`:

- O terreno dentro da `Área de Efeito` se torna $\text{Terreno Difícil}$ para todos os seres dentro da barreira, exceto o usuário.
- As Habilidades e Técnicas de Ember Approach podem ser usadas na intensidade `Brasas Densas`.
- Todos os personagens inimigos dentro da `Área de Efeito` passam a sofrer $\text{Envenenado}$, exceto o usuário.
- O usuário tem sua Margem de Crítico diminuída em $2$.
- O usuário ganha $+6$ em $\text{Testes}$ de $\text{Furtividade}$.

#### Martírio Opressor

Ocorre quando $C$ atinge $1500 \frac{\text{mg}}{\text{L}}$.

Nessa `Aflição`:

- As Habilidades e Técnicas de Ember Approach podem ser usadas na intensidade `Neblina Flamejante`.
- Todos os personagens inimigos dentro da `Área de Efeito` passam a sofrer $\text{Cegado}$, exceto o usuário.
- Caso um ser tente sair da `Área de Efeito`, é preciso que ele tenha sucesso em um $\text{Teste}$ de $\text{Atletismo DT }15$
- O usuário tem sua Margem de Crítico diminuída em $3$.
- O usuário ganha $+9$ em $\text{Testes}$ de $\text{Furtividade}$.

#### Martírio Sufocante

Ocorre quando $C$ atinge $2000 \frac{\text{mg}}{\text{L}}$.

Nessa `Aflição`:

- Não é possível sair ou entrar na `Área de Efeito`.
- As Habilidades e Técnicas de Ember Approach podem ser usadas na intensidade `Desabrochar da Fênix`.
- Todos os personagens inimigos dentro da `Área de Efeito` passam a sofrer $\text{Vulnerável}$ e `Falta de Ar`, exceto o usuário.
- O usuário passa a sofrer $\text{Envenenado}$ e $\text{Foco}$.
- Todos os seres aliados, exceto o usuário, podem fazer um $\text{Teste}$ de $\text{Fortitude DT }12$ para anular as condições $\text{Vulnerável}$ e `Falta de Ar`.
- O usuário tem sua Margem de Crítico diminuída em $4$.
- O usuário ganha $+12$ em $\text{Testes}$ de $\text{Furtividade}$.

#### Martírio Asfixiante

Ocorre quando $C$ atinge $2500 \frac{\text{mg}}{\text{L}}$.

Nessa `Aflição`:

- As Habilidades e Técnicas de Ember Approach podem ser usadas na intensidade `Ego Cinzento`.
- Todos os personagens inimigos dentro da `Área de Efeito` passam a sofrer `Petrificação Desacelerada`, exceto o usuário.
- O usuário tem sua Margem de Crítico diminuída em $5$.
- O usuário ganha $+15$ em $\text{Testes}$ de $\text{Furtividade}$.

### Eutimia

Desativar a barreira

### Perseverança

Parar a barreira

### Efemeridade

Transmutar a barreira

[Stand]: ../Stand/geral.md
[Atributos_Stand]: ../Stand/atributos.md
[Atributos_Personagem]: ../Personagem/atributos.md