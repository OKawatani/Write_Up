# Drag Path

**Categoria:** OSINT

**Autor:** M3SSAG3_MAN

### Introdução

Esse CTF, presente na [Escola CTF](https://web-e.discloud.app), possui a seguinte descrição:

> "Um rastro gravado na superfície, como evidência que eu deixei lá de propósito.
>
> Eu cravei os meus calcanhares no cascalho, como evidência para você desvendar.
>
> Você consegue me encontrar?"

Junto com essa descrição, há uma imagem com o nome **Trench**.

<img width="1068" height="648" alt="image" src="https://github.com/user-attachments/assets/d4a6c2c0-6565-485e-a543-91c126565410" />

### Resolução

Pesquisando os termos [Trench](https://www.google.com/search?sca_esv=28d5dd4666abb16a&sxsrf=APpeQntochWxS89QU2fqj3gyta159BbI3A:1786720449862&q=Trench&source=lnms&fbs=ABfTbFXXq5_lq1-qc-RNbCT-iVCvZUY4OllCx8eHi2DBbGa2PoUPiBop7GRck9_ggqJeBKll0uNH5-o_DmiqZYfdMFHSMQ7m9lGiXMmoLpyBCvs0fha8MLwauUu8kFshyTso0QBo6MY16pqU4X1dTMTrNg9ApjhzIQeQBlgg6wvH3FcHuQIBlKneyhHb6sxS5ocPBAFfn_cSJbP7xHZe8X-kF1YhjEA2TluvUe36mxBQ4kuJe4Zr-Eg&sa=X&ved=2ahUKEwii--ettKCWAxX-n5UCHYhXE1oQ0pQJegQICxAB&biw=1745&bih=859&dpr=1.1) e [Drag Path](https://www.google.com/search?q=drag+path&oq=drag+path&gs_lcrp=EgZjaHJvbWUqDwgAEAAYQxjjAhiABBiKBTIPCAAQABhDGOMCGIAEGIoFMgwIARAuGEMYgAQYigUyBwgCEAAYgAQyBwgDEAAYgAQyBwgEEAAYgAQyBggFEEUYPDIGCAYQRRg8MgYIBxBFGDzSAQgyNTUzajBqN6gCALACAA&sourceid=chrome&source=chrome.ob&ie=UTF-8), ambos nos levam a uma mesma pista: a banda **Twenty One Pilots**.

*Drag Path* sendo a última música lançada por eles no momento da escrita deste write-up, uma possível solução seria reconhecer a citação presente na letra de *Drag Path* e relacioná-la à música [Jumpsuit](https://www.youtube.com/watch?v=UOUBW8bkjQ4&list=RDUOUBW8bkjQ4&start_radio=1), uma música do álbum *Trench* que mostra os acontecimentos citados em *Drag Path*.

<img width="1919" height="813" alt="image" src="https://github.com/user-attachments/assets/f9773fd6-0aad-4a17-90cc-6d6e9b8892a0" />

Com essas informações, pesquisamos o local de gravação do clipe de *Jumpsuit* e conseguimos encontrar parte da resposta no site [Capital UK](https://www.capitalfm.com/artists/jumpsuit-video-location-iceland/): **Fjaðrárgljúfur**.

<img width="684" height="137" alt="image" src="https://github.com/user-attachments/assets/144bb3c1-7756-4495-ab5f-5e2c38dbbf50" />

Retirando os acentos do nome, chegamos à resposta final:

**Flag{Fjaorargljufur}**

### Conclusão

Esse desafio tem como principal objetivo nos incentivar a buscar respostas nos pequenos detalhes, nos nomes e nas citações. Com um pouco de pesquisa, é possível chegar à resposta.

Outra alternativa, mais simples, para chegar à resposta seria simplesmente jogar a imagem no Google, junto com o nome **Twenty One Pilots**. Dessa forma, também seria possível encontrar o nome da localização.
