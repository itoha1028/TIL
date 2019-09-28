# 環境構築手順

1. PHPを最新化

1. Composerをインストール

    Composerはパッケージ管理
    1. Composer.pharを入手

        スクリプトを実行すると、composer.pharファイルが出来ているはず。
        ```Bash
        php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
        php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
        php composer-setup.php
        php -r "unlink('composer-setup.php');"
        ```

    1. パスを通す

    Composer.pharを `/usr/local/bin` へ配置

1. Laravelをインストール

    1. インストーラーを入手

        https://readouble.com/laravel/4.2/ja/quick.html
        
        ```Bash
        composer global require "laravel/installer=~1.1"
        ```
    1. パスを通す

        ```Bash
        export PATH=$PATH:~/.composer/vendor/bin
        ```