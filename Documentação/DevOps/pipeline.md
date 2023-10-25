## Explicação das branches

**Main:** usada como branch final, onde ficará o código das versões oficiais de cada sprint, após ser mesclada com as branches de release e hotfix.

**Devolp:** branch usada para produção, onde são mesclado os códigos das branch de feature, hotfix e bugfix. Eventualmente enviada para branch de release para teste e depois mesclada na main, para entrega do código final.

**Feature -> Nome da feature:** nomeada baseada na feature, a branch é criada a partir da develop para codar e realizar a nova feature, quando terminada é testada e então mesclada com a develop.

**Hotfix -> Nome do hotfix:** nomeada baseada no hotfix, a branch é criada a partir da main para codar e resolver o hotfix, quando terminada é testada e então mesclada com a main e a develop.

**Bugfix -> Nome do bugfix:** nomeada baseada no bugfix, a branch é criada a partir da develop para codar e resolver o bugfix, quando terminada é testada e então mesclada com a develop.

**Release:** branch usada para teste de integração, onde são enviados os códigos das branch de develop para teste, e em caso de sucesso, mesclada com a main, em caso de falha o erro deve ser corrigido pela bugfix.

![grafico das branches](https://github.com/Vitality-4DSM/Documentacao/assets/101061910/03891e9d-6d82-456c-9a53-99c2299d41ee)
