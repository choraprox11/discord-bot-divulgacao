@echo off
echo ================================
echo  DISCORD BOT - DIVULGACAO
echo ================================
echo.
echo Iniciando o bot...
echo.

REM Verificar se o Node.js está instalado
node --version >nul 2>&1
if %errorlevel% neq 0 (
    echo ERRO: Node.js nao encontrado!
    echo Por favor, instale o Node.js em: https://nodejs.org
    pause
    exit /b 1
)

REM Verificar se as dependências estão instaladas
if not exist "node_modules" (
    echo Instalando dependencias...
    npm install
    echo.
)

REM Iniciar o bot
echo Bot iniciando...
echo Para parar o bot, pressione Ctrl+C
echo.
node bot.js

pause
