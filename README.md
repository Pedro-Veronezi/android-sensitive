Android Sensitive
===================================

Este repositório tem como objetivo desacoplar informações e artefatos sensiveis a aplicação Android.

Passos
--------------

1. Incluir o sensitive.gradle no build.gradle do app com o seguinte bloco:
apply plugin: 'com.github.triplet.play'

if(file("sensitive/sensitive.gradle").exists()) {
    apply from: "sensitive/sensitive.gradle";
}

2. Gerar chave de Release e adicionar na raiz

3. Gerar chave para o acesso ao Google Play e colocar na raiz deste projeto.

4. Configurar o sensitive.gradle com as configuração do Release

5. Fazer o primeiro deploy no Google play de forma manual

Links
-------
https://github.com/Triple-T/gradle-play-publisher



TODO
------
- Verificar se o apply plugin: 'com.github.triplet.play' pode ficar dentro do sensitive.gradle
