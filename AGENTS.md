# HIDRA V11: motor canônico da operação

## Papel no ecossistema
- Este repositório contém o motor canônico e completo da HIDRA V11.
- Caminho oficial em produção: `~/Desktop/HIDRA-V11`.
- Repositório privado: `https://github.com/luigi011-1/hidra-v11`.
- O orquestrador oficial é `https://github.com/luigi011-1/hidra`, instalado em `~/Desktop/HIDRA`.
- O mapa dos consumidores fica em `integracao/ecossistema.json`.

## Regras de produção
- Produção somente por `~/Desktop/HIDRA/hidra gerar <lotes...>` ou `~/Desktop/HIDRA/hidra madrugada <lotes...>`.
- Não executar `studio_web.py` ou `edicao/vigia.py` avulsos na operação oficial.
- Não reativar motores históricos, trocar o modelo de vídeo, o perfil Chrome ou a porta CDP sem autorização explícita do Luigi.
- Preservar as proteções do Flow e o fluxo de uma única conta usado pelo orquestrador oficial.
- Depois de alterações no motor, validar por `~/Desktop/HIDRA/hidra testar`.

## Versionamento
- Branch principal: `main`.
- Não versionar `.venv`, `.env`, contas reais, cookies, proxies, pacotes com base64, mídias ou caches.
- Todo código Python, JavaScript, scripts de instalação, extensão, fontes e documentação essencial deve permanecer versionado.
- Ao atualizar a `main` deste repositório, atualizar o commit registrado em `integracao/hidra-v11.json` nos repositórios consumidores.
