# Painel de SITs | Oficina de Trens de Passageiros (Marka x Vale, TFPM)

Site estático (GitHub Pages) que mostra o status das Solicitações de Informação Técnica, monta a mensagem de WhatsApp com as SITs em aberto e permite atualizar os dados online.

- Dados: `data/sits.json` (fonte única, todos os visitantes leem este arquivo)
- Página: `index.html` (sem build; SheetJS via cdnjs)

## Como atualizar (quem envia o relatório)
1. Exportar o "Relatório de resumo" (.xlsx) da plataforma.
2. Abrir o painel, aba **Atualizar**, soltar o arquivo e conferir o resumo de mudanças.
3. Informar o nome e a chave de acesso e clicar em **Publicar para todos**.

O arquivo atualiza as SITs que ele traz. SITs ausentes no arquivo (por exemplo, filtradas por data de vencimento) permanecem como estavam.

## Chave de acesso (Gerson gera uma vez)
GitHub > Settings > Developer settings > Fine-grained tokens. Repositório: só este. Permissão: Contents = Read and write. Validade: 90 dias. A chave fica salva apenas no navegador de quem atualiza.

Sem chave, use **Baixar sits.json** e suba o arquivo em `data/` pelo site do GitHub.
