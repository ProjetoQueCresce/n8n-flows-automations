# Fluxos de Disparo de E-mail

Esta pasta contém todas as automações de n8n responsáveis pela cadência de prospecção por e-mail.

## Fluxos Principais (GW Disparo #Email 1 ao 6)

Todos os arquivos `GW Disparo #Email X - Oficial.json` (do 1 ao 6) operam de forma similar, seguindo a estratégia de prospecção:

- Leem os leads diretamente da planilha de prospecção.
- Utilizam uma LLM (Modelo de Linguagem) para personalizar o texto de cada e-mail.
- Realizam o disparo do e-mail para o lead.
- A principal diferença entre eles é o **texto** do e-mail e o **intervalo de tempo** (quando será enviado), seguindo a cadência definida.

## Automações de Suporte

Estes fluxos ajudam a manter a planilha e o Pipedrive atualizados:

- **Emails com erro.json:**
  - Monitora a caixa de entrada em busca de e-mails que retornaram (Bounce).
  - Quando um e-mail dá erro, esta automação marca na Planilha E no Pipedrive que aquele e-mail é inválido.
  - Isso sinaliza que o lead deve ser removido ou verificado posteriormente.

- **Atualizando a planilha e o pipedrive com pessoas que já ...:**
  - Monitora a caixa de entrada em busca de **respostas** dos leads.
  - Quando um lead responde, a automação atualiza o status desse lead na Planilha E no Pipedrive (ex: "Respondeu").
  - Isso permite que os vendedores deem sequência no atendimento e tratem a oportunidade.
