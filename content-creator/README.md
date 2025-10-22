# Fluxo de Automação "Content Creator"

Esta pasta contém um fluxo completo de automações n8n para transformar um Reels do Instagram em um novo conteúdo e publicá-lo em outras plataformas.

O processo funciona em 4 etapas:

- **1. Scrap Reels do Instagram copy.json**
  - Esta automação inicia o fluxo.
  - Ela faz o "scrap" de um Reels do Instagram e extrai o roteiro (texto).
  - Utiliza uma LLM (Modelo de Linguagem) para fazer pequenas modificações e otimizações no roteiro.

- **2. Geração de vídeo com heygen.json**
  - Esta automação pega o roteiro modificado da etapa anterior.
  - Utiliza a plataforma HeyGen para gerar um novo vídeo com um Avatar (apresentador) real.

- **3. Gerando a Thumb e a Descrição copy.json**
  - Como o nome diz, esta automação cria os complementos para o vídeo.
  - Ela gera uma Thumbnail (capa) e um texto de Descrição otimizado.

- **4. Agente de publicação copy.json**
  - Esta é a última etapa do fluxo.
  - O agente pega o vídeo, a thumbnail e a descrição e publica o conteúdo final automaticamente no YouTube e no Twitter.
