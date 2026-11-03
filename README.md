# Private Streaming Platform

Plataforma web experimental de **compartilhamento de tela para pequenos grupos**, desenvolvida com **ASP.NET Core (.NET 8)** e **Angular**, utilizando **WebRTC** para comunicação em tempo real e **WebSocket** para sinalização.

> **Status:** projeto pessoal em desenvolvimento. A configuração descrita abaixo é voltada à execução local; não representa uma implantação pública pronta para produção.

## Visão geral

O projeto explora a construção de uma aplicação de streaming privado, separando as responsabilidades entre um backend em .NET e uma interface web em Angular.

## Tecnologias

| Camada | Tecnologia | Papel |
| --- | --- | --- |
| Backend | C# / ASP.NET Core (.NET 8) | Servidor e lógica da aplicação |
| Frontend | Angular | Interface web |
| Comunicação em tempo real | WebRTC | Compartilhamento de mídia/tela |
| Sinalização | WebSocket | Troca de mensagens para estabelecimento das conexões |

## Estrutura do projeto

```text
backend/    # Aplicação ASP.NET Core
frontend/   # Aplicação Angular
```

## Como executar localmente

### Pré-requisitos

- SDK do .NET 8
- Node.js e npm
- Navegador compatível com WebRTC e compartilhamento de tela

### 1. Iniciar o backend

No PowerShell, a partir da raiz do repositório:

```powershell
cd backend
$env:ROOM_PASSWORD="sua-senha-local"
dotnet run
```

Backend: `http://localhost:8080`.

### 2. Iniciar o frontend

Abra outro terminal na raiz do repositório:

```powershell
cd frontend
npm install
npm start
```

Frontend: `http://localhost:4200`.

Acesse o frontend pelo navegador com o backend em execução.

## Configuração e segurança

A senha da sala é definida pela variável de ambiente `ROOM_PASSWORD`. **Não publique senhas reais, tokens ou outros segredos no repositório.**

Este é um protótipo para estudo e uso local. Antes de disponibilizá-lo na internet, é necessário revisar autenticação, transporte seguro (HTTPS/WSS), configuração de rede e as condições de conectividade do WebRTC.

## Próximos passos

- Documentar com capturas de tela e uma demonstração curta.
- Validar o funcionamento em diferentes redes e navegadores.
- Revisar segurança e configuração para acesso externo.

## Autor

Desenvolvido por [Rodrigo Abade](https://github.com/RodrigoAbade).
