# 🚜 Algoritmos com The Farmer Was Replaced

Repositório criado para a prática de algoritmos e escrita de programas com Python. 

O objetivo é criar um ambiente onde as pessoas possam interagir com programação através do jogo "The Farmer Was Replaced" e sua DLC "The Miner Was replaced". E quem sabe, formar uma comunidade que queira otimizar os códigos a ponto de subir na rankeada — sendo este último objetivo apenas uma consequência. Apenas divirtam-se!

## 📂 Arquitetura (Em Construção)

As pastas/diretórios estão, atualmente, organizados da seguinte forma:

```text
.
├── 📄 README.md
├── 📚 docs/
│   ├── 🚜 jogo/
│   │   ├── 💻 Programacao/
│   │   │   ├── 📝 01_comentarios.md
│   │   │   └── 🔀 fluxo_de_controle/
│   │   │       ├── 📝 01_break.md
│   │   │       ├── 📝 02_continue.md
│   │   │       ├── 📝 03_if.md
│   │   │       └── 📝 04_while.md
│   │   ├── 📦 conteineres/
│   │   ├── 🔓 desbloqueios/
│   │   │   ├── 🌻 agricultura/
│   │   │   └── 🧩 outros/
│   │   ├── 📖 informacoes_gerais/
│   │   │   ├── 📝 01_creditos.md
│   │   │   ├── 📝 02_editor_externo.md
│   │   │   └── 📝 03_primeiro_programa.md
│   │   └── 📝 99_progressao_fazenda.md
│   └── 🐍 python/
└── 📜 scripts/
    ├── 📄 README.md
    ├── 🌾 fazenda/
    │   ├── 🌱 iniciante/
    │   ├── 🌿 intermediario/
    │   └── 🌳 avancado/
    └── ⛏️ mina/
        ├── 🪨 iniciante/
        ├── 🪙 intermediario/
        └── 💎 avancado/
```

---

## 🤝 Acordo Entre Damas e Cavalheiros

Apesar de que nada do que será escrito a seguir seja determinante para a participação ou utilização do repositório, alguns acordos podem ser considerados:

1. **Evitar o uso de IA para geração de códigos (*vibe coding*):** o objetivo é conseguir progredir no jogo sem necessariamente este poderoso atalho.
   - **1.1. Uso consciente:** Caso utilize IA, considere fazê-lo de forma **socrática**, para que ela te guie sobre as ideias, e não resolva as *milestones* pra você.
   - **1.2. Transparência:** Se mesmo assim acabar rolando uma "vibezada", não tem problema — indique no arquivo do script um prefixo ou sufixo no nome com a sigla `IA` (ex.: `ia_arquivo.py` ou `arquivo_ia.py`) para termos controle do que foi gerado com agentes artificiais ou não. Também indique, se possível, com *docstrings* qual trecho do código foi feito na *vibe*.
2. **Foco inicial na solução:** Os scripts não precisam ter uma excelente performance logo de início, portanto, sugiram algoritmos que resolvam a proposta antes de pensar em tempo de execução (pra isso, devemos ter pessoas que sempre refatorarão alguns códigos).
   - **2.1. Solicitação de melhoria:** Talvez o responsável por refatorar o código não seja necessariamente a mesma pessoa que o criou. Portanto, solicitem a refatoração caso acreditem que o código tenha potencial de melhorar.
   - **2.2. Refatoração proativa:** Seja proativo e realize refatorações em scripts existentes, ajudando a melhorar as performances destes para usos futuros.
   - **2.3. Consistência nas regras:** Para refatoração, a cláusula 1 permanece válida.
3. **Documentação evolutiva:** Realize a documentação dos scripts, principalmente quando estes vão migrando de nível (`iniciante` -> `intermediario` -> `avancado`).
   - **3.1. Registro de decisões:** Considere colocar num arquivo Markdown as modificações e decisões importantes das alterações implementadas, para que um log de versões seja criado, além das mensagens de *commits*.
   - **3.2. Registro de prompts:** Caso tenha utilizado IA para geração de código, considere compartilhar o *prompt* utilizado para chegar à solução, com uma explicação breve e pessoal sobre os resultados alcançados.
4. **Banco de ideias:** Teve alguma ideia de script? Solicite uma *milestone* (ou abra uma *Issue*) com uma solicitação, descrevendo a ideia, pra ela servir de acervo para o repositório.
5. **Uso livre sem compromisso:** Gosta da fazenda e mina como um *pet* de Desktop enquanto faz qualquer outra coisa, mas não quer programar? Sem problemas, fique à vontade para utilizar qualquer script na sua fazenda e colete seus recursos sem compromisso. Considere a Cláusula 4: a solicitação de um script não necessariamente deve partir de alguém que irá programar algo.
6. **Padronização e referências:** Ao participar com uma sugestão de scripts, códigos, *requests* ou documentação e registros, considerem seguir as orientações que estarão na seção *Referências* a seguir neste documento, para manter a formatação de todas as etapas próxima de um padrão (ou ao menos tentar manter um padrão).
   - **6.1. Critério de evolução:** Para um script subir de categoria, este deve, sim, atender à maior parte das boas práticas colocadas nos documentos de referência.
---
