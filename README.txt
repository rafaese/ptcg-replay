PTCG Replay v2.1 — Instruções de uso e deploy (tema claro)
=========================================================

Arquivos incluídos:
- index.html : aplicação principal (versão light, parser v2.1)
- assets/placeholder.png : placeholder usado quando imagem não é encontrada
- example_log.txt : exemplo de log para testar a aplicação
- README.txt : este arquivo

Como usar localmente:
1. Extraia o ZIP e abra `index.html` no seu navegador.
2. Cole o registro de batalha no campo e clique em "Gerar".
   - Observação: quando abrir via file:// algumas requisições à Pokémon TCG API podem falhar por CORS.
     O código usa um fallback (images.weserv.nl) para imagens por nome.

Deploy no GitHub Pages:
1. Crie um repositório no GitHub (por exemplo: ptcg-replay).
2. Faça upload do conteúdo do ZIP para o repositório na branch `main`.
3. No GitHub, vá em Settings -> Pages, escolha branch `main` e pasta `/(root)` e salve.
4. Aguarde alguns minutos; seu site ficará disponível em:
   https://SEU_USUARIO.github.io/NOME_DO_REPO/

Notas:
- O parser é mais robusto, mas logs com frases muito diferentes ainda podem precisar de ajustes.
- Se quiser, eu adapto o parser para reconhecer ainda mais padrões (status detalhados, energias, habilidades específicas).
