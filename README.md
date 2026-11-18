<div align="center">

<img src="assets/04-final.png" alt="Cena final do motion: Pense antes de clicar" width="100%">

# 🛡️ Motion · Cibersegurança

**Uma animação interativa, narrada e com sons, que mostra como os maiores ataques da história aconteceram e como uma configuração certa teria evitado cada um.**

![HTML](https://img.shields.io/badge/HTML5-single%20file-00ff9c?style=for-the-badge&logo=html5&logoColor=white&labelColor=04070d)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-27d3ff?style=for-the-badge&logo=javascript&logoColor=white&labelColor=04070d)
![WebAudio](https://img.shields.io/badge/Web%20Audio-sons%20sintetizados-ff3b5c?style=for-the-badge&labelColor=04070d)
![Voz](https://img.shields.io/badge/Narra%C3%A7%C3%A3o-voz%20neural%20pt--BR-00ff9c?style=for-the-badge&labelColor=04070d)
![Zero dependências](https://img.shields.io/badge/depend%C3%AAncias-zero-8a9bb0?style=for-the-badge&labelColor=04070d)

</div>

---

## ✨ O que é

Um *motion graphic* em **um único arquivo HTML**, sem bibliotecas, sem build e sem internet. Ele começa pedindo autorização de áudio, conduz a pessoa por **17 cenas** e termina com a mensagem: **"Pense antes de clicar."**

Estilo visual: neon verde e ciano sobre fundo escuro, chuva de código ao fundo, linhas de varredura estilo CRT, efeitos de glitch e contadores animados.

## 🖼️ Galeria

| Abertura | Simulador de defesa |
|:---:|:---:|
| <img src="assets/01-abertura.png" alt="Abertura"> | <img src="assets/02-simulador.png" alt="Simulador de defesa"> |

| Caso real (WannaCry) | Final |
|:---:|:---:|
| <img src="assets/03-caso.png" alt="Caso WannaCry"> | <img src="assets/04-final.png" alt="Final"> |

## 🎬 Roteiro das cenas

| # | Cena | O que acontece |
|:-:|------|----------------|
| 1 | **Abertura** | Escudo se desenha sozinho e o título aparece com brilho neon |
| 2 | **A ameaça é real** | Phishing, ransomware e brechas em sistemas desatualizados |
| 3 | **Senha fraca = porta aberta** | `123456` é quebrada em menos de 1 segundo e vira uma senha forte |
| 4 | **Alguém tenta entrar** | Três tentativas de acesso e o que acontece sem proteção |
| 5 | **Configure sua defesa** | 🕹️ Simulador interativo (a animação pausa até você continuar) |
| 6–15 | **10 casos reais** | O que aconteceu, falha explorada, configuração preventiva e lição |
| 16 | **Sua defesa** | Senhas fortes, verificação em 2 etapas, backup e atualizações |
| 17 | **Pense antes de clicar** | Fechamento |

## 🕹️ Simulador de defesa

Ligue ou desligue as defesas e rode os ataques para ver o resultado no log.

| Defesas configuráveis | Ataques simulados |
|-----------------------|-------------------|
| Senha forte e única | Força bruta |
| Verificação em 2 etapas | Phishing |
| Atualizações automáticas | Senha vazada reutilizada |
| Backup offline | Brecha em software antigo |
| Treinamento anti-phishing | Ransomware |
| Bloqueio após 3, 5 ou 10 tentativas | Botão **Rodar todos** |

Os resultados são simplificados, para fins didáticos: 🟢 bloqueado, 🟡 recuperado (backup) ou 🔴 invadido, sempre com a explicação do motivo.

## 📚 Os 10 casos reais

| # | Caso | Ano | Tipo de falha | Lição principal |
|:-:|------|:---:|---------------|-----------------|
| 1 | **WannaCry** | 2017 | Falha de atualização | Não mantenha serviços antigos e vulneráveis habilitados |
| 2 | **Equifax** | 2017 | Software desatualizado | Atualize rapidamente as aplicações críticas |
| 3 | **Mirai Botnet** | 2016 | Senhas padrão | Nunca coloque IoT na internet com credenciais de fábrica |
| 4 | **Capital One** | 2019 | Configuração incorreta na nuvem | Um servidor comprometido não deve ter acesso irrestrito aos dados da nuvem |
| 5 | **Target** | 2013 | Falta de segmentação | Fornecedores não devem ter acesso livre à infraestrutura interna |
| 6 | **Colonial Pipeline** | 2021 | Acesso remoto sem MFA | Uma conta esquecida pode ser a porta de entrada de toda a organização |
| 7 | **NotPetya** | 2017 | Falta de isolamento de rede | Impeça a movimentação lateral, não só a entrada |
| 8 | **Heartbleed** | 2014 | Biblioteca vulnerável | Bibliotecas também precisam ser atualizadas |
| 9 | **SQL Slammer** | 2003 | Serviço vulnerável exposto | Um serviço exposto pode se propagar em velocidade extrema |
| 10 | **Morris Worm** | 1988 | Senhas e serviços inseguros | Serviços expostos e autenticação fraca continuam sendo riscos atuais |

## 🔊 Áudio e narração

- **Autorização:** ao abrir, o motion pergunta se a pessoa quer ativar o áudio. Dá para continuar sem áudio e ligar depois pelo botão 🔊.
- **Micro sons:** zumbido ambiente, alarmes, glitch, acordes de sucesso e cliques, todos sintetizados com a **Web Audio API** (sem arquivos de som).
- **Narração:** 47 trechos de voz neural em português do Brasil, gerados com o modelo **Piper (`pt_BR-faber-medium`)** e embutidos no HTML em MP3 (base64).
- **Sincronia:** em cada caso, os blocos aparecem no momento em que a voz fala sobre eles, e a cena só avança quando a fala termina. As pausas entre frases foram ajustadas manualmente.
- **Plano B:** se os áudios não carregarem, o motion usa a voz do navegador (Web Speech API) ou segue por tempo fixo.

## 🎮 Controles

| Botão | Função |
|:-----:|--------|
| ◀ / ▶ | Cena anterior / próxima (com trava de ~1,1 s para evitar sobreposição) |
| ⏸ / ⏵ | Pausar / retomar |
| 🔊 / 🔇 | Ligar / desligar som e narração |
| ↻ repetir | Reiniciar do começo |
| continuar ▶ | Sair do simulador e seguir |

## 🚀 Como usar

1. Baixe o arquivo `motion-ciberseguranca.html`.
2. Abra em qualquer navegador moderno (Chrome, Edge, Firefox ou Safari).
3. Escolha **Ativar áudio** ou **Continuar sem áudio**.

Não precisa de servidor, instalação ou internet. Para publicar, basta colocar o arquivo no **GitHub Pages**, no **Netlify** ou em qualquer hospedagem estática.

## 🧩 Estrutura do projeto

```text
.
├── motion-ciberseguranca.html   # o motion completo (HTML + CSS + JS + áudios)
├── README.md
└── assets/
    ├── 01-abertura.png
    ├── 02-simulador.png
    ├── 03-caso.png
    └── 04-final.png
```

## 🛠️ Personalização

- **Casos reais:** edite o array `D` no JavaScript. Cada item tem nome, ano, tipo de falha, ícone, o que aconteceu, falha explorada, prevenção e lição.
- **Textos da narração:** ficam no array `NR`. Se mudar um texto, é preciso gerar o áudio dele de novo (o objeto `window.VO` guarda os MP3 em base64, um por trecho).
- **Cores:** variáveis `--g` (verde), `--c` (ciano) e `--r` (vermelho) no início do CSS.
- **Duração das cenas:** array `dur` (em milissegundos).

## ⚠️ Observações

- Navegadores só tocam áudio depois de uma interação, por isso existe a tela inicial.
- Os resultados do simulador são didáticos e simplificados, não substituem uma análise de segurança real.
- Antes de usar a voz Piper em um produto comercial, confira a licença do modelo de voz.

---

<div align="center">

**Segurança não é produto, é hábito.** 🛡️

</div>
