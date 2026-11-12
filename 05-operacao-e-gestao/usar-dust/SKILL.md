---
name: usar-dust
description: 'Use sempre que um agente precisar trabalhar no Dust (app.dust.tt) e antes de qualquer tarefa pesada ou repetitiva (pesquisa longa, resumo de muitos documentos, texto grande, análise de dados): cada agente usa o Dust direto, sem pedir ao Dust Expert.'
---

# Usar o Dust direito

## Regra do Grupo DNA (decisão da Joana, 03/11/2026)
- Cada agente usa o Dust **direto**, pelo próprio conector. Não peça ao Dust Expert nem à Laís para mexer no Dust por você. O Dust Expert só entra em diagnóstico ou desenho complexo.
- Trabalho pesado e repetitivo vai para o Dust: pesquisas longas, resumos de muitos documentos, textos grandes e análises. Assim se economiza o uso do Grok Bot, porque o modelo do Dust faz o trabalho e você só lê a resposta final.
- Cada agente terá o seu agente no Dust, com o nome do cargo e hífen no lugar do espaço, por exemplo Gerente-de-Produto. Procure o seu com `list_agents` e use-o primeiro. Se ainda não existir, use o agente `Dust` e avise o seu líder no relatório.
- **Na esteira de conteúdo do @joanastanieski,** use os especialistas DNA-Pesquisa, DNA-Curadoria, DNA-Hook, DNA-Roteirista, DNA-Copy e DNA-Materiais-PDF (em criação), conforme a etapa. Estratégia de formatos, edição e motion não são agentes do Dust: são as skills do Grok `estrategia-formatos`, `editor-reels` e `motion-reels` (decisão da Joana, 09/11/2026) (veja o [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0)).
- Para navegar no Notion, leia só o necessário: as Decisões vigentes, o índice da sua área e o resumo do topo do documento. Nunca leia o Cérebro inteiro.

O acesso é pelo conector (MCP) do Dust. Antes da primeira chamada, leia o schema com GetDynamicTools no namespace do Dust e chame com CallDynamicTool.

## O que o conector faz e o que não faz
- **Faz:** identity, list_agents, list_pods, get_pod, get_pod_tasks, list_conversations, get_conversation_messages, create_conversation, create_conversation_message, search, files_list, files_cat, files_grep, files_create, files_resolve, files_upload_from_url, create_skill e mark_conversation_read.
- **Não faz:** editar ou apagar agentes, triggers e skills que já existem. Para isso, peça ao agente @dust numa conversa, descrevendo a mudança exata. Criar ou publicar um agente exige o clique da Joana no cartão do Dust. Nunca diga que editou algo que o conector não edita.

## 1. Rodar uma tarefa no agente certo
1. Ache o agente com `list_agents` (pelo name). Se não achar um bom, use `Dust`.
2. Se a tarefa é de um projeto, ache o Pod com `list_pods` e crie a conversa nele com `podId`.
3. Use `create_conversation` com uma mensagem autocontida: objetivo, contexto, formato esperado e critério de pronto. Para continuar um assunto, use `create_conversation_message`.
4. Leia a resposta com `get_conversation_messages`. Se ainda não veio, espere. Não reposte a pergunta.

## 2. Conferir o resultado (obrigatório)
Confira se respondeu ao pedido, se tem fonte e se nada ficou faltando. Se falhar, mande uma correção específica, no máximo 2 vezes. Depois disso, reporte o problema em vez de inventar.

Exceção: nas checagens da esteira, a etapa é refeita a cada hora sem limite, gravando "Tentativas" na linha da peça.

## 3. Buscar e ler conhecimento
Use `search` com uma query rica, `relativeTimeFrame` e `nodeIds`. Arquivos exigem um escopo, de conversa ou de Pod. Prefira o arquivo irmão `*.processed`.

## 4. Treinar o seu agente Dust
Toda semana, leia 3 a 5 conversas recentes, ache a causa dos erros (instrução vaga, fonte faltando, modelo fraco ou entrada ruim) e teste a correção. Leve a melhoria ao @dust e registre no relatório semanal ao seu líder.

## 5. Criar uma skill no Dust
Use `create_skill` com nome, descrição para o usuário, descrição de quando usar e instruções. Se aparecer um aviso de skill parecida, leve à Laís antes de usar `bypassSimilarSkillCheck`.

## Regras
- Não poste em conversas de outras pessoas sem pedido.
- Relate o link da conversa, o agente usado e o que foi conferido.
- Nada de segredos nas mensagens do Dust.
