# Cookie Monster

**Categoria:** Web exploitation.

### Introdução

Esse CTF é um desafio presente na Escolinha CTF. Sua resolução consiste em manipular um valor presente nos cookies do site fornecido.

* [Página do desafio](https://monster.discloud.app/)

### Resolução

Logo de início, nos deparamos com uma tela branca com um título Cookie Monster e uma descrição: `NOM NOM... você não é admin!`.

<img width="1919" height="944" alt="image" src="https://github.com/user-attachments/assets/2179b283-709b-462a-8b89-6c750c96461e" />

Com base no texto apresentado na imagem acima, conseguimos identificar duas dicas: a primeira é que você não é admin da página, e a segunda é que isso está, de alguma forma, relacionado com os cookies do site.

Apertando a tecla F12 no navegador Google Chrome, acessamos as DevTools do site.

<img width="1919" height="945" alt="image" src="https://github.com/user-attachments/assets/ba1e53d0-16ce-422e-a069-0ab8c16f690f" />

Indo até a aba `Application`, na categoria `Storage`, conseguimos encontrar os cookies do site. Entre eles, há uma linha com o nome `admin`, que possui o valor `nao`.

<img width="1919" height="942" alt="image" src="https://github.com/user-attachments/assets/43eb6fb1-2b9c-49d0-a433-01a2e4541784" />

Alterando esse valor para `sim` e atualizando a página, a flag que estávamos procurando é revelada: `"NOM NOM NOM! DELÍCIA! Aqui está sua flag: FLAG{C00K1E_M0NST3R_MUNCH}"`.

<img width="1919" height="941" alt="image" src="https://github.com/user-attachments/assets/a6de57de-2a71-47d1-b703-1cc2dd32a7b6" />

### Conclusão

Esse desafio aborda conceitos bastante simples de web exploitation que, embora sejam simples, são ferramentas de extrema importância no ramo da cybersegurança. Ele nos ensina como podemos acessar e manipular os cookies de um site por meio das DevTools do navegador.
