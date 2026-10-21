# sentinela-plugins

Atualizações dos plugins WordPress da agência (**Sentinela Agent** e **Blindagem**).

O WordPress de cada site lê `versoes.json` e baixa o zip de `zips/` quando o administrador clica em
atualizar no wp-admin. Nada é instalado sozinho.

Cada zip é assinado (Ed25519) sobre `slug\nversão\nsha256`. O plugin traz a chave pública e recusa
zip sem assinatura válida — mexer neste repositório não basta para entregar código aos sites.
A chave privada nunca entra aqui.

Publicar: no repositório do Sentinela, `node scripts/assinatura.mjs publicar <esta pasta>`, depois
commit e push.
