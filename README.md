# Auction Bid Assistant - RPA Project 🚀

Este projeto consiste em um **Assistente de Lances** desenvolvido para monitorar variações de preços em sites de leilão de estrutura desconhecida e automatizar interações com sistemas públicos.

## 🎯 Objetivo
O desafio é desenvolver um sistema que monitore um campo específico (definido pelo usuário via XPath/Seletor) em uma URL arbitrária. Ao identificar uma mudança de preço, o sistema interage com outra página pública (ex: Gmail) para notificar os valores antigo e novo.

## 🛠️ Tecnologias e Arquitetura
- **Linguagem:** Python 3.x (escolhida pela robustez e simplicidade das bibliotecas de automação).
- **Automação Web:** Selenium com `undetected-chromedriver`.
- **Backend/API:** FastAPI.
- **Documentação:** MkDocs (Site estático profissional).
- **Testes:** Pytest (Testes unitários automatizados).

## ✨ Funcionalidades (Critérios de Pontuação)
- **Validação Robusta:** O sistema valida o nome do usuário (mín. 3 caracteres), URLs, timeouts e tipos de dados de entrada para evitar travamentos.
- **Monitoramento Inteligente:** Identifica a posição do elemento na página (logando XPath/Regex no console) e monitora alterações em tempo real.
- **Ação Automatizada:** Registra a alteração e aciona botões de envio em sistemas terceiros.
- **Logging de Ações:** Log detalhado de todas as atividades do usuário e do sistema.
- **Análise de Complexidade:** Cálculo de Big O incluído na documentação e comentários do código.

## 📊 Análise de Complexidade (Big O)
O algoritmo de monitoramento opera em um ciclo de tempo definido pelo usuário ($T$). 
- **Tempo:** $O(n)$, onde $n$ é o número de iterações do loop de monitoramento. Por ciclo, a busca do elemento via XPath é $O(1)$ caso o DOM não mude drasticamente.
- **Espaço:** $O(1)$, pois o sistema armazena apenas variáveis constantes de estado (valor antigo e novo).

## 🚀 Como Executar
1. Instale as dependências: `pip install -r requirements.txt`
2. Inicie a API: `uvicorn src.main:app --reload`
3. Acesse a documentação técnica gerada: `mkdocs serve`

## 👥 Grupo e Evolução (Git History)
Este repositório utiliza o padrão de commits semânticos para contar a história da evolução do projeto:
- `feat`: Novas funcionalidades.
- `fix`: Correção de bugs.
- `docs`: Atualizações na documentação.
