# HIDRA V11 no ecossistema Luigi

A HIDRA V11 é o motor canônico de produção de vídeos. Ela permanece instalada em `~/Desktop/HIDRA-V11` e passa a ter histórico e distribuição próprios em `https://github.com/luigi011-1/hidra-v11`.

## Conexão com os demais repositórios

A integração não usa submodule nem uma segunda cópia do motor. Isso evita divergência entre a cópia versionada e a cópia usada em produção.

- Cada repositório consumidor possui um remote Git chamado `hidra-v11`.
- Cada consumidor registra a URL, a branch e o commit aceito em `integracao/hidra-v11.json`.
- Este repositório possui remotes para os consumidores e registra seus papéis em `integracao/ecossistema.json`.
- O caminho local de produção continua sendo `~/Desktop/HIDRA-V11`.

## Repositórios conectados

- `luigi011-1/hidra`: orquestrador oficial, fila, banco, geração e edição contínua.
- `luigi011-1/luigi-repos`: central da operação, ofertas, planejamento e decisões.
- `luigi011-1/postador`: publicação e consumo dos vídeos produzidos.
- `luigi011-1/ecossistema-luigi`: manuais e backup do ecossistema.

## Restauração do motor

```bash
git clone https://github.com/luigi011-1/hidra-v11.git ~/Desktop/HIDRA-V11
cd ~/Desktop/HIDRA-V11
uv venv .venv --python 3.12
uv pip install --python .venv/bin/python -r requirements.txt
```

A geração continua sendo iniciada apenas pelo orquestrador `~/Desktop/HIDRA`.
