# Instruções sobre os scripts

Boas-vindas ao diretório de scripts. Neste diretório serão armazenados os scripts do jogo, inicialmente, separados em 2 subdiretórios: **fazenda** e **mina**.
**fazenda** e **mina** tem mais outros 3 diretórios, que separam os scripts por "níveis":
* **Iniciante** -> Para pratica pontual de algumas ideias, são scripts majoritariamente monolíticos que não contam com as boas práticas que queremos alcançar.
Podem ser considerados os scripts que podem sofrer refatoração. Qualquer script que não seja modular ou que a ideia seja muito "crua" podem ser alocados aqui.
* **Intermediário** -> São scripts que já contém algumas estruturas mais fundamentadas, como funções, variaveis bem definidas e afins, porém, ainda não são scripts suficientemente
adequados para serem considerados modulares (estarão a um passo disso). Apesar de não serem modulares, todas ou a maior parte das boas práticas já devem ser aplicadas.
Adicionalmente, são scripts que podem não serem considerados avançados pela falta da habilidade `import` que deve ser desbloqueada no jogo.
* **avancado** -> O objetivo de maestria. Todos os scripts aqui podem e devem ser utilizados em uma biblioteca personalisada e, a partir dela, seja possível reutilizar códigos já
feitos anteriormente para a criação de uma função `main()` mais robusta. Para estes programas, espera-se que a habilidade `import` esteja desbloqueada.
