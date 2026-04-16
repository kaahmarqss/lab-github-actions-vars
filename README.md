# Pergunta de reflexao:
1.Por que a Secret aparece no log como *** e a variavel aparece normalmente?

Porque o GitHub mascara os valores vindo de secrets, e como vars são variaveis comuns, 
não tem a necessidade da informação ficar escondida.

2.O Job 2 consegue ler a variavel BUILD_VERSION criada no Job 1? Por que?

Não consegue, porque BUILD_VERSION foi definida no escopo do job build_app, 
e variáveis de job não são compartilhadas entre jobs.
