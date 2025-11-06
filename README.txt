PTCG Replay — Instruções de uso e deploy
=======================================

Arquivos incluídos:
- index.html : aplicação principal (abra localmente ou hospede no GitHub Pages)
- example_log.txt : exemplo de log para testar a aplicação
- README.txt : este arquivo

Como usar localmente:
1. Extraia o ZIP e abra `index.html` no seu navegador.
2. Cole o registro de batalha no campo e clique em "Gerar".
   - Observação: quando abrir via file:// algumas requisições à Pokémon TCG API podem falhar por CORS.
     O código usa um fallback (images.weserv.nl) para imagens por nome.

Deploy no GitHub Pages:
1. Crie um repositório no GitHub (por exemplo: ptcg-replay).
2. Faça upload do conteúdo do ZIP para o repositório na branch `main` (ou `gh-pages`).
3. No GitHub, vá em Settings -> Pages, escolha branch `main` e a pasta `/ (root)` e salve.
4. Aguarde alguns minutos; seu site ficará disponível em:
   https://SEU_USUARIO.github.io/NOME_DO_REPO/

Recomendações e notas:
- Para melhorar a detecção de imagens, permita que o navegador faça chamadas à `api.pokemontcg.io` (normalmente funciona em https).
- O parser é heurístico: cobre ações comuns, mas pode precisar de ajustes para logs com formatos muito específicos.
- Se quiser, eu posso adaptar o parser para extrair ainda mais detalhes (condições de status, contadores exatos de energias, badges).
