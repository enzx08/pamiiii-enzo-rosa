# Instalação do Laravel!

Antes de criar seu primeiro aplicativo Laravel, certifique-se de que sua máquina local tenha PHP, Composer e o instalador do Laravel instalados. Além disso, você deve instalar o Node e o NPM ou o Bundle para poder compilar os recursos de front-end do seu aplicativo.

# Run as administrator...

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))

Se você já tem o PHP e o Composer instalados, você pode instalar o instalador do Laravel via Composer:

    composer global require laravel/installer

# Criando o aplicativo
 
Após instalar o PHP, o Composer e o instalador do Laravel, você estará pronto para criar uma nova aplicação Laravel.

    laravel new example-app

Depois que o aplicativo for criado, você pode iniciar o servidor de desenvolvimento local do Laravel, o queue worker e o servidor de desenvolvimento Vite usando o `dev`script do Composer:

    cd example-app
    npm install && npm run build
    composer run dev
    

 - Criar uma copia do arquivo env.example e colar, renomear para .env
 
 
 - Criar uma chave encriptada com o comando:

>  php artisan key:generete

 - Rodar as migrations para criar o banco de dados com o comando php artisan migrate.


# Criando o aplicativo

Comando para iniciar o seu Laravel:
    composer run dev
 




