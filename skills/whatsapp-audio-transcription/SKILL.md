---
name: "whatsapp-audio-transcription"
description: "Audio WhatsApp: transcricao antes de resposta e fallback seguro."
---

# WhatsApp Audio Transcription

Sempre converter audio em texto antes de responder. Nao pedir para a pessoa digitar o conteudo se o audio puder ser processado.

## Quando Usar

Use quando uma mensagem chegar com:
- audio;
- nota de voz;
- gravacao;
- video ou midia que provavelmente contem fala;
- contexto em que o usuario espera resposta baseada no conteudo falado.

## Procedimento

1. Identificar o anexo de audio e preservar o contexto da conversa.
2. Priorizar o canal integrado do OpenClaw/WhatsApp e as ferramentas de midia disponiveis; nao abrir WhatsApp Web ou navegador para atendimento normal se o canal integrado estiver disponivel.
3. Baixar ou acessar a midia usando as ferramentas disponiveis do OpenClaw.
4. Se necessario, converter para formato transcritivel como mp3, wav, m4a ou ogg sem alterar o original.
5. Transcrever com a melhor ferramenta disponivel.
6. Ler a transcricao antes de responder.
7. Se a transcricao estiver incerta, dizer isso brevemente ao dono/admin e pedir esclarecimento apenas do trecho duvidoso.
8. Se for conversa comercial do produto, responder conforme o playbook comercial ativo e mensagens aprovadas.
9. Se falhar por midia expirada, ausente, grande, criptografada ou inacessivel, fazer uma tentativa segura de recuperacao; se continuar bloqueado, explicar ao dono/admin sem expor stack trace, nomes de ferramentas ou detalhes internos a leads externos.

## Regras

- Nao ignorar audio.
- Nao responder com confirmacao generica antes de entender o conteudo.
- Nao pedir versao em texto quando for possivel transcrever.
- Nao armazenar conteudo sensivel do audio alem da memoria operacional normal, salvo pedido explicito.
- Tratar transcricao como processamento interno; responder naturalmente, como quem escutou e entendeu.
- Nao expor erros internos de ferramenta a leads externos.
- Se o gateway estiver offline/desconectado e o audio existir apenas no telefone do usuario, pedir ao dono/admin o contato ou o conteudo necessario antes de agir.

## Saida Esperada

Quando util para o dono/admin, entregar:
- transcricao resumida;
- intencao principal;
- pontos de decisao;
- resposta recomendada.

Em conversa externa, enviar apenas a resposta final adequada ao contexto.
