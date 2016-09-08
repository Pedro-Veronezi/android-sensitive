Android Sensitive
===================================

Este repositório tem como objetivo desacoplar informações e artefatos sensiveis a aplicação Android.

Configurar o sensitive
--------------
1.Clonar como um submodulo dentro do diretório raiz do modulo do app :
```sh
git submodule add https://github.com/Pedro-Veronezi/android-sensitive.git sensitive
```
2.Inclusão do sensitive.gradle no build.gradle do app:

Adicionar depois do bloco Android:

```sh
if(file("sensitive/sensitive.gradle").exists()) {
    apply from: "sensitive/sensitive.gradle";
}
```
3.Gerar chave de Release e adicionar na raiz do modulo app.

Passos para o deploy no Google Play
--------------

1. Gerar chave para o acesso ao Google Play e colocar na raiz do modulo app.
2. Configurar o sensitive.gradle com as configuraçãoo do Release.
3. Fazer o primeiro deploy no Google play de forma manual.

Referência
-------
https://github.com/Triple-T/gradle-play-publisher



TODO
------
- Verificar se o apply plugin: 'com.github.triplet.play' pode ficar dentro do sensitive.gradle
- Refatorar para que as informações fiquem em variaveis.
