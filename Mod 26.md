# Mod 26

**Categoria:** Crypto

**Autor:** Pandu

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/144?page=1&bookmarked=true&workspace=true), possui a seguinte descrição, acompanhada de um arquivo `values.txt`:

> Cryptography can be easy, do you know what ROT13 is?

### Resolução

Ao abrir o arquivo `values.txt`, nos deparamos com o seguinte texto:

`npnqrzl{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_5p5s5o36}`

<img width="674" height="173" alt="image" src="https://github.com/user-attachments/assets/2de60c15-d796-4ce2-bb5a-bd4bf9c3d1aa" />

O texto se parece muito com uma FLAG, porém está criptografado. Como o próprio enunciado nos pergunta `"Você sabe o que é ROT13?"`, podemos entender que a resposta está relacionada a esse método de criptografia.

O ROT13 é uma técnica de substituição de caracteres que consiste em deslocar cada letra do alfabeto em 13 posições. Como o alfabeto possui 26 letras, aplicar esse processo duas vezes retorna ao texto original.

Para realizar a decodificação, acessei o site [Dcode](https://www.dcode.fr/en), especificamente a ferramenta [ROT13](https://www.dcode.fr/rot-13-cipher). Inserindo o código encontrado no arquivo `values.txt` no campo de decodificação (Decoder), conseguimos obter a FLAG:

`academy{next_time_I'll_try_2_rounds_of_rot13_5c5f5b36}`

<img width="786" height="243" alt="image" src="https://github.com/user-attachments/assets/30ce394a-25c4-469c-9f7a-f84486b55ca1" />

### Conclusão

Com a resolução desse desafio, foi possível compreender como funciona a técnica de substituição ROT13 e como ela pode ser utilizada para codificar e decodificar mensagens.

O desafio demonstrou que nem sempre uma sequência aparentemente sem sentido representa uma criptografia complexa. Nesse caso, utilizando uma técnica simples de substituição e a ferramenta Dcode, conseguimos decodificar o texto e obter a FLAG necessária para concluir o desafio.
