# 🐍 Guia de Boas Práticas em Python

Este documento visa ser um guia de boas práticas para escrever códigos mais limpos e organizados.
Algumas das práticas que consideraremos para os programas foram tiradas de fontes como o livro "Fluent in Python" e as PEPs (Python Enhancement Proposal).
O objetivo é sempre verificar as possibilidades de melhoria de código em todas as formas possíveis, como performance, legibilidade, documentação, estética e afins.
considerem sempre aplicar algumas das normas descritas aqui, não importando como os programas estão classificados, ou seja, mesmo um script colocado como "iniciante" pode
e deve ter algumas das praticas descritas aqui, principalmente as esteticas.

Contudo, como qualquer coisas por aqui, e seguindo as próprias linhas da PEP 8, nem sempre a consistência de parâmetros, principalmente dos descritos aqui, sejam aplicaveis,
portanto, quando não for possível realizar alguma dessas práticas, veja exemplos, peça opiniões e use seu próprio julgamento para aplicar, ou não, algumas das sugestões.
em uma tradução livre do trecho que comenta algumas exceções:

> Algumas boas razões para ignorar certas diretrizes:
> 1. Quando a aplicação da diretiva tornar o código menos legivel, mesmo para alguém que esteja habituado com a leitura de
> programas que utilizem essa PEP;
> 2. para ser consistente com o hambiente do codigo, que talvez possa quebgrar (devido ao seu legado), apesar disso ser uma
> boa oportunidade para arrumar a bagunça feita no passado;
> 3. O código em questão veio antes da publicação destas diretrizes e não existam razões para a modificação do código;
> 4. Quando o código precisa permanecer compatível com versões antigas do Python que não suportam as "features"
> necessárias para seguir as diretrizes.
>

---

## 1. Convenções Básicas e Estilo

A primeira impressão de um código vem da sua organização visual. Isso garante que praticamente qualquer pessoa, seja
alguém que nunca leu o código como o "você do futuro" possam se localizar e compreender com mais facilidade o que
cada parte do programa faz.

### 1.1. Nomes de Arquivos
* Utilize apenas letras minúsculas, números e sublinhados (`snake_case`).
***Não** utilizar acentos ou caracteres especiais.
* **Regra de transparência:** Caso o script tenha sido gerado com apoio direto de IA, adicione o prefixo ou sufixo `ia` (ex.: `ia_colheita_abobora.py` ou `colheita_abobora_ia.py`).

| Nome valido | nome invalido |
| :--: | :--: |
| colheita_abobora.py | colheita abobora.py <br> colheita-abobora.py <br> COLHEITA_ABOBORA.py |

### 1.2. Indentação e Espaçamento
Para diversas linguagens, a indentação é algo estético (e altamente recomendado), porém, além de manter a estetica,
em Python, a indentação é o que indica para o interpretador o que faz parte do bloco de código dentre de uma função ou estrutura
e o que não faz, tornando-se obrigatória para o funcionamento do código.
Para a indentação e espaçamento, iremos considerar as seguintes diretrizes:
* **4 espaços por nível:** Não misture tabulações (`Tab`) com espaços. Configure seu editor para converter a tecla `Tab` em **4 espaços**.
* **Linhas em branco:** Use uma linha em branco para separar blocos lógicos dentro de um algoritmo e duas linhas em branco antes e depois da definição de funções.
* **Espaços em operadores:** Coloque um espaço antes e depois de operadores matemáticos e de comparação (`a = 10`, `if x == y:`), mantendo o código arejado.

### 1.3. Variáveis, Funções e Constantes

* **Variáveis (`snake_case`):** Use substantivos descritivos que indiquem o que está armazenado (ex.: `posicao_x`, `total_feno`, `solo_arado`). Evite letras soltas como `a`, `b` ou `tmp`, exceto em coordenadas (`x`, `y`) ou contadores muito curtos.
* **Funções (`snake_case`):** Use verbos no infinitivo que expressem claramente a ação executada (ex.: `irrigar_solo()`, `mover_para_origem()`, `colher_tudo()`).
* **Constantes (`UPPER_SNAKE_CASE`):** Valores fixos de configuração que não mudam durante a execução do script devem ser escritos em letras maiúsculas e declarados no topo do arquivo.

```python
# ❌ Evite: nomes genéricos, falta de espaçamento e valores fixos espalhados
t=get_world_size()
for i in range(t):
    if get_water()<0.5:
        use_item(Items.Water_Tank)

# ✅ Prefira: intenção clara, espaçamento adequado e constantes no topo
NIVEL_MINIMO_AGUA = 0.5
tamanho_fazenda = get_world_size()

for passo in range(tamanho_fazenda):
    if get_water() < NIVEL_MINIMO_AGUA:
        use_item(Items.Water_Tank)
