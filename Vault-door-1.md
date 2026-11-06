# Vault-door-1

**Categoria:** Rev

**Autor:** Mark E. Haase

### Introdução

Esse CTF, presente na plataforma [Cylab](https://learn.cylabacademy.org/library/12?page=1&search=vault-door-1&workspace=true), possui a seguinte descrição:

> This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here:
>
> VaultDoor1.java

### Resolução

Baixando o código `VaultDoor1.java` e executando-o em um compilador Java, podemos observar as seguintes linhas de código:

<img width="653" height="909" alt="image" src="https://github.com/user-attachments/assets/7f16c373-6855-4a1c-b877-d0459e08ad5d" />

Analisando o código, podemos observar, na linha 9, que a suposta senha do cofre começa com `academy{`, seguindo o formato da FLAG que estamos procurando.

Observando as linhas 22 até 55, encontramos uma função que determina a ordem em que os caracteres da senha devem ser organizados. Para descobrir a senha, basta analisar a função, anotar cada caractere na ordem em que aparece e reorganizá-los conforme essa sequência.

Após realizar esse processo, chegamos à seguinte resposta:

`academy{d35cr4mbl3_tH3_cH4r4cT3r5_d66e42}`

### Conclusão

Com a resolução desse desafio, foi possível compreender como a análise de código-fonte pode ser utilizada para encontrar informações importantes, mesmo quando os caracteres de uma senha estão organizados de maneira aparentemente confusa.

Ao analisar a função responsável pela verificação da senha, conseguimos identificar a ordem correta dos caracteres e reconstruir a sequência necessária para obter a FLAG e concluir o desafio.
