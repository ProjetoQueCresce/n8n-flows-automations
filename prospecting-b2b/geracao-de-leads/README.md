# Automações de Geração de Leads

Esta pasta contém os fluxos (flows) de n8n responsáveis pelo processo de geração e qualificação de leads.

## GD Captação Linkedin - Oficial

Esta automação é responsável por encontrar novos leads. O processo funciona da seguinte forma:

- Faz um "scrappe" (varredura) no LinkedIn buscando vagas de emprego que correspondam ao cargo alvo (ex: Consultoria).
- Identifica a empresa que publicou a vaga e encontra o domínio (site) dessa empresa.
- Utiliza a plataforma Snov.io para buscar todos os e-mails associados a esse domínio.
- Filtra a lista para pegar apenas os e-mails que pertencem a "tomadores de decisão".
- Salva as informações completas desses leads (Nome, Empresa, Cargo e E-mail) dentro de uma planilha.

## GD Atualização Pipedrive - Oficial

Esta automação é a segunda etapa do processo. Ela pega os leads da planilha e os insere no CRM:

- Lê a planilha que foi preenchida pela automação de captação.
- "Normatiza" todas as informações (corrige formatos, limpa dados, etc.).
- Cadastra cada um desses leads verificados dentro do Pipedrive.

