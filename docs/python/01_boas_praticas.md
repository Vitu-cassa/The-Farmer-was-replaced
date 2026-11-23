# 🐍 Guia de Boas Práticas em Python

Este documento visa ser um guia de boas práticas para escrever códigos mais limpos e organizados. Algumas das práticas que consideraremos para os programas foram tiradas de fontes como o livro *Fluent Python* e as PEPs (*Python Enhancement Proposals*).

O objetivo é sempre verificar as possibilidades de melhoria de código em todas as formas possíveis, como performance, legibilidade, documentação, estética e afins. Considerem sempre aplicar algumas das normas descritas aqui, não importando como os programas estão classificados — ou seja, mesmo um script colocado como "iniciante" pode e deve ter algumas das práticas descritas aqui, principalmente as estéticas.

Contudo, como qualquer coisa por aqui, e seguindo as próprias linhas da PEP 8, nem sempre a consistência de parâmetros (principalmente os descritos aqui) será aplicável. Portanto, quando não for possível realizar alguma dessas práticas, veja exemplos, peça opiniões e use seu próprio julgamento para aplicar, ou não, algumas das sugestões. Em uma tradução livre do trecho da PEP 8 que comenta algumas exceções:

> **Algumas boas razões para ignorar certas diretrizes:**
> 1. Quando a aplicação da diretiva tornar o código menos legível, mesmo para alguém que esteja habituado com a leitura de programas que utilizem essa PEP;
> 2. Para ser consistente com o ambiente do código, que talvez possa quebrar (devido ao seu legado), apesar de isso ser uma boa oportunidade para arrumar a bagunça feita no passado;
> 3. O código em questão veio antes da publicação destas diretrizes e não existam razões para a modificação do código;
> 4. Quando o código precisa permanecer compatível com versões antigas do Python que não suportam as *features* necessárias para seguir as diretrizes.

---

## 1. Convenções Básicas e Estilo

A primeira impressão de um código vem da sua organização visual. Isso garante que praticamente qualquer pessoa — seja alguém que nunca leu o código ou o "você do futuro" — possa se localizar e compreender com mais facilidade o que cada parte do programa faz.

### 1.1. Nomes de Arquivos
- Utilize apenas letras minúsculas, números e sublinhados (`snake_case`).
- **Não** utilize espaços, acentos ou caracteres especiais.
- **Regra de transparência:** Caso o script tenha sido gerado com apoio direto de IA, adicione o prefixo ou sufixo `ia`.

| ✅ Nome válido | ❌ Nome inválido | Observação |
| :--- | :--- | :--- |
| `colheita_abobora.py` | `colheita abobora.py` | Espaços dificultam comandos no terminal e importações |
| `plantio_cenoura.py` | `plantio-cenoura.py` | Hífens não são válidos para importar módulos em Python |
| `mineracao_ouro.py` | `MINERACAO_OURO.py` | Letras maiúsculas são reservadas para constantes |
| `ia_colheita_abobora.py`<br>`colheita_abobora_ia.py` | `colheita_abobora.py`<br>*(quando gerado por IA)* | Sinaliza a participação de IA no arquivo |

---

### 1.2. Indentação e Espaçamento
Para diversas linguagens, a indentação é apenas estética (embora altamente recomendada). Porém, além de manter a organização visual, em Python a indentação é o que indica para o interpretador o que faz parte do bloco de código dentro de uma função ou estrutura e o que não faz — tornando-se obrigatória para o funcionamento do programa.

Para a indentação e o espaçamento, consideraremos as seguintes diretrizes:
- **4 espaços por nível:** Não misture tabulações (`Tab`) com espaços. Configure seu editor para converter a tecla `Tab` em **4 espaços**.
- **Espaços em operadores:** Coloque um espaço antes e depois de operadores matemáticos e de comparação.

  | ❌ Evitar | ✅ Aplicar |
  | :---: | :---: |
  | `a=10` <br> `if x==y:` | `a = 10` <br> `if x == y:` |

- **Comprimento de linha:** Procure manter as linhas curtas para facilitar a leitura lado a lado sem rolagem horizontal.
- **Linhas em branco:** Use **1 linha em branco** para separar blocos lógicos dentro de um algoritmo e **2 linhas em branco** antes e depois da definição de funções.

```python
# ❌ Evite: código colado e operadores sem espaço
def verificar_agua():
    nivel=get_water()
    if nivel<0.5:
        use_item(Items.Water_Tank)
def colher_recurso():
    if can_harvest():
        harvest()


# ✅ Prefira: 2 linhas entre funções, 1 linha entre blocos lógicos e espaços nos operadores
def verificar_agua():
    nivel = get_water()

    if nivel < 0.5:
        use_item(Items.Water_Tank)


def colher_recurso():
    if can_harvest():
        harvest()
```

---

### 1.3. Variáveis, Funções e Constantes
Variáveis e funções devem ser escritas/declaradas no estilo `snake_case`, enquanto constantes devem ser declaradas como `UPPER_SNAKE_CASE`.
Sobre as diretrizes de decisão de nomes:
- **Variáveis:** Use substantivos descritivos que indiquem o que está armazenado. Evite letras soltas como `a`, `b` ou `tmp`, exceto em coordenadas (`x`, `y`) ou contadores muito curtos.
- **Funções:** Use verbos no infinitivo que expressem claramente a ação executada.
- **Constantes:** Valores fixos de configuração que não mudam durante a execução do script devem ser escritos em letras maiúsculas e declarados no topo do arquivo.

| Elemento | Padrão | Forma Gramatical | ❌ Evite | ✅ Prefira |
| :--- | :--- | :--- | :--- | :--- |
| **Variável** | `snake_case` | Substantivo | `t`, `x1`, `flag` | `tamanho_fazenda`, `posicao_x`, `solo_arado` |
| **Função** | `snake_case` | Verbo no infinitivo | `agua()`, `faz_tudo()`, `check()` | `irrigar_solo()`, `mover_para_origem()`, `verificar_colheita()` |
| **Constante** | `UPPER_SNAKE_CASE` | Substantivo fixo | `min_agua = 0.5` | `NIVEL_MINIMO_AGUA = 0.5` |

```python
# ❌ Evite: constante em minúsculo, valor fixo não declarado, função sem verbo e variáveis genéricas
cultura = Entities.Pumpkin


def solo():
    t = get_world_size()

    for _ in range(t):
        a = get_water()

        if a < 0.5:
            use_item(Items.Water_Tank)

        if can_harvest():
            harvest()
            plant(cultura)


# ✅ Prefira: constantes em UPPER_SNAKE_CASE no topo, função com verbo e variáveis descritivas
NIVEL_MINIMO_AGUA = 0.5
CULTURA_ATUAL = Entities.Pumpkin


def gerenciar_solo():
    tamanho_fazenda = get_world_size()

    for _ in range(tamanho_fazenda):
        nivel_agua = get_water()

        if nivel_agua < NIVEL_MINIMO_AGUA:
            use_item(Items.Water_Tank)

        if can_harvest():
            harvest()
            plant(CULTURA_ATUAL)
```
