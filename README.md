Android Sensitive
===================================

Este repositório tem como objetivo desacoplar informações e artefatos sensiveis a aplicação Android.

Passos
--------------
1. Criar uma pasta sensitive no modulo do app

2. Incluir o sensitive.gradle no build.gradle do app com o seguinte bloco:
apply plugin: 'com.github.triplet.play'

if(file("sensitive/sensitive.gradle").exists()) {
    apply from: "sensitive/sensitive.gradle";
}

3. Gerar chave de Release e adicionar na raiz

4. Gerar chave para o acesso ao Google Play e colocar na raiz.

5. Configurar o sensitive.gradle com as configuração do Release

6. Adicionar a pasta sensitive no .gitignore do app:
    sensitive/

7. Fazer o primeiro deploy no Google play de forma manual

Referência
-------
https://github.com/Triple-T/gradle-play-publisher



TODO
------
- Verificar se o apply plugin: 'com.github.triplet.play' pode ficar dentro do sensitive.gradle
- Refatorar para que as informações fiquem em variaveis.
