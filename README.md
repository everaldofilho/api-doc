# Documentando API
Criado este projeto somente para colocar em pratica as ferramentas citadas abaixo

## Ferramentas
- Api Blueprint (Documentação makerdown)
- Aglio (Redenriza em HTML ou outros formatos)
- Drakov (Sobe um servidor fake com a estrutura documentada)
- Dredd (Testa API com base na documentação)

## Requisitos
- Tenha instaldo o `NPM` 

## Instalação

Aglio

    npm install -g aglio

Drakov

    npm install -g drakov

Dredd

    npm install -g dredd

## Usando as ferramentas

Aglio para geração da documentação em HTML ou Subindo um no localhost

````aglio -i api.apib  -o api-doc.html````

Ou

````aglio -i api.apib --theme-full-width --no-theme-condense -s````

Subindo o servidor fake usando `Drakov`

````drakov -f api.apib -p 4000````


Testando a API `Dredd`

````dredd api.apib http://localhost:4000````

ou 

````dredd````