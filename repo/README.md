# Copa Jogo Pensado

App para organizar as copinhas de futebol das festas de aniversário (Jogo Pensado): monta os confrontos automaticamente, cuida da classificação, do mata-mata (semifinal/disputa de 3º/final) e da lista de artilheiros. No final, exporta um resumo em PDF ou PNG pra mandar pro pai da criança.

É um arquivo único (`index.html`) — não precisa de instalação, servidor, Node, nada. Os dados de cada copa ficam salvos no navegador (localStorage), então continuam ali mesmo se você fechar a aba ou reiniciar o celular/computador (mas só naquele navegador específico).

## Como abrir no seu computador (localhost)

Não dá pra simplesmente abrir o `index.html` clicando duas vezes em alguns casos (o navegador bloqueia alguns recursos em arquivos abertos direto do disco). O mais seguro é subir um servidor local bem simples:

**Se você tem Python instalado** (Mac e Linux já vêm com ele):
```bash
cd copa-jogo-pensado
python3 -m http.server 8000
```
Depois abre no navegador: http://localhost:8000

**Se você tem Node instalado:**
```bash
cd copa-jogo-pensado
npx serve .
```
Ele vai te mostrar o endereço (algo como http://localhost:3000).

## Como subir pro GitHub

```bash
cd copa-jogo-pensado
git init
git add .
git commit -m "Copa Jogo Pensado"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/copa-jogo-pensado.git
git push -u origin main
```
(Troque `SEU_USUARIO` pelo seu usuário do GitHub. Você precisa ter criado o repositório vazio antes, direto no site do GitHub.)

## Como deixar acessível de qualquer lugar (opcional)

Se quiser abrir pelo celular sem precisar rodar nada no computador, dá pra publicar de graça no **GitHub Pages**:
1. No repositório, vá em Settings → Pages
2. Em "Source", escolha a branch `main` e a pasta `/ (root)`
3. Salva — em alguns minutos o GitHub te dá um link tipo `https://SEU_USUARIO.github.io/copa-jogo-pensado/`
4. Abre esse link no celular e adiciona à tela de início (fica com carinha de app)

## Como instalar como app (tela inicial do celular)

Isso só funciona quando o site está sendo servido por http/https (localhost ou GitHub Pages) — não funciona abrindo o arquivo direto (`file://`).

**Android (Chrome):**
1. Abre o link do app
2. Toca no menu (⋮) → "Adicionar à tela inicial" ou "Instalar app"

**iPhone (Safari):**
1. Abre o link do app
2. Toca no ícone de compartilhar (□ com seta pra cima)
3. Escolhe "Adicionar à Tela de Início"

Depois disso, o ícone da lâmpada aparece na tela inicial igual um app de verdade, abre em tela cheia (sem barra de navegador) e mantém os dados salvos normalmente.

## Sobre os dados salvos


Os dados (times, placares, artilheiros) ficam guardados no navegador de cada aparelho separadamente. Ou seja:
- Se você abrir sempre pelo **mesmo navegador, no mesmo celular/computador**, os dados continuam de onde parou.
- Se abrir num navegador diferente ou outro aparelho, começa uma copa nova (ele não sincroniza entre dispositivos).
- O botão "Nova Copa" dentro do app limpa os dados salvos e começa do zero.
